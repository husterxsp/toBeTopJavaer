[![](http://www.hollischuang.com/wp-content/uploads/2018/10/Hollis.png)](https://www.hollischuang.com)

## To Be Top Javaer  -  Java工程师成神之路

![](https://img.shields.io/badge/version-v2.0.0-green.svg) ![](https://img.shields.io/badge/author-Hollis-yellow.svg) ![](https://img.shields.io/badge/license-GPL-blue.svg)


| 主要版本 | 更新时间       | 备注             |
| ---- | ---------- | -------------- |
| v1.0 | 2015-08-01 | 首次发布           |
| v1.1 | 2018-03-12 | 增加新技术知识、完善知识体系 |
| v2.0 | 2019-02-19 | 结构调整，更适合从入门到精通；<br>进一步完善知识体系； <br>新技术补充；|

## 一、基础篇

### 面向对象

#### 什么是面向对象

面向对象、面向过程

> 面向过程：以事件为中心，按照时间发生的顺序，调用一系列函数。开发简单但是不易于维护。
>
> 面向对象：以对象为中心，把涉及到的事物抽象成对象。好处：结构化、模块化，易于维护。
> [https://zhuanlan.zhihu.com/p/28427324](https://zhuanlan.zhihu.com/p/28427324)


面向对象的[三大基本特征](/basics/java-basic/characteristics.md)和[五大基本原则](/basics/java-basic/principle.md)

> 《think in java》第一章有介绍
>
> 封装、继承、多态：
>
> 封装：一些内部数据可以被不被暴露给外部访问，从而保护数据的安全。可以通过private、protected等关键字实现。
>
> 继承：子类继承父类，可以复用父类的方法什么的。
>
> 多态：后期绑定/动态绑定/运行时绑定。多态机制使具有不同内部结构的对象可以共享相同的外部接口。
>
> 前期绑定：程序执行前就进行绑定，由编译器和连接程序实现
>
> 后期绑定：运行时根据对象的类型进行绑定。对象种会有某种类型信息
>
> 绑定：把方法调用同方法主体关联起来。
>
> http://www.cnblogs.com/hnrainll/archive/2012/09/18/2690846.html
>
>
> 组合优于继承，组合确实比继承更加灵活，也更有助于代码维护。
>
> 继承：会破坏代码的封装性，子类与父类之间紧密耦合，子类依赖于父类的实现，子类缺乏独立性
>
> 组合 vs 继承：https://www.hollischuang.com/archives/1319
>
>
>
> 单一职责原则：一个类，最好只做一件事
>
> 开闭原则：软件实体应该是可扩展的，而不可修改的
>
> 里氏替换原则：子类必须能够替换其基类
>
> 依赖倒置：依赖于抽象。具体而言就是高层模块不依赖于底层模块，在依赖之间定义一个抽象的接口使得高层模块调用接口，而底层模块实现接口的定义
>
> 接口隔离：用多个小的专门的接口，而不要使用一个大的总接口。一个类对另外一个类的依赖应该建立在最小的接口上，不要强迫依赖不用的方法，这是一种接口污染。
>
> https://www.hollischuang.com/archives/220

#### 平台无关性

Java如何实现的平台无关


> 平台无关有两种：源代码级和目标代码级。
>
> 我们常说的跨平台，或者平台无关，指的就是目标代码，或者说是软件交付件跨平台。
>
> Java源码编译出来的字节码文件，JVM会解析翻译成机器语言，即JVM帮我们把字节码翻译成机器语言的过程中就已经充分考虑到对应平台的特性了。


[JVM还支持哪些语言（Kotlin、Groovy、JRuby、Jython、Scala）](/basics/java-basic/jvm-language.md)

> ErJang、Clojure
>
> https://coolshell.cn/articles/2631.html
>
> https://www.zhihu.com/question/20003582

#### 值传递

值传递、引用传递

> 基本类型一般是值传递、引用类型一般是引用传递
>
> https://www.zhihu.com/question/31203609/answer/50992895

[为什么说Java中只有值传递](/basics/java-basic/java-pass-by.md)

> 当传入引用类型的时候，传入的是引用类型的地址，当修改这个传入变量的地址后，其实已经是在修改另一个对象了，所以说并没有修改原来的对象。
>
> |          |         值传递         |        引用传递        |
> | -------- | :--------------------: | :--------------------: |
> | 根本区别 |     会创建副本对象     |     不创建副本对象     |
> | 所以     | 函数中无法改变原始对象 | 函数中可以改变原始对象 |

#### 封装、继承、多态

什么是多态、[方法重写与重载](/basics/java-basic/overloading-vs-overriding.md)

> 重载：同一个类中的方法，有相同的函数名，但是有不同的参数列表
>
> 重写：子类重写父类方法
>
> https://www.hollischuang.com/archives/1308

为什么函数签名没有返回值？

> 只要编译器可以根据语境明确判断出语义，比如在int x =f()中，那么的确可以据此却分重载方法。不过，有时你并不关心方法的返回值，你想要的是方法调用的其他效果，这时你可能会调用方法而忽略其返回值。所以，如果像下面这样调用方法：
> f()；
>
> https://bluestar.iteye.com/blog/416527

Java的继承与实现

> implements 可以实现多重继承

interface 和 abstract 区别？

>
>
> https://data-flair.training/blogs/java-extends-vs-implements/

构造函数与默认构造函数



[类变量、成员变量和局部变量](/basics/java-basic/variable.md)

成员变量和方法作用域

### Java基础知识

#### 基本数据类型

7种基本数据类型：整型、浮点型、布尔型、字符型

整型中byte、short、int、long的取值范围

什么是浮点型？什么是单精度和双精度？为什么不能用浮点型表示金额？

> 浮点数会有精度丢失的问题，可以用 BigDecimal
>
> https://blog.csdn.net/bruce128/article/details/52529734

#### 自动拆装箱

[什么是包装类型、什么是基本类型、什么是自动拆装箱](/basics/java-basic/boxing-unboxing.md)

[Integer的缓存机制](/basics/java-basic/integer-cache.md)

> -128 ~ 127 缓存
>
> 可以通过vm potion `-XX:AutoBoxCacheMax=1000`可以修改，注意最小也是127。
>
> ```java
>     /**
>      * Cache to support the object identity semantics of autoboxing for values between
>      * -128 and 127 (inclusive) as required by JLS.
>      *
>      * The cache is initialized on first usage.  The size of the cache
>      * may be controlled by the {@code -XX:AutoBoxCacheMax=<size>} option.
>      * During VM initialization, java.lang.Integer.IntegerCache.high property
>      * may be set and saved in the private system properties in the
>      * sun.misc.VM class.
>      */
>
>     private static class IntegerCache {
>         static final int low = -128;
>         static final int high;
>         static final Integer cache[];
>
>         static {
>             // high value may be configured by property
>             int h = 127;
>             String integerCacheHighPropValue =
>                 sun.misc.VM.getSavedProperty("java.lang.Integer.IntegerCache.high");
>             if (integerCacheHighPropValue != null) {
>                 try {
>                     int i = parseInt(integerCacheHighPropValue);
>                     i = Math.max(i, 127);
>                     // Maximum array size is Integer.MAX_VALUE
>                     h = Math.min(i, Integer.MAX_VALUE - (-low) -1);
>                 } catch( NumberFormatException nfe) {
>                     // If the property cannot be parsed into an int, ignore it.
>                 }
>             }
> ```
>
> Integer的缓存上限可以通过Java虚拟机参数修改，Byte、Short、Long、Character的缓存则没法修改。
>
> https://www.jianshu.com/p/c12ab3f675cc

#### String

[字符串的不可变性](/basics/java-basic/final-string.md)

[JDK 6和JDK 7中substring的原理及区别](/basics/java-basic/substring.md)

replaceFirst、replaceAll、replace区别、

String对“+”的重载、字符串拼接的几种方式和区别

String.valueOf和Integer.toString的区别、

[switch对String的支持](/basics/java-basic/switch-string.md)

字符串池、常量池（运行时常量池、Class常量池）、intern

#### 熟悉Java中各种关键字

transient、instanceof、volatile、synchronized、final、static、const 原理及用法。

> transient：控制变量的序列化，在变量声明前加上该关键字，可以阻止该变量被序列化到文件中，在被反序列化后，transient 变量的值被设为初始值，如 int 型的是 0，对象型的是 null。
>
> https://www.hollischuang.com/archives/1150
>
> serialVersionUID：控制反序列化
>
> https://github.com/husterxsp/java-learning/blob/master/daily/083-serialVersionUID.md
>
> instanceof：判断是否有父类、子类以及实现接口的关系
>
> https://stackoverflow.com/questions/7526817/use-of-instance-of-in-java
>
> volatile：原子性、可见性（参见《java并发编程的艺术》）
>
> synchronized：通过字节码指令`monitorenter`和`monitorexit` 加锁（参见《java并发编程的艺术》）
>
> final：
>
> static：
>
> const：

#### 集合类

常用集合类的使用、ArrayList和LinkedList和Vector的区别 、SynchronizedList和Vector的区别、HashMap、HashTable、ConcurrentHashMap区别、

Set和List区别？Set如何保证元素不重复？

Java 8中stream相关用法、apache集合处理工具类的使用、不同版本的JDK中HashMap的实现的区别以及原因

Collection和Collections区别

Arrays.asList获得的List使用时需要注意什么

Enumeration和Iterator区别

fail-fast 和 fail-safe

CopyOnWriteArrayList、ConcurrentSkipListMap

#### 枚举

枚举的用法、枚举的实现、枚举与单例、Enum类

Java枚举如何比较

switch对枚举的支持

枚举的序列化如何实现

枚举的线程安全性问题

#### IO

字符流、字节流、输入流、输出流、

同步、异步、阻塞、非阻塞、Linux 5种IO模型

BIO、NIO和AIO的区别、三种IO的用法与原理、netty

#### Java反射与javassist

反射与工厂模式、 反射有什么作用

Class类

`java.lang.reflect.*`

#### 动态代理

静态代理、动态代理

动态代理和反射的关系

动态代理的几种实现方式

AOP

#### 序列化

什么是序列化与反序列化、为什么序列化、序列化底层原理、序列化与单例模式、protobuf、为什么说序列化并不安全

#### 注解

元注解、自定义注解、Java中常用注解使用、注解与反射的结合

Spring常用注解

#### JMS

什么是Java消息服务、JMS消息传送模型

#### JMX

`java.lang.management.*`、 `javax.management.*`

#### 泛型

泛型与继承、类型擦除、泛型中K T V E ？ object等的含义、泛型各种用法

限定通配符和非限定通配符、上下界限定符extends 和 super

List<Object>和原始类型List之间的区别?

List<?>和List<Object>之间的区别是什么?

#### 单元测试

junit、mock、mockito、内存数据库（h2）

#### 正则表达式

`java.lang.util.regex.*`

#### 常用的Java工具库

`commons.lang`, `commons.*...` `guava-libraries` `netty`

#### API&SPI

API、API和SPI的关系和区别

如何定义SPI、SPI的实现原理

#### 异常

异常类型、正确处理异常、自定义异常

Error和Exception

异常链、try-with-resources

finally和return的执行顺序

#### 时间处理

时区、冬令时和夏令时、时间戳、Java中时间API

格林威治时间、CET,UTC,GMT,CST几种常见时间的含义和关系

SimpleDateFormat的线程安全性问题

Java 8中的时间处理

如何在东八区的计算机上获取美国时间

#### 编码方式

Unicode、有了Unicode为啥还需要UTF-8

GBK、GB2312、GB18030之间的区别

UTF8、UTF16、UTF32区别

URL编解码、Big Endian和Little Endian

如何解决乱码问题

#### 语法糖

Java中语法糖原理、解语法糖

语法糖：switch 支持 String 与枚举、泛型、自动装箱与拆箱、方法变长参数、枚举、内部类、条件编译、 断言、数值字面量、for-each、try-with-resource、Lambda表达式、

### 阅读源代码

String、Integer、Long、Enum、BigDecimal、ThreadLocal、ClassLoader & URLClassLoader、ArrayList & LinkedList、 HashMap & LinkedHashMap & TreeMap & CouncurrentHashMap、HashSet & LinkedHashSet & TreeSet

### Java并发编程

#### 并发与并行

什么是并发

什么是并行

并发与并行的区别

#### 线程

线程的实现、线程的状态、优先级、线程调度、创建线程的多种方式、守护线程

线程与进程的区别

#### 线程池

自己设计线程池、submit() 和 execute()、线程池原理

为什么不允许使用Executors创建线程池

#### 线程安全

死锁、死锁如何排查、线程安全和内存模型的关系

#### 锁

CAS、乐观锁与悲观锁、数据库相关锁机制、分布式锁、偏向锁、轻量级锁、重量级锁、monitor、

锁优化、锁消除、锁粗化、自旋锁、可重入锁、阻塞锁、死锁

#### 死锁

死锁的原因

死锁的解决办法

#### synchronized

synchronized是如何实现的？

synchronized和lock之间关系、不使用synchronized如何实现一个线程安全的单例

synchronized和原子性、可见性和有序性之间的关系

#### volatile

happens-before、内存屏障、编译器指令重排和CPU指令重

volatile的实现原理

volatile和原子性、可见性和有序性之间的关系

有了symchronized为什么还需要volatile

#### sleep 和 wait

#### wait 和 notify

#### notify 和 notifyAll

#### ThreadLocal

#### 写一个死锁的程序

#### 写代码来解决生产者消费者问题

### 并发包

#### 阅读源代码，并学会使用

Thread、Runnable、Callable、ReentrantLock、ReentrantReadWriteLock、Atomic*、Semaphore、CountDownLatch、、ConcurrentHashMap、Executors

## 二、底层篇

### JVM

#### JVM内存结构

class文件格式、运行时数据区：堆、栈、方法区、直接内存、运行时常量池、

堆和栈区别

Java中的对象一定在堆上分配吗？

#### Java内存模型

计算机内存模型、缓存一致性、MESI协议

可见性、原子性、顺序性、happens-before、

内存屏障、synchronized、volatile、final、锁

#### 垃圾回收

GC算法：标记清除、引用计数、复制、标记压缩、分代回收、增量式回收

GC参数、对象存活的判定、垃圾收集器（CMS、G1、ZGC、Epsilon）

#### JVM参数及调优

-Xmx、-Xmn、-Xms、Xss、-XX:SurvivorRatio、

-XX:PermSize、-XX:MaxPermSize、-XX:MaxTenuringThreshold

#### Java对象模型

oop-klass、对象头

#### HotSpot

即时编译器、编译优化

#### 虚拟机性能监控与故障处理工具

jps, jstack, jmap、jstat, jconsole, jinfo, jhat, javap, btrace、TProfiler

Arthas

### 类加载机制

classLoader、类加载过程、双亲委派（破坏双亲委派）、模块化（jboss modules、osgi、jigsaw）

### 编译与反编译

什么是编译（前端编译、后端编译）、什么是反编译

JIT、JIT优化（逃逸分析、栈上分配、标量替换、锁优化）

编译工具：javac

反编译工具：javap 、jad 、CRF

## 三、 进阶篇

### Java底层知识

#### 字节码、class文件格式

#### CPU缓存，L1，L2，L3和伪共享

#### 尾递归

#### 位运算

用位运算实现加、减、乘、除、取余

### 设计模式

设计模式的六大原则：

开闭原则（Open Close Principle）、里氏代换原则（Liskov Substitution Principle）、依赖倒转原则（Dependence Inversion Principle）

接口隔离原则（Interface Segregation Principle）、迪米特法则（最少知道原则）（Demeter Principle）、合成复用原则（Composite Reuse Principle）

#### 了解23种设计模式

创建型模式：单例模式、抽象工厂模式、建造者模式、工厂模式、原型模式。

结构型模式：适配器模式、桥接模式、装饰模式、组合模式、外观模式、享元模式、代理模式。

行为型模式：模版方法模式、命令模式、迭代器模式、观察者模式、中介者模式、备忘录模式、解释器模式（Interpreter模式）、状态模式、策略模式、职责链模式(责任链模式)、访问者模式。

#### 会使用常用设计模式

单例的七种写法：懒汉——线程不安全、懒汉——线程安全、饿汉、饿汉——变种、静态内部类、枚举、双重校验锁

工厂模式、适配器模式、策略模式、模板方法模式、观察者模式、外观模式、代理模式等必会

#### 不用synchronized和lock，实现线程安全的单例模式

#### 实现AOP

#### 实现IOC

#### nio和reactor设计模式

### 网络编程知识

#### tcp、udp、http、https等常用协议

三次握手与四次关闭、流量控制和拥塞控制、OSI七层模型、tcp粘包与拆包

#### http/1.0 http/1.1 http/2之间的区别

http中 get和post区别

常见的web请求返回的状态码

404、302、301、500分别代表什么

#### http/3

#### Java RMI，Socket，HttpClient

#### cookie 与 session

cookie被禁用，如何实现session

#### 用Java写一个简单的静态文件的HTTP服务器

#### 了解nginx和apache服务器的特性并搭建一个对应的服务器

#### 用Java实现FTP、SMTP协议

#### 进程间通讯的方式

#### 什么是CDN？如果实现？

#### DNS？

什么是DNS 、记录类型:A记录、CNAME记录、AAAA记录等

域名解析、根域名服务器

DNS污染、DNS劫持、公共DNS：114 DNS、Google DNS、OpenDNS

#### 反向代理

正向代理、反向代理

反向代理服务器

### 框架知识

#### Servlet

生命周期

线程安全问题

filter和listener

web.xml中常用配置及作用

#### Hibernate

什么是OR Mapping

Hibernate的缓存机制

Hibernate的懒加载

Hibernate/Ibatis/MyBatis之间的区别

#### Spring

Bean的初始化

AOP原理

实现Spring的IOC

spring四种依赖注入方式

#### Spring MVC

什么是MVC

Spring mvc与Struts mvc的区别

#### Spring Boot

Spring Boot 2.0、起步依赖、自动配置、

Spring Boot的starter原理，自己实现一个starter

#### Spring Security

### Spring Cloud

服务发现与注册：Eureka、Zookeeper、Consul

负载均衡：Feign、Spring Cloud Loadbalance

服务配置：Spring Cloud Config

服务限流与熔断：Hystrix

服务链路追踪：Dapper

服务网关、安全、消息

### 应用服务器知识

#### JBoss

#### tomcat

#### jetty

#### Weblogic

### 工具

#### git & svn

#### maven & gradle

#### Intellij IDEA

常用插件：Maven Helper 、FindBugs-IDEA、阿里巴巴代码规约检测、GsonFormat

Lombok plugin、.ignore、Mybatis plugin

## 四、 高级篇

### 新技术

#### Java 8

lambda表达式、Stream API、时间API

#### Java 9

Jigsaw、Jshell、Reactive Streams

#### Java 10

局部变量类型推断、G1的并行Full GC、ThreadLocal握手机制

#### Java 11

ZGC、Epsilon、增强var、

#### Spring 5

响应式编程

#### Spring Boot 2.0

### http/2

### http/3

### 性能优化

使用单例、使用Future模式、使用线程池、选择就绪、减少上下文切换、减少锁粒度、数据压缩、结果缓存

### 线上问题分析

#### dump获取

线程Dump、内存Dump、gc情况

#### dump分析

分析死锁、分析内存泄露

#### dump分析及获取工具

jstack、jstat、jmap、jhat、Arthas

#### 自己编写各种outofmemory，stackoverflow程序

HeapOutOfMemory、 Young OutOfMemory、MethodArea OutOfMemory、ConstantPool OutOfMemory、DirectMemory OutOfMemory、Stack OutOfMemory Stack OverFlow

#### Arthas

jvm相关、class/classloader相关、monitor/watch/trace相关、

options、管道、后台异步任务

文档：https://alibaba.github.io/arthas/advanced-use.html

#### 常见问题解决思路

内存溢出、线程死锁、类加载冲突

#### 使用工具尝试解决以下问题，并写下总结

当一个Java程序响应很慢时如何查找问题、

当一个Java程序频繁FullGC时如何解决问题、

如何查看垃圾回收日志、

当一个Java应用发生OutOfMemory时该如何解决、

如何判断是否出现死锁、

如何判断是否存在内存泄露

使用Arthas快速排查Spring Boot应用404/401问题

使用Arthas排查线上应用日志打满问题

利用Arthas排查Spring Boot应用NoSuchMethodError

### 编译原理知识

#### 编译与反编译

#### Java代码的编译与反编译

#### Java的反编译工具

javap 、jad 、CRF

#### 即时编译器

#### 词法分析，语法分析（LL算法，递归下降算法，LR算法），语义分析，运行时环境，中间代码，代码生成，代码优化

### 操作系统知识

#### Linux的常用命令

#### 进程间通信

#### 进程同步

生产者消费者问题、哲学家就餐问题、读者写者问题

#### 缓冲区溢出

#### 分段和分页

#### 虚拟内存与主存

#### 虚拟内存管理

#### 换页算法

### 数据库知识

#### MySql 执行引擎

#### MySQL 执行计划

如何查看执行计划，如何根据执行计划进行SQL优化

#### 索引

Hash索引、B树索引（B+树、和B树、R树）

普通索引、唯一索引

覆盖索引、最左前缀原则、索引下推

#### SQL优化

#### 数据库事务和隔离级别

事务的隔离级别、事务能不能实现锁的功能

#### 数据库锁

行锁、表锁、使用数据库锁实现乐观锁、

#### 连接

内连接，左连接，右连接

#### 数据库主备搭建

#### binlog

#### redolog

#### 内存数据库

h2

#### 分库分表

#### 读写分离

#### 常用的nosql数据库

redis、memcached

#### 分别使用数据库锁、NoSql实现分布式锁

#### 性能调优

#### 数据库连接池

### 数据结构与算法知识

#### 简单的数据结构

栈、队列、链表、数组、哈希表、

栈和队列的相同和不同之处

栈通常采用的两种存储结构

#### 树

二叉树、字典树、平衡树、排序树、B树、B+树、R树、多路树、红黑树

#### 堆

大根堆、小根堆

#### 图

有向图、无向图、拓扑

#### 排序算法

稳定的排序：冒泡排序、插入排序、鸡尾酒排序、桶排序、计数排序、归并排序、原地归并排序、二叉排序树排序、鸽巢排序、基数排序、侏儒排序、图书馆排序、块排序

不稳定的排序：选择排序、希尔排序、Clover排序算法、梳排序、堆排序、平滑排序、快速排序、内省排序、耐心排序

各种排序算法和时间复杂度

#### 深度优先和广度优先搜索

#### 全排列、贪心算法、KMP算法、hash算法

#### 海量数据处理

分治，hash映射，堆排序，双层桶划分，Bloom Filter，bitmap，数据库索引，mapreduce等。

#### 两个栈实现队列，和两个队列实现栈

### 大数据知识

#### Zookeeper

基本概念、常见用法

#### Solr，Lucene，ElasticSearch

在linux上部署solr，solrcloud，，新增、删除、查询索引、倒排索引

#### Storm，流式计算，了解Spark，S4

在linux上部署storm，用zookeeper做协调，运行storm hello world，local和remote模式运行调试storm topology。

#### Hadoop，离线计算

HDFS、MapReduce

#### 分布式日志收集flume，kafka，logstash

#### 数据挖掘，mahout

### 网络安全知识

#### XSS

XSS的防御

#### CSRF

#### 注入攻击

SQL注入、XML注入、CRLF注入

#### 文件上传漏洞

#### 加密与解密

对称加密、非对称加密、哈希算法、加盐哈希算法

MD5，SHA1、DES、AES、RSA、DSA

彩虹表

#### DDOS攻击

DOS攻击、DDOS攻击

memcached为什么可以导致DDos攻击、什么是反射型DDoS

如何通过Hash碰撞进行DOS攻击

#### SSL、TLS，HTTPS

#### 用openssl签一个证书部署到apache或nginx

## 五、架构篇

### 分布式

数据一致性、服务治理、服务降级

#### 分布式事务

2PC、3PC、CAP、BASE、 可靠消息最终一致性、最大努力通知、TCC

#### Dubbo

服务注册、服务发现，服务治理

http://dubbo.apache.org/zh-cn/

#### 分布式数据库

怎样打造一个分布式数据库、什么时候需要分布式数据库、mycat、otter、HBase

#### 分布式文件系统

mfs、fastdfs

#### 分布式缓存

缓存一致性、缓存命中率、缓存冗余

#### 限流降级

Hystrix、Sentinal

#### 算法

共识算法、Raft协议、Paxos 算法与 Raft 算法、拜占庭问题与算法

2PC、3PC

### 微服务

SOA、康威定律

#### ServiceMesh

sidecar

#### Docker & Kubernets

#### Spring Boot

#### Spring Cloud

### 高并发

#### 分库分表

#### CDN技术

#### 消息队列

ActiveMQ

### 监控

#### 监控什么

CPU、内存、磁盘I/O、网络I/O等

#### 监控手段

进程监控、语义监控、机器资源监控、数据波动

#### 监控数据采集

日志、埋点

#### Dapper

### 负载均衡

tomcat负载均衡、Nginx负载均衡

四层负载均衡、七层负载均衡

### DNS

DNS原理、DNS的设计

### CDN

数据一致性

## 六、 扩展篇

### 云计算

IaaS、SaaS、PaaS、虚拟化技术、openstack、Serverlsess

### 搜索引擎

Solr、Lucene、Nutch、Elasticsearch

### 权限管理

Shiro

### 区块链

哈希算法、Merkle树、公钥密码算法、共识算法、Raft协议、Paxos 算法与 Raft 算法、拜占庭问题与算法、消息认证码与数字签名

#### 比特币

挖矿、共识机制、闪电网络、侧链、热点问题、分叉

#### 以太坊

#### 超级账本

### 人工智能

数学基础、机器学习、人工神经网络、深度学习、应用场景。

#### 常用框架

TensorFlow、DeepLearning4J

### IoT

### 量子计算

### AR & VR

### 其他语言

Groovy、Python、Go、NodeJs、Swift、Rust

## 六、 推荐书籍

《深入理解Java虚拟机》
《Effective Java》
《深入分析Java Web技术内幕》
《大型网站技术架构》
《代码整洁之道》
《架构整洁之道》
《Head First设计模式》
《maven实战》
《区块链原理、设计与应用》
《Java并发编程实战》
《鸟哥的Linux私房菜》
《从Paxos到Zookeeper》
《架构即未来》

-------------

扫描二维码，关注Hollis，所有内容第一时间在公众号更新

![](http://www.hollischuang.com/wp-content/uploads/2018/10/%E4%BA%8C%E7%BB%B4%E7%A0%81%E7%BE%8E%E5%8C%96-1.png)
