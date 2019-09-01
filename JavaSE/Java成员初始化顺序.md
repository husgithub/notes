1.定义一个简单实体Dog
```
public class Dog {

    private String name;

    public Dog(String name) {
        System.out.println("Dog Constructor...,dog's name: " + name);
        this.name = name;
    }

    public String getname() {
        return name;
    }

    public void setname(String name) {
        this.name = name;
    }

    public void print() {
        System.out.println("dog's name is: " + name);
    }
}
```
2.定义测试类InitSeqParent
```
public class InitSeqParent {

    static Dog a = new Dog("A");

    Dog b = new Dog("B");

    static Dog c;

    static {
        c = new Dog("C");
    }

    Dog d;

    {
        d = new Dog("D");
    }

    InitSeqParent() {
        System.out.println("InitSeqParent Constructor...");
    }

}
```
3.定义InitSeqParent子类InitSeqChild
```
public class InitSeqChild extends InitSeqParent {

    static Dog a = new Dog("E");

    Dog b = new Dog("F");

    static Dog c ;

    static {
        c = new Dog("G");
    }

    Dog d ;

    {
        d = new Dog("H");
    }

    InitSeqChild(){
        System.out.println("InitSeqChild Constructor...");
    }

    public static void main(String[] args) {
        new InitSeqChild();
    }
}
```
4.查看打印结果
>Dog Constructor...,dog's name: A
Dog Constructor...,dog's name: C
Dog Constructor...,dog's name: E
Dog Constructor...,dog's name: G
Dog Constructor...,dog's name: B
Dog Constructor...,dog's name: D
InitSeqParent Constructor...
Dog Constructor...,dog's name: F
Dog Constructor...,dog's name: H
InitSeqChild Constructor...
>
4.结论
- Java成员初始化顺序为：
父类静态变量/静态代码块 > 子类静态变量/静态代码块 > 父类非静态变量/非静态代码块 > 父类构造方法 > 子类类非静态变量/非静态代码块 > 子类构造方法
- 即使没有显式地使用static关键字，构造器实际上也是静态方法。因此当创建InitSequenceTest类型对象或者使用静态方法时，Java解释器会查找类路径并加载InitSequenceTest.class，有关静态初始化的所有方法都会执行
- 静态初始化只在Class对象首次加载的时候执行一次