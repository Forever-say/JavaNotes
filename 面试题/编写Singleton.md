### 编写Singleton

Singleton：单例设计模式，是软件开发中最常用的设计模式之一

单：唯一

例：实例



要点：

饿汉式

直接实例化饿汉式(简洁直观)

枚举类(最简洁)

静态代码块饿汉式(适合复杂实例化)



懒汉式

线程不安全(为什么不安全)

线程安全(适用于多线程)

静态内部类形式(适用于多线程)



```java
//在内部类被加载和初始化时，才创建INSTANCE的实例对象
//静态内部类不会随着外部类的加载和初始化而初始化，它要单独加载和初始化
//因为在内部类加载和初始化时，创建的，因此线程安全
public class Singleton{
    private Singleton(){

    }

    private static class Inner{
        private static final Singleton INSTANCE = new Singleton();
    }

    public static Singleton getInstance(){
        return Inner.INSTANCE;
    }
}
```