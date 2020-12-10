---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Java关键字相关知识点总结"
subtitle: ""
summary: "关键字的前世今生"
authors: []
tags: [关键字]
categories: [OOP]
date: 2018-11-23T23:31:05+08:00
lastmod: 2018-11-23T23:31:05+08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

0x00 概念
---------------------------------

首先区分两个概念：关键字和保留字。关键字指事先定义的，用来表示一种数据类型或者程序结构的对于编译器有特殊意义的“字符串”。而保留字则是预留的关键字，即现在还没有用到，但以后可能会作为关键字被使用。
所以，认识关键字与保留字的一个基本的作用，起码就在于为变量命名时不至于与关键字冲突、或者与“未来的关键字”冲突（如果使用了关键字、保留字作为变量命名，比较智能的IDE是会报错的，但如果用记事本或者在线刷题那就不一定有这么好的福利了）。当然，要真正使程序高效、健壮，那就要深刻认识各个关键字的内在含义。


0x01 关键字总览
---------------------------------

目前而言，Java的关键字有50个，还有一些保留字。其中保留字包括：goto、const，这是C++中的关键字。而关键字可大致分为9类。清单如下：

- 包相关（2个）：import、package
- 访问控制相关（3个）：public、protected、private
- 类、接口、抽象类、对象相关（6个）：class、interface、abstract、implements、extends、new
- 数据类型相关（9个）：void、short、int、long、float、double、byte、char、boolean、null
- 异常处理相关（5个）：try、catch、finally、throw、throws
- 程序控制结构相关（13个）：if、else、switch、case、break、default、for、continue、while、do、return、instanceof
- 修饰类、方法、属性、变量相关（7个）：static、final、native、synchronized、transient、volatile、strictfp
- 变量引用相关（2个）：super、this
- 其他（2个）：assert、enum


0x02 包相关
----------------------------------

类似于C++中的命名空间，java提供了包机制用于区分不同组织、个人所编写的类，有效防止命名冲突，方便共享java程序。

- package关键字
  声明编译单元属于某个类库。如果使用package语句，它必须是文件中除了注释以外的第一行语句。

- import关键字
  导入包。

0x03 访问控制相关
----------------------------------

对于java而言，访问控制权限可分为：public、protected、默认的、private，上述四种访问权限的大小排序是从大到小的，其中默认访问控制权限没有关键字。

- public
  接口访问权限

- protected
  继承访问权限

- private
  私有的


0x04类、接口、抽象类、对象相关
----------------------------------

- class
  定义类的关键字

- interface
  定义接口的关键字。

- abstract class
  定义抽象类的关键字

- extends
  继承类或接口的关键字。类继承类，接口继承接口

- implements
  实现接口的关键字。一个类实现了某个接口就必须要实现该接口下的所有方法。

- new
  实例化对象。java完全采用了动态分配配内存的方式，即使用new关键字来动态创建对象实例，当对象不再被使用时，由垃圾回收器（GC）自动销毁对象，释放其占用的内存空间。

- null
  表示空对象。

0x04 数据类型相关
----------------------------------

- void
  空返回类型，用于修饰函数。

- byte
  字节类型，占8 bit。因java中byte类型默认是带符号的，所以其范围为-2^7~2^7-1，即-128~127。
  直接对两个byte类型的变量进行相加，其会自动转型为int，要对其进行强制转型。

- short
  短整型，占16 bit。范围-2^15~2^15-1。即Short.MIN_VALUE~Short.MAX_VALUE。

- int
  整型，占32 bit。范围-2^31~2^31-1。

- long
  长整型，占64 bit。范围-2^63~2^63-1。尽管long的范围已经比较大了，但要求如斐波那契数列数值时，还是很容易失效，比如要求斐波那契数列第一百个数，就超出了long类型所能表示的范围，此时考虑使用大整数，java中提供了BigInteger类型。

- float
  浮点型，占32 bit。

- double
  双精度型，占64 bit。java中double和float都是以科学计数法的方式进行表示。

- char
  字符型，16 bit。

- boolean
  布尔类型，取值true or false。


0x05 异常处理相关
----------------------------------

- try
  捕获异常。 包含可能发生异常的语句块。

- catch
  处理异常。包含对异常的处理，一般用于提示开发者代码中不对劲的地方。

- finally
  指定不管是否发生异常都要执行的语句块。

- throw
  抛出异常对象。

- throws
  声明一个方法可能会抛出某种异常。（抛给调用该方法的地方）




0x06 程序控制结构相关
----------------------------------

if、else、switch、case、break、default、for、continue、while、do、return、instanceof

0x07 修饰类、方法、属性、变量相关
----------------------------------

- final
  final表示最终的，其用于修饰的对象都不可更改。final可修饰的内容包括：
    - 类
      用final修饰的类不可被继承。
    - 普通方法
      用final修饰ide普通方法不可被重写。（构造方法本身就不可被重写）
    - 属性、变量、常量、形参
      不可被改变。当final修饰基本类型时，参数值在方法体中不可被改变；修饰引用类型时，参数变量所引用的对象也不可改变。

- static
  一般来说，在创建类时，就是在描述那个类ide对象的外观和行为，在使用new创建对象之前，实际上并没有获得任何对象，只有当执行new之后，对象的数据存储空间才被分配，才可以被外界所调用。但如果希望特定的域不与类的任何对象关联在一起，即不创建对象也能够调用该方法，就可以考虑使用static关键字来修饰特定的域。
  当使用static关键字声明某个属性或方法时，就意味着这个域或者方法不会与包含它的那个类的任何对象实例关联在一起。用static修饰的域或者变量存储在静态存储区域，在类被创建时优先被加载到内存中。
  static可以修饰的内容包括
    - 属性
    - 常量
    - 内部类
    - 普通方法
      要注意，static不能修饰构造方法。
    - 代码块
      用static修饰的代码块优先与构造方法执行


- native
  用于扩展java程序的功能，告知JVM该方法在外部定义，一般配合。java在运行速度上比C++要慢，对访问操作系统底层的支持也不够好，因此可使用native声明某些方法是由其他语言实现的（如C++）。

- volatile
  数据同步。

- synchronized
  针对代码块的同步锁

- transient
  瞬时的。

- strictfp
  可用于类、接口或方法。使用strictfp关键字声明一个方法时，该方法中所有的float和double表达式都严格遵守FP-strict的限制，符合IEEE-754规范。

0x09 变量引用相关
----------------------------------

- super
  用于表示基类对象。

- this
  用于表示当前对象。

0x10 其他关键字
----------------------------------

- assert
  断言，在代码中捕捉一些假设，看我们的假设是否成立，如果假设不成立，即断言中的布尔表达式为false，则会停止运行程序，抛出AssertionError错误（前提是要先支持断言），断言也可看作是更高级的异常捕获，主要在于它引入了程序猿的先验。Eclipse、MyEclipse中默认关闭断言，可在偏好设置中修改VM参数进行开启。

- enum
  枚举。

0x11 问题
-----------------------------------

1. 内部类
2. GC需要解决的问题：

   （1） 哪些对象需要被回收？

   （2） 何时回收这些对象？
   
   （3） 如何回收这些对象？