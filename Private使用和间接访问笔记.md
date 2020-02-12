### Private使用

> 问题：定义变量是无法阻止不合理的数值被设置进来。

> 解决：用private关键字将需要保护的变量进行修饰。

> 注意：使用private进行修饰，在本类仍然可以继续随意访问，但是超出本类范围就不可以“直接访问”了。

### Set和Get的使用

> 间接访问private成员变量就定义一对set Xxx和get Xxx
>
> set：专门向成员变量设置数据
>
> ​		无返回值，有参数参数类型必须和成员变量一至
>
> get：专门向成员变量获取数据
>
> ​		无参数，有返回值返回值类型和成员变量相对应

代码：成员变量与成员方法

```
public class Demo04 {
    //成员变量
    String name;//姓名
    private int age;//年龄
    //成员方法
    public void show() {
        System.out.println("我叫" + name + "今年" + age);
    }
    //专门向age设置数据，有参数无返回值，参数类型和要set的成员变量保持一致
    public void setAge(int num) {
        if (num < 0) {
            num = 0;
            System.out.println("格式错误");
        }
        age = num;
    }
    //专门获取age的数据，无参数有返回值返回值类型和成员变量相对应
    public int getAge() {
        return age;
    }
}
```

代码：调用成员变量与方法

```
public class Demo004 {
    public static void main(String[] args) {
        Demo04 person = new Demo04();
        person.show();
        person.name = "小明";
        // person.age = 18;//直接调用不可以
        person.setAge(20);//间接调用
        person.show();
    }
}
```

