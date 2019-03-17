#### 自己编写各种outofmemory，stackoverflow程序

HeapOutOfMemory、 Young OutOfMemory、MethodArea OutOfMemory、ConstantPool OutOfMemory、DirectMemory OutOfMemory、Stack OutOfMemory、 Stack OverFlow



JDK1.7及以前，常量池属于方法区，方法区是虚拟机中的永久代，所以测试的时候主要看 

```shell
java.lang.OutOfMemoryError: PermGen space
```

但是JDK1.8已经去除PermGen，改用MetaspaceSize，这里就不再测试了。

```java
/**
 * VM Args：-XX:PermSize=1M -XX:MaxPermSize=1M
 * VM Args：-XX:MetaspaceSize=1M -XX:MaxMetaspaceSize=1M
 */
```



###  HeapOutOfMemory

```java
/**
 * VM Args：-Xms20m -Xmx20m -XX:+HeapDumpOnOutOfMemoryError
 * 参考《深入理解java虚拟机 2.4小节》
 */
public class Test {
    static class OOMObject {
    }

    public static void main(String[] args) {
        List<OOMObject> list = new ArrayList<OOMObject>();
        while (true) {
            list.add(new OOMObject());
        }
    }
}
```

运行结果

```shell
java.lang.OutOfMemoryError: Java heap space
Dumping heap to java_pid62892.hprof ...
Heap dump file created [27813826 bytes in 0.223 secs]
Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
	at java.util.Arrays.copyOf(Arrays.java:3210)
	at java.util.Arrays.copyOf(Arrays.java:3181)
	at java.util.ArrayList.grow(ArrayList.java:261)
	at java.util.ArrayList.ensureExplicitCapacity(ArrayList.java:235)
	at java.util.ArrayList.ensureCapacityInternal(ArrayList.java:227)
	at java.util.ArrayList.add(ArrayList.java:458)
	at Test.main(Test.java:16)
```

`-XX:+HeapDumpOnOutOfMemoryError` 可以让虚拟机出现内存溢出异常时Dump当前内存转储快照。

用`jhat`工具分析

```shell
jhat java_pid62892.hprof
```

访问 <http://127.0.0.1:7000/showInstanceCounts/includePlatform/>

可以看到 `class Test$OOMObject ` 对象的实例个数非常多。



### Young OutOfMemory



###  Stack OverFlow

线程请求的栈深度大于虚拟机栈所允许的最大深度

```java
/**
 * VM Args：-Xss160k
 */
public class JavaVMStackSOF {

    private int stackLength = 1;

    public void stackLeak() {
        stackLength++;
        stackLeak();
    }

    public static void main(String[] args) throws Throwable {
        JavaVMStackSOF oom = new JavaVMStackSOF();
        try {
            oom.stackLeak();
        } catch (Throwable e) {
            System.out.println("stack length:" + oom.stackLength);
            throw e;
        }
    }
}
```

运行结果

```shell
stack length:771
Exception in thread "main" java.lang.StackOverflowError
	at JavaVMStackSOF.stackLeak(JavaVMStackSOF.java:12)
```



### Stack OutOfMemory

参照《深入理解java虚拟机》

不管是栈帧太大还是虚拟机栈容量太小，最后都是`StackOverflowError` 的错误。



### Metaspace

```java
/**
 * VM Args：-XX:PermSize=1M -XX:MaxPermSize=1M
 * VM Args：-XX:MetaspaceSize=1M -XX:MaxMetaspaceSize=1M
 */
public class JavaMethodAreaOOM {

    public static void main(String[] args) {
        while (true) {
            Enhancer enhancer = new Enhancer();
            enhancer.setSuperclass(OOMObject.class);
            enhancer.setUseCache(false);
            enhancer.setCallback(new MethodInterceptor() {
                @Override
                public Object intercept(Object obj, Method method, Object[] args, MethodProxy proxy) throws Throwable {
                    return proxy.invokeSuper(obj, args);
                }
            });
            enhancer.create();
        }
    }

    static class OOMObject {

    }
}
```

运行结果

```shell
Exception in thread "main" java.lang.OutOfMemoryError: Metaspace
	at net.sf.cglib.core.AbstractClassGenerator.generate(AbstractClassGenerator.java:345)
	at net.sf.cglib.proxy.Enhancer.generate(Enhancer.java:492)
	at net.sf.cglib.core.AbstractClassGenerator$ClassLoaderData.get(AbstractClassGenerator.java:114)
	at net.sf.cglib.core.AbstractClassGenerator.create(AbstractClassGenerator.java:291)
	at net.sf.cglib.proxy.Enhancer.createHelper(Enhancer.java:480)
	at net.sf.cglib.proxy.Enhancer.create(Enhancer.java:305)
	at JavaMethodAreaOOM.main(JavaMethodAreaOOM.java:26)
```



### DirectMemory

```java
/**
 * VM Args：-Xmx20M -XX:MaxDirectMemorySize=10M
 */
private static final int _1MB = 1024 * 1024;

public static void main(String[] args) throws Exception {
    List<ByteBuffer> list = new ArrayList<ByteBuffer>();
    while (true) {
        list.add(ByteBuffer.allocateDirect(_1MB));
    }
}
```

运行结果

```shell
Exception in thread "main" java.lang.OutOfMemoryError: Direct buffer memory
	at java.nio.Bits.reserveMemory(Bits.java:693)
	at java.nio.DirectByteBuffer.<init>(DirectByteBuffer.java:123)
	at java.nio.ByteBuffer.allocateDirect(ByteBuffer.java:311)
	at io.Read.main(Read.java:16)
```



按照《深入理解java虚拟机》，上述代码虽然报内存溢出异常，但是是计算得知的，实际并没有向操作系统申请内存。但是书中的示例代码 2-9，跑起来不抛出异常。。。

### 参考

- <https://www.cnblogs.com/duanxz/p/4901437.html>