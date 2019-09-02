#Java访问权限
访问权限	|本类|本包的类	|子类|非子类的其他包的类
:--|:--:|:--:|:--:|:--:
public|✔|✔|✔|✔|
protected|✔|✔|✔|✘|
包访问权限（default）|✔|✔|✘|✘|
private|✔|✘|✘|✘|
1.类的访问权限
```
类既不可以是private（这样任何类都不能访问它），也不可以是protected的（但内部类除外）
```
2.抽象方法的访问权限
```
public abstract class AbstractClass {

    /**
     * 不合法的代码，子类无法继承
     */
    //private abstract void print();

    /**
     * 不建议的代码 这样虽然同一个包下的子类可以继承实现该方法，但是不同包下子类却无法继承
     */
    //abstract void print2();

    protected abstract  void print3();

    public abstract  void print4();
}
```
3.构造方法访问权限
访问权限	|描述
:--|:--:
public|所有类都可以访问
protected|子类可以继承该类，本包可以访问，其它包非子类无法访问
包访问权限（default）|本包可以访问，其它包无法访问
private|不允许在其它类中直接创建该类的对象
```
/**
 * 以下为单列模式实现方式
 */
public class SingletonDemo {

    private static SingletonDemo singletonDemo = new SingletonDemo();

    private SingletonDemo() {};

    public static SingletonDemo getSingleton() {
        return singletonDemo;
    }
}
```