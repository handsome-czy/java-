#### 关键字This

> 当方法局部变量和类的成员变量重名的时候，会自动根据就近原则，优先使用局部变量。
>
> 如果需要访问本类中成员变量，需要使用格式：
>
> this.成员变量名
>
> 代码：
>
> ```
> //关键字this的使用
> public class Demo05 {
>     String name;
>     public void hello(String name){
>         System.out.println(name+"你好我是"+this.name);//虽然成员变量名称和局部变量名称一样但引用关键字this
>     }
> }
> ```

 代码：根据Demo05类创建str对象

```
public class Hello {
    public static void main(String[] args) {
        Demo05 str = new Demo05();
        str.name = "蔡徐坤";
        str.hello("鹿晗");
    }
}
```