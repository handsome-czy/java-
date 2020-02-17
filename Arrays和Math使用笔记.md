### Arrays和Math使用

1. public  static  String  to  string(数组);//将参数数组转变字符串
2. public  static  voiid  sord(数组);数组排序
3. String--->>数组，用 toCharArrays

1,2演示代码：

```
public class Demo01 {
    public static void main(String[] args) {
        //将参数数组变成字符串
        int[] array = {1, 2, 3, 4};
        System.out.println(Arrays.toString(array));

        //默认升序排列数组，int类型
        int[] array1 = {4, 3, 2, 1};
        Arrays.sort(array1);
        //循环输出
        //for (int i = 0; i < array1.length; i++) {
        // System.out.println(array1[i]);
        // }
        //直接转换成字符串输出
        System.out.println(Arrays.toString(array1));
        //字符串类型,自动按照字母升序
        String[] array2 = {"ccc", "bbb", "aaa"};
        Arrays.sort(array2);
        System.out.println(Arrays.toString(array2));

    }
}
```

3.演示代码：

```
public class Demo02 {
    public static void main(String[] args) {
        String str = "abcdsdhfsj";
        //将字符串转换成字符数组
        char[] chars = str.toCharArray();
        Arrays.sort(chars);
        //逆序输出
        for (int i = chars.length - 1; i >= 0; i--) {
            System.out.println(chars[i]);
        }
    }
}
```

#### Math

代码演示：

```
public class math {
    public static void main(String[] args) {
        //绝对值
        System.out.println(Math.abs(3.14));//3.14
        System.out.println(Math.abs(-3.14));//3.14

        //向上取整,不会根据四舍五入
        System.out.println(Math.ceil(3.1));//4.0
        System.out.println(Math.ceil(2.2));//3.0

        //向下取整，不会四舍五入
        System.out.println(Math.floor(30.1));//30.0
        System.out.println(Math.floor(30.9));//30.0

        //四舍五入
        System.out.println(Math.round(20.4));//20
        System.out.println(Math.round(20.5));//21
    }
}
```