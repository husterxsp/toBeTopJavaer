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

[面向对象、面向过程](/basics/java-basic/object-oriented-vs-procedure-oriented.md)

> 面向过程：以事件为中心，按照时间发生的顺序，调用一系列函数。开发简单但是不易于维护。
>
> 面向对象：以对象为中心，把涉及到的事物抽象成对象。好处：结构化、模块化，易于维护。
> [https://zhuanlan.zhihu.com/p/28427324](https://zhuanlan.zhihu.com/p/28427324)


[面向对象的三大基本特征](/basics/java-basic/characteristics.md)和[五大基本原则](/basics/java-basic/principle.md)


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

[Java如何实现的平台无关性的](/basics/java-basic/platform-independent.md)


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

[值传递、引用传递](/basics/java-basic/java-pass-by.md)

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

[什么是多态](/basics/java-basic/polymorphism.md)、[方法重写与重载](/basics/java-basic/overloading-vs-overriding.md)

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

> https://data-flair.training/blogs/java-extends-vs-implements/

构造函数与默认构造函数

[Java的继承与组合](/basics/java-basic/inheritance-composition.md)

[构造函数与默认构造函数](/basics/java-basic/constructor.md)


[类变量、成员变量和局部变量](/basics/java-basic/variable.md)

[成员变量和方法作用域](/basics/java-basic/scope.md)

### Java基础知识

#### 基本数据类型

[7种基本数据类型：整型、浮点型、布尔型、字符型](/basics/java-basic/basic-data-types.md)

[整型中byte、short、int、long的取值范围](/basics/java-basic/integer-scope.md)

[什么是浮点型？](/basics/java-basic/float.md)

[什么是单精度和双精度？](/basics/java-basic/single-double-float.md)

[为什么不能用浮点型表示金额？](/basics/java-basic/float-amount.md)

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

[String对“+”的重载](/basics/java-basic/string-append.md)

[字符串拼接的几种方式和区别](/basics/java-basic/string-concat.md)

String.valueOf和Integer.toString的区别

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

常用集合类的使用、ArrayList和LinkedList和Vector的区别 、[SynchronizedList和Vector的区别](/basics/java-basic/synchronizedlist-vector.md)、HashMap、HashTable、ConcurrentHashMap区别、

Set和List区别？Set如何保证元素不重复？

[Java 8中stream相关用法](/basics/java-basic/stream.md)、apache集合处理工具类的使用、不同版本的JDK中HashMap的实现的区别以及原因

Collection和Collections区别

Arrays.asList获得的List使用时需要注意什么

Enumeration和Iterator区别

fail-fast 和 fail-safe

CopyOnWriteArrayList、ConcurrentSkipListMap

#### 枚举

枚举的用法、枚举的实现、枚举与单例、Enum类

Java枚举如何比较

switch对枚举的支持

[枚举的序列化如何实现](/basics/java-basic/enum-serializable.md)

枚举的线程安全性问题

#### IO

字符流、字节流、输入流、输出流、

> 知识星球IO专题
>
> 字节流逐字节地访问文件。字节流适用于任何类型的文件，但不太适合文本文件（txt文件）。例如，如果文件使用的是unicode编码，而字符用两个字节表示，则字节流将会将这个字符分开处理，因而自己还需要做转换。
>
> 字符流将逐个字符地读取文件。需要为字符流提供文件的编码才能正常工作。
>
> 字节流类继承自抽象类 InputStream 和 OutputStream。 字符流类继承自抽象类 Reader 和 Writer。
>
> 输入输出以内存为参照：输入是从外存读入内存
>
> https://github.com/husterxsp/java-learning/blob/master/daily/092-byte-and-character-stream.md



同步、异步、阻塞、非阻塞、Linux 5种IO模型

> 同步，异步，是描述被调用方的。
> 阻塞，非阻塞，是描述调用方的。主要是从CPU的消耗上来说的。阻塞就是CPU停下等待。非阻塞看起来效率高，但是会有线程切换的代价。
>
>
>
> Linux 5种IO模型
>
> - 阻塞式IO模型
> - 非阻塞IO模型
> - IO复用模型
> - 信号驱动IO模型
> - 异步IO模型

BIO、NIO和AIO的区别、三种IO的用法与原理、netty

> BIO：阻塞IO。java.io 下面的实现
>
> NIO：非阻塞IO。java.nio下的实现
>
> 关键组件 Selector、Channel、Buffer。（《深入分析Java web》）
>
> AIO：异步非阻塞。也在java.nio下面，比如 AsynchronousFileChannel。channel.read 返回的是 future对象
>
> BIO方式适用于连接数目比较小且固定的架构，这种方式对服务器资源要求比较高，并发局限于应用中，JDK1.4以前的唯一选择，但程序直观简单易理解。
>
> NIO方式适用于连接数目多且连接比较短（轻操作）的架构，比如聊天服务器，并发局限于应用中，编程比较复杂，JDK1.4开始支持。
>
> AIO方式适用于连接数目多且连接比较长（重操作）的架构，比如相册服务器，充分调用OS参与并发操作，编程比较复杂，JDK7开始支持。
>
> netty：Netty 封装了 JDK 的 NIO，不用再写一大堆复杂的代码了。（掘金小册：<https://juejin.im/book/5b4bc28bf265da0f60130116/section/5b4bc28b5188251b1f224ee5>）

#### Java反射与javassist

反射与工厂模式、 反射有什么作用

> **反射** 机制指的是程序在运行时能够获取自身的信息。在java中，只要给定类的名字，那么就可以通过反射机制来获得类的所有属性和方法。（星球直面java系列 140期）
>
> 作用：
>
> - 在运行时判断任意一个对象所属的类。
> - 在运行时判断任意一个类所具有的成员变量和方法。
> - 在运行时任意调用一个对象的方法
> - 在运行时构造任意一个类的对象
>
> 反射有哪些优缺点？
>
> 优点
>
> - 反射提高了程序的灵活性和扩展性。
>   缺点
>
> - 代码可读性低及可维护性
>
> - 反射代码执行的性能低
>
> - 破坏了封装性。
>
> - 在业务代码中应该尽量避免使用反射。但是，作为一个合格的Java开发，也要能读懂中间件、框架中的反射代码。在有些场景下，要知道可以使用反射解决部分问题。
>
> 反射与工厂模式
> <http://www.hollischuang.com/archives/1163>

Class类

`java.lang.reflect.*`

> Java的Class类是java反射机制的基础,通过Class类我们可以获得关于一个类的相关信息
>
> Java.lang.Class是一个比较特殊的类，它用于封装被装入到JVM中的类（包括类和接口）的信息。当一个类或接口被装入的JVM时便会产生一个与之关联的java.lang.Class对象，可以通过这个Class对象对被装入类的详细信息进行访问。
>
> 虚拟机为每种类型管理一个独一无二的Class对象。也就是说，每个类（型）都有一个Class对象。运行程序时，Java虚拟机(JVM)首先检查是否所要加载的类对应的Class对象是否已经加载。如果没有加载，JVM就会根据类名查找.class文件，并将其Class对象载入。（直面java 144）
>
>
>
> Class.forName(“com.test.Foo”)  加载类
>
> 再看

反射的用法？

> 动态代理
> JDBC的class.forName
> BeanUtils中属性值的拷贝
> RPC框架
> ORM框架
> Spring的IOC/DI

#### 动态代理

静态代理、动态代理

> 静态代理相当于给原来的方法再包装一层：比如可以记录日志、控制对象访问权限，增强对象功能。
>
> 比如可以实现接口，调用委托类的方法。
>
> 静态代理，需要写很多代码。然后就有了动态代理。
>
> 动态代理中的代理类并不要求在编译期就确定，而是可以在运行期动态生成，从而实现对目标对象的代理功能。
>

动态代理和反射的关系

> 反射是动态代理的一种实现方式。

动态代理的几种实现方式

> jdk动态代理和cglib动态代理
>
> <http://www.iocoder.cn/RPC/laoxu/rpc-dynamic-proxy//>
>
> [Java中的动态代理有几种实现方式，各有什么优缺点](<https://github.com/husterxsp/java-learning/blob/master/daily/150-Java%E4%B8%AD%E7%9A%84%E5%8A%A8%E6%80%81%E4%BB%A3%E7%90%86%E6%9C%89%E5%87%A0%E7%A7%8D%E5%AE%9E%E7%8E%B0%E6%96%B9%E5%BC%8F%EF%BC%8C%E5%90%84%E6%9C%89%E4%BB%80%E4%B9%88%E4%BC%98%E7%BC%BA%E7%82%B9.md>)
>
> Java Proxy 和 CGLIB 动态代理原理：<http://www.importnew.com/27772.html>
>
> FastClass：<https://www.jianshu.com/p/13aa63e1ac95>
>
> - JDK动态代理原理和静态代理类似，只不过是动态生成字节码的。
>
> java.lang.reflect 包中的Proxy类和InvocationHandler接口提供了生成动态代理类的能力。
>
> Cglib是一个第三方代码生成类库，运行时在内存中动态生成一个子类对象从而实现对目标对象功能的扩展。
>
> Cglib与JDK动态代理最大的区别就是：
>
> - 使用动态代理的对象必须实现一个或多个接口
> - 使用cglib代理的对象则无需实现接口，达到代理类无侵入。
> - cglib是通过继承来实现的代理。

问：Java 实现动态代理主要涉及哪几个类？(直面java153)

> java.lang.reflect.Proxy: 这是生成代理类的主类，通过 Proxy 类生成的代理类都继承了 Proxy 类，即 DynamicProxyClass extends Proxy。
> java.lang.reflect.InvocationHandler: 这里称他为"调用处理器"，他是一个接口，我们动态生成的代理类需要完成的具体内容需要自己定义一个类，而这个类必须实现 InvocationHandler 接口。



AOP（直面java156）

> 动态代理。
>
> Spring AOP中的动态代理主要有两种方式，JDK动态代理和CGLIB动态代理。
> JDK动态代理通过反射来接收被代理的类，并且要求被代理的类必须实现一个接口。JDK动态代理的核心是InvocationHandler接口和Proxy类。
> 如果目标类没有实现接口，那么Spring AOP会选择使用CGLIB来动态代理目标类。
> CGLIB（Code Generation Library），是一个代码生成的类库，可以在运行时动态的生成某个类的子类，注意，CGLIB是通过继承的方式做的动态代理，因此如果某个类被标记为**final**，那么它是无法使用CGLIB做动态代理的。

#### 序列化

什么是序列化与反序列化、为什么序列化、序列化底层原理、序列化与单例模式、protobuf、为什么说序列化并不安全

><http://www.hollischuang.com/archives/1150>
>
>序列化是将对象转换为可传输格式的过程。 是一种数据的持久化手段。一般广泛应用于网络传输，RMI和RPC等场景中。
>
>Serializable接口：
>
>Externalizable接口：需要重写writeExternal()与readExternal()
>
>序列化会破坏单例模式
>
>- 因为 序列化会通过反射调用无参数的构造方法创建一个新的对象。
>
><https://www.hollischuang.com/archives/1144>
>
>protobuf：一种序列化协议
>
>安全性：<https://www.secpulse.com/archives/60819.html>
>
>- 由于对象序列化是遵循标准协议的，所以可以轻易地分析出流中的信息，并且可以进行篡改
>- 解决
>  - 对数据加密
>  - 对传输加密
>  - 使用transient字段，敏感字段不序列化

#### 注解

元注解、自定义注解、Java中常用注解使用、注解与反射的结合

> 元注解：定义其他注解的注解 。元注解有四个:@Target（表示该注解可以用于什么地方）、@Retention（表示再什么级别保存该注解信息）、@Documented（将此注解包含再javadoc中）、@Inherited（允许子类继承父类中的注解）
>
> 自定义注解：除了元注解，都是自定义注解。通过元注解定义出来的注解。如我们常用的Override 、Autowire等。日常开发中也可以自定义一个注解，这些都是自定义注解。
>
> JDK内置的常用注解：
>
> 1.@Override 表示当前方法覆盖了父类的方法
> 2.@Deprecation 表示方法已经过时,方法上有横线，使用时会有警告。
> 3.@SuppressWarnings 表示关闭一些警告信息(通知java编译器忽略特定的编译警告)
>
>

Spring常用注解

> 1. @Component指的是组件，
>   @Controller，@Repository和@Service 注解都被@Component修饰，用于代码中区分表现层，持久层和业务层的组件，代码中组件不好归类时可以使用@Component来标注
> 2. 当前版本只有区分的作用，未来版本可能会添加更丰富的功能

#### JMS

什么是Java消息服务、JMS消息传送模型

#### JMX

`java.lang.management.*`、 `javax.management.*`

#### 泛型

泛型与继承、类型擦除、泛型中K T V E ？ [object等的含义](/basics/java-basic/k-t-v-e.md)、泛型各种用法

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

> SPI：调用方来制定接口，实现方来针对接口来实现不同的实现。调用方来选择自己需要的实现方。
>
> 通过线程上下文类加载器去加载所需要的SPI代码。也就是父加载器请求子类加载器去完成类加载的动作。
>
> 读取META-INF/services/下的配置文件，获得所有能被实例化的类的名称
>
> 通过反射方法Class.forName()加载类对象，并用instance()方法将类实例化



什么是JNDI？

> <https://docs.oracle.com/javase/tutorial/jndi/overview/index.html>
>
>

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

> HashMap：循环死锁问题，<https://coolshell.cn/articles/9606.html>
>
>

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

> jstack 查看线程状态：
>
> ```
> java.lang.Thread.State: WAITING (on object monitor)
> 
> Found one Java-level deadlock:
> 
> ...
> ```
>
>

#### 锁

CAS、乐观锁与悲观锁、数据库相关锁机制、分布式锁、偏向锁、轻量级锁、重量级锁、monitor、

锁优化、锁消除、锁粗化、自旋锁、可重入锁、阻塞锁、死锁

> CAS：compareAndSwap。一般是和循环一块儿使用。由底层C语言代码负责保证原子性。加锁。
>
> 这里说是给总线加锁？<https://juejin.im/post/5a73cbbff265da4e807783f5>
>
> CAS的问题：ABA问题。循环CPU消耗。解决使用版本号。
>
> ---
>
> 都是用在数据库里的。
>
> “悲观锁”，Pessimistic Concurrency Control，缩写“PCC”
>
> “乐观锁”，Optimistic Concurrency Control，缩写“OCC”
>
> <https://www.hollischuang.com/archives/934>
>
> ---
>
> 分布式锁的几种实现方式：<https://www.hollischuang.com/archives/1716>
>
> Zookeeper > 缓存 > 数据库
>
> Zookeeper分布式锁要详细了解。
>
> ---
>
> 偏向锁：对象头和栈帧的锁记录里存储偏向的线程ID，这样下次该线程进出同步块的时候不用CAS来加锁和解锁了，测试简单测试一下对象头里的标记。
>
> 轻量级锁：循环CAS设置。如果设置失败，会膨胀为重量级锁，即阻塞。？
>
> monitor：监视器。
>
> - <https://www.hollischuang.com/archives/2030>
> - <https://stackoverflow.com/questions/3362303/whats-a-monitor-in-java>
> - <https://dymanzy.github.io/2017/08/07/synchronized%E4%B8%8E%E5%AF%B9%E8%B1%A1%E7%9A%84Monitor/>
>
> monitor是一种机制，负责管理同步代码块的访问？每个对应的加锁的对象都有一个monitor对象？底层C实现的monitor对象。。。?其实底层是monitor在负责维护等待队列。
>
> ----
>
> 锁优化、粗化：<https://www.cnblogs.com/paddix/p/5405678.html>
>
> 锁粗化（Lock Coarsening）：锁粗化的概念应该比较好理解，就是将多次连接在一起的加锁、解锁操作合并为一次，将多个连续的锁扩展成一个范围更大的锁。
>
>

#### 死锁

死锁的原因

死锁的解决办法

#### synchronized

[synchronized是如何实现的？](/basics/java-basic/synchronized.md)

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

Client 和 Server 模式？

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

> 标记清除：效率不高，空间碎片
>
> 复制：效率高了，不会有空间碎片，但是代价大，只能用一半的内存空间。
>
> - 目前新生代是用这种复制算法，不过不是1：1，而是分为Edgn，Survivor，8：1：1
> - 当Survivor空间不够用时，由老年代做担保
>
> 标记-整理：一半用于老年代，存活对象较多。与标记清除类似，只是清除完之后，所有的对象往一端移动。然后直接清理掉边界外的空间。
>
> 分代回收：分为新生代和老年代

GCRoots有哪些？

> 所谓“GC roots”，或者说tracing GC的“根集合”，就是**一组必须活跃的引用**。
>
> java的gc为什么要分代？ - RednaxelaFX的回答 - 知乎
> https://www.zhihu.com/question/53613423/answer/135743258



GC参数、对象存活的判定、垃圾收集器（CMS、G1、ZGC、Epsilon）

> CMS：并发标记整理
>
> G1：Garbage-First（G1）从整体来看基于标记-整理，但是从局部来看（两个region之间），还是基于复制。有非常好的空间整理能力，不会产生空间碎片。
>
> （具体还是以实测为准，基准测试?）
>
> - G1虽然也还有新生代和老生代的概念，但不是物理的隔离了。

什么情况下会发生full GC?

> 标记清除算法产生较多空间碎片，需要分配一个连续较大空间时会容易发生FGC

Major GC和Full GC的区别是什么？触发条件呢？ - RednaxelaFX的回答 - 知乎
https://www.zhihu.com/question/41922036/answer/93079526

#### JVM参数及调优

-Xmx、-Xmn、-Xms、Xss、-XX:SurvivorRatio、

-XX:PermSize、-XX:MaxPermSize、-XX:MaxTenuringThreshold

> -Xmx：最大堆容量，mx表示 memory max
>
> -Xms：最小堆容量，ms表示 memory start
>
> -Xmn：年轻代大小
>
> -Xss：线程栈容量
>
> -XX:SurvivorRatio：年轻代中 Eden区与Survivor区的大小比值
>
> -XX:MaxTenuringThreshold：垃圾最大年龄。如果设置为0的话,则年轻代对象不经过Survivor区,直接进入年老代. 对于年老代比较多的应用,可以提高效率。

<https://www.cnblogs.com/redcreen/archive/2011/05/04/2037057.html>

#### Java对象模型

oop-klass、对象头

#### HotSpot

即时编译器、编译优化

#### 虚拟机性能监控与故障处理工具

jps, jstack, jmap、jstat, jconsole, jinfo, jhat, javap, btrace、TProfiler

Arthas

### 类加载机制

classLoader、类加载过程、双亲委派（破坏双亲委派）、模块化（jboss modules、osgi、jigsaw）

> 深度分析Java的ClassLoader机制：<https://www.hollischuang.com/archives/199>
>
> ```java
> public abstract class ClassLoader {
> }
> ```
>
> 三个类加载器
>
> **根装载器**
>
> `ExtClassLoader`(**扩展类装载器**)
>
> `AppClassLoader`，其中根装载器不是ClassLoader的子类，由C++编写，因此在java中看不到
>
> “**委托机制**”是指先委托父类装载器寻找目标类，只有在找不到的情况下才从自己的类路径中查找并装载目标类。
>
> 所以即便用户写了一个String类，也是加载不进去的。
>
> ---
>
> 破坏双亲委派：
>
> - <https://blog.csdn.net/u012129558/article/details/81540804>
> - <https://blog.csdn.net/u014590757/article/details/80190998>

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

> 享元模式：底层的数据共享
>
>

#### 会使用常用设计模式

单例的七种写法：懒汉——线程不安全、懒汉——线程安全、饿汉、饿汉——变种、静态内部类、枚举、双重校验锁

> - <https://www.jianshu.com/p/61b67ca754a3>
> - <https://github.com/youlookwhat/DesignPattern/blob/master/app/src/main/java/com/example/jingbin/designpattern/singleton/ehan/SingletonEHan.java>
> - <https://github.com/youlookwhat/DesignPattern/blob/master/app/src/main/java/com/example/jingbin/designpattern/singleton/lanhan/SingletonLanHan.java>
>
>

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

> Servlet的生命周期有四个阶段：加载并实例化、初始化、请求处理、销毁。
>
> <https://blog.csdn.net/qq_24145735/article/details/52433096>

线程安全问题

> Servlet不是线程安全的。
>
> 当Tomcat接收到Client的HTTP请求时，Tomcat从线程池中取出一个线程，之后找到该请求对应的Servlet对象并进行初始化，之后调用service()方法。要注意的是每一个Servlet对象再Tomcat容器中只有一个实例对象，即是单例模式。如果多个HTTP请求请求的是同一个Servlet，那么着两个HTTP请求对应的线程将并发调用Servlet的service()方法。
>
> <https://www.cnblogs.com/chanshuyi/p/5052426.html>

filter和listener

> 

web.xml中常用配置及作用

[servlet-demo>](<https://github.com/husterxsp/servlet-demo>)

#### Hibernate

什么是OR Mapping

Hibernate的缓存机制

Hibernate的懒加载

Hibernate/Ibatis/MyBatis之间的区别

#### Spring

> Bean 的四种作用域：单例、原型、会话、请求
>
> 单例的线程安全问题：<https://www.jianshu.com/p/d21b65f7a6b8>

Bean的初始化

> 

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

<https://juejin.im/post/5be13b83f265da6116393fc7>

服务发现与注册：Eureka、Zookeeper、Consul

>

负载均衡：Feign、Spring Cloud Loadbalance

> Feign是封装Restful 请求的，底层用的ribbon才是负载均衡。
>
> - 对某个接口定义了@FeignClient注解，Feign就会针对这个接口创建一个**动态代理**

服务配置：Spring Cloud Config

>

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

HeapOutOfMemory、 Young OutOfMemory、MethodArea OutOfMemory、ConstantPool OutOfMemory、DirectMemory OutOfMemory、Stack OutOfMemory、 Stack OverFlow

> [outofmemory.md](./answer/outofmemory.md)



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

> https://github.com/alibaba/arthas/issues/429
>
>

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



OLTP和OLAP：

> OLTP：事务处理on-line transaction processing。我们一般用的都是OLTP
>
> OLAP：联机分析处理On-Line Analytical Processing。比如Hive

#### SQL优化

#### 数据库事务和隔离级别

事务的隔离级别、事务能不能实现锁的功能

> 事务隔离级别：
>
> - 可串行化
> - 可重复读
> - 读已提交
> - 读未提交
>
> <http://www.cnblogs.com/zhoujinyi/p/3437475.html>

ACID是什么意思？

> 原子性
>
> 一致性
>
> 隔离性
>
> 持久性

#### 数据库锁

行锁、表锁、使用数据库锁实现乐观锁、

> 行锁：共享锁、排它锁
>
> 表锁：意向锁，意向共享锁、意向排它锁。

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

> R树是B树在高维空间的扩展，是一棵平衡树。
>
> https://blog.csdn.net/v_JULY_v/article/details/6530142
>
> 多路查找树(muitl-way search tree)，其每一个节点的孩子数可以多于两个，且每一个节点处可以存储多个元素

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

> CAP（维基百科）
>
> - 一致性（**C**onsistency） （等同于所有节点访问同一份最新的数据副本）
> - [可用性](https://zh.wikipedia.org/wiki/%E5%8F%AF%E7%94%A8%E6%80%A7)（**A**vailability）（每次请求都能获取到非错的响应——但是不保证获取的数据为最新数据）
> - [分区容错性](https://zh.wikipedia.org/w/index.php?title=%E7%BD%91%E7%BB%9C%E5%88%86%E5%8C%BA&action=edit&redlink=1)（**P**artition tolerance）（以实际效果而言，分区相当于对通信的时限要求。系统如果不能在时限内达成数据一致性，就意味着发生了分区的情况，必须就当前操作在C和A之间做出选择[[3\]](https://zh.wikipedia.org/wiki/CAP%E5%AE%9A%E7%90%86#cite_note-3)。）。。。。。。就是容忍网络分区。那么容忍网络分区，就要在C和A之间选一个。
>
> TCC：

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

> Paxos算法：

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

扫描二维码，关注作者微信

![](http://www.hollischuang.com/wp-content/uploads/2018/10/%E4%BA%8C%E7%BB%B4%E7%A0%81%E7%BE%8E%E5%8C%96-1.png)
