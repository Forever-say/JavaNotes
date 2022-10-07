### Date



date有两个类

java.util.Date类

​		  |---java.sql.Date类

1.两个构造器的使用



2.两个方法的使用

toString(); 显示当前年、月、日、时、分、秒

getTime();获取时间戳

```java
Date date = new Date();  //获取当前时间的对象
System.out.println(date.toString());
//Thu Jul 28 20:29:50 CST 2022
System.out.println(date.getTime());
        //1659011472778 毫秒数

Date date2 = new Date(1659011472778L); //创建指定时间戳的对象
```



3.java.sql.Date对应着数据库中的日期类型的变量

实例化

```java
java.sql.Date date = new java.sql.Date(1659011472778L);
System.out.println(date);
        //2022-07-28
```

util.Date --->sql.Date对象

通过getTime()进行时间戳的传递