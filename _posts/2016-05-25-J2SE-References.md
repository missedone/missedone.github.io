---
layout: post
title: Java Core References
categories: [language]
tags: [java, j2se]
description: the collection of Java Core relate articles.
---

## 1. Language

### Object

* [Object clone](http://java-questions.com/Cloning-interview-questions.html)
  * shallow clone
    * Object.clone/Cloneable - Bloch: Item 10: Override Clone Judiciously
    * [commons-beanutils BeanUtils](http://commons.apache.org/proper/commons-beanutils/javadocs/v1.8.3/apidocs/index.html)
    * [Spring BeanUtils](http://static.springsource.org/spring/docs/2.5.x/api/org/springframework/beans/BeanUtils.html)
  * deep clone
    * ObjectOutputStream/ObjectInputStream
    * [commons-lang SerializationUtils](http://commons.apache.org/proper/commons-lang/javadocs/api-release/org/apache/commons/lang3/SerializationUtils.html)
    * [Java Deep Cloning Library](http://stackoverflow.com/questions/2156120/java-recommended-solution-for-deep-cloning-copying-an-instance)
* [hashcode/equals](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#hashCode%28%29)
* [wait/notify/notifyAll](http://tutorials.jenkov.com/java-concurrency/thread-signaling.html)
  * [Wait() and notify() methods in java - Definition, 8 key features, solving consumer producer problem with & without these methods and consequences of not using wait() and notify() methods.](http://www.javamadesoeasy.com/2015/03/wait-and-notify-methods-definition-8.html)

### Class

* [Inner/Nested Class](http://viralpatel.net/blogs/inner-classes-in-java/)
  * Inner Class
    * Local Inner Class
    * Anonymous Inner Class
  * Static Inner Class

### Classloading

* [diagram: Classloaders](http://www2.sys-con.com/itsg/virtualcd/java/archives/0808/chaudhri/fig1.jpg)
  * Bootstrap classloader
  * Extensions Classloader
  * System classloader
  * User-defined classloader
* [insidejvm2: The Class Loader Subsystem](http://www.artima.com/insidejvm/ed2/jvm4.html)
  ![image](http://www.artima.com/insidejvm/ed2/images/fig7-1.gif)
  1. Loading: finding and importing the binary data for a type
  2. Linking
    * Verification: ensuring the correctness of the imported type
    * Preparation: allocating memory for class variables and initializing the memory to default values
    * Resolution: transforming symbolic references from the type into direct references.
  3. Initialization: invoking Java code that initializes class variables to their proper starting values.
* [insidejvm2: The Lifetime of a Type](http://www.artima.com/insidejvm/ed2/lifetype.html)
  * Loading, Linking, Initialization
  * [The Lifetime of an Object](http://www.artima.com/insidejvm/ed2/lifetype5.html)
  * [Unloading of Types](http://www.artima.com/insidejvm/ed2/lifetype6.html)

### Collections

### Generic

### String

* [Oracle Tunes Java's Internal String Representation](http://www.infoq.com/news/2013/12/Oracle-Tunes-Java-String)

### Reflection

* [Java Reflection: Private Fields and Methods](http://tutorials.jenkov.com/java-reflection/private-fields-and-methods.html)
* Dynamic Proxy
  * [Java深度历险（七）——Java反射与动态代理](http://www.infoq.com/cn/articles/cf-java-reflection-dynamic-proxy)
  * [Java 动态代理机制分析及扩展，第 1 部分](http://www.ibm.com/developerworks/cn/java/j-lo-proxy1/index.html)
  * [Java 动态代理机制分析及扩展，第 2 部分](http://www.ibm.com/developerworks/cn/java/j-lo-proxy2/index.html)
  * [Spring AOP: Dynamic Proxies vs. CGLib proxies](http://insufficientinformation.blogspot.com/2007/12/spring-dynamic-proxies-vs-cglib-proxies.html)

### [Threads](https://dzone.com/articles/threads-top-80-interview)/Concurrency

* [Threads implement their own stack - demonstration using program and diagram](http://www.javamadesoeasy.com/2015/03/threads-implement-their-own-stack.html)
  ![image](https://lh6.googleusercontent.com/_svC5M0EsqxhAF4s3scoPSyh7ssKqA0SQH3ipHeksBMAll_d72w_abuyQ766i8edOFkWU6PQm5x9OZ1Xc3qT_wMsoy6YFpQSO9VnUWYfJgEDLR8dklnt_ndlFd7_hXQa8xEkfe0)
* [Thread states/ Thread life cycle in java](http://www.javamadesoeasy.com/2015/03/thread-states-thread-life-cycle-in-java.html)
  ![image](https://lh4.googleusercontent.com/oR0_liUxjMnfgFS-fSuc0x2vCCPLQ0Vdw6w2rBVGloaE_84tRNprqNJEJiyI1unMY8Vpj2CDK9GiQGy03_RmteRz-aM31iIQcZsVZhIH2cLrne_5nY9miXKDmQqEHdY60_WopC0)
* [Lock Contention](https://www.javacodegeeks.com/2014/11/multithreading-concurrency-interview-questions-answers.html)
  > Lock contention occurs, when two or more threads are competing in the acquisition of a lock. The scheduler has to decide whether it lets the thread, which has to wait sleeping and performs a context switch to let another thread occupy the CPU, or if letting the waiting thread busy-waiting is more efficient. Both ways introduce idle time to the inferior thread.
  In some cases lock contention can be reduced by applying one of the following techniques:
    * The scope of the lock is reduced.
    * The number of times a certain lock is acquired is reduced (lock splitting).
    * Using hardware supported optimistic locking operations instead of synchronization.
    * Avoid synchronization where possible.
    * Avoid object pooling.
* [insidejvm2: Thread Synchronization](http://www.artima.com/insidejvm/ed2/threadsynch.html)
* synchronized
  * [Synchronized vs Lock Performance](http://architects.dzone.com/articles/synchronized-vs-lock-0)
* volatile
  * [聊聊并发（一）——深入分析Volatile的实现原理](http://www.infoq.com/cn/articles/ftf-java-volatile)
  * [Volatile keyword in java- difference between synchronized and volatile, 10 key points about volatile keyword, why volatile variables are not cached in memory](http://www.javamadesoeasy.com/2015/03/volatile-keyword-in-java-difference.html)
* [Coordinating threads with CountDownLatch](http://www.javamex.com/tutorials/threads/CountDownLatch.shtml)
* [CyclicBarrier: concordinating the stages of a multithreaded operation](http://www.javamex.com/tutorials/threads/CyclicBarrier.shtml)
* Collections
  * ConcurrentHashMap
    * [聊聊并发（四）——深入分析ConcurrentHashMap](http://www.infoq.com/cn/articles/ConcurrentHashMap)
    * [Java并发编程之ConcurrentHashMap](http://www.goldendoc.org/2011/06/juc_concurrenthashmap/)
    * [探索 ConcurrentHashMap 高并发性的实现机制](http://www.ibm.com/developerworks/cn/java/java-lo-concurrenthashmap/index.html)
* Fork/Join
  * [An Introduction to the Fork / Join Framework](http://java.dzone.com/articles/javas-fork-join-framework)
  * [A walkthrough for the fork/join framework introduced in Java SE 7](http://kalali.me/a-walk-through-the-forkjoin-api-introduced-in-java-se-7/)
  * [应用 fork-join 框架，第 1 部分: 学习如何使用 Java 7 中的 fork-join 框架实现细粒度并行性](http://www.ibm.com/developerworks/cn/java/j-jtp11137.html)
  * [应用 fork-join 框架，第 2 部分: 用 Java 7 中的 ParallelArray 类加速排序和搜索](http://www.ibm.com/developerworks/cn/java/j-jtp03048.html)
  * [JDK 7 中的 Fork/Join 模式](http://www.ibm.com/developerworks/cn/java/j-lo-forkjoin/index.html)
  * [Java Fork/Join Example](http://www.javacreed.com/java-fork-join-example/)

### try-catch-finally

* [finally explained - common questions, uses, etc.](http://geekexplains.blogspot.com/2008/06/finally-explained-common-questions-uses.html)
* [Playing with try-catch-finally in Java. Intersting scenarios](http://geekexplains.blogspot.com/2008/11/playing-with-try-catch-finally-in-java.html)
* [finally contd.: an interesting try-catch-finally scenario](http://geekexplains.blogspot.com/2009/01/finally-contd-interesting-try-catch.html)

### Security

* KeyStore
  * [Common Java Keytool commands](http://nl.globalsign.com/en/support/ssl+certificates/java/java+based+webserver/keytool+commands/)
* https
  * [The First Few Milliseconds of an HTTPS Connection](http://www.infoq.com/articles/HTTPS-Connection-Jeff-Moser)

### Java 7

* NIO2
  * [Introducing NIO.2 (JSR 203) Part 1: What are new features?](http://kalali.me/introducing-nio-2-jsr-203-part-1-what-are-new-features/)
  * [Introducing NIO.2 (JSR 203) Part 2: The Basics](http://kalali.me/introducing-nio-2-jsr-203-part-2-the-basics/)
  * [Introducing NIO.2 (JSR 203) Part 3: File System Attributes and Permissions support in NIO.2](http://kalali.me/introducing-nio-2-jsr-203-part-3-file-system-attributes-and-permissions-support-in-nio-2/)
  * [Introducing NIO.2 (JSR 203) Part 4: Changing File System Attributes and Permissions](http://kalali.me/introducing-nio-2-jsr-203-part-4-changing-file-system-attributes-and-permissions/)
  * [Introducing NIO.2 (JSR 203) Part 5: Watch Service and Change Notification](http://kalali.me/introducing-nio-2-jsr-203-part-5-watch-service-and-change-notification/)
  * [Introducing NIO.2 (JSR 203) Part 6: Filtering directory content and walking over a file tree](http://kalali.me/introducing-nio-2-jsr-203-part-6-filtering-directory-content-and-walking-over-a-file-tree/)
  * [An NIO.2 primer, Part 1: The asynchronous channel APIs](http://www.ibm.com/developerworks/java/library/j-nio2-1/?ca=drs-)
  * [An NIO.2 primer, Part 2: The file system APIs](http://www.ibm.com/developerworks/java/library/j-nio2-2/?ca=drs-)
  * [Java 7: NIO.2 I/O operations on asynchronous channels are not atomic](Java 7: NIO.2 I/O operations on asynchronous channels are not atomic)
  * [Java 7: Closing NIO.2 file channels without loosing data](http://niklasschlimm.blogspot.com/2012/05/java-7-9-nio2-file-channels-on-test.html)

### Java 8

* Lambda
  * [Lambda Expressions](http://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html)
  * [State of the Lambda](http://cr.openjdk.java.net/~briangoetz/lambda/lambda-state-final.html)
  * [State of the Lambda: Libraries Edition](http://cr.openjdk.java.net/~briangoetz/lambda/lambda-libraries-final.html)
* Multitenant JVM
  * [Introduction to Java multitenancy](http://www.ibm.com/developerworks/java/library/j-multitenant-java/index.html)
* Static and Default Methods on interfaces.
  * [Default Methods](http://docs.oracle.com/javase/tutorial/java/IandI/defaultmethods.html)
  * [Abstract Class Versus Interface in the JDK 8 Era](http://java.dzone.com/articles/abstract-class-versus)
  * [Why does Java 8 not allow non-public default methods?](http://stackoverflow.com/a/27369217/4867232)

### Java 9

* [jagsaw](http://openjdk.java.net/projects/jigsaw/)
* [Java 9, OSGi and the Future of Modularity](https://www.infoq.com/articles/java9-osgi-future-modularity)

## 2. JVM

### GC

* [insidejvm2: Garbage Collection](http://www.artima.com/insidejvm/ed2/gc.html)
  * Reference Counting Collectors
  * Tracing Collectors
  * Compacting Collectors
  * Copying Collectors
  * Generational Collectors
  * Adaptive Collectors
* [GC Algorithms: Implementations](https://plumbr.eu/handbook/garbage-collection-algorithms-implementations)
  * The Serial GC
  * The Parallel GC: Throughput Matters
  * Concurrent Mark-Swap (CMS) GC: Latency Matters
    * [Java VM Options You Should Always Use in Production](http://blog.sokolenko.me/2014/11/javavm-options-production.html)
  * Garbage First (G1) GC
    * [解析JDK 7的Garbage-First收集器](http://www.infoq.com/cn/articles/jdk7-garbage-first-collector)
    * [Presentation: Deep Dive into G1 Garbage Collector](http://www.infoq.com/presentations/java-g1)
    * [G1: One Garbage Collector To Rule Them All](http://www.infoq.com/articles/G1-One-Garbage-Collector-To-Rule-Them-All)
* Generational GC
  * [Java theory and practice: Garbage collection in the HotSpot JVM: Generational and concurrent garbage collection](http://www.ibm.com/developerworks/library/j-jtp11253/)
  * [Useful JVM Flags – Part 5 (Young Generation Garbage Collection)](https://blog.codecentric.de/en/2012/08/useful-jvm-flags-part-5-young-generation-garbage-collection/)
  * [Java Platform, Standard Edition HotSpot Virtual Machine Garbage Collection Tuning Guide: Sizing the Generations](https://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/sizing.html)
* [Java深度历险（四）——Java垃圾回收机制与引用类型](http://www.infoq.com/cn/articles/cf-java-garbage-references)
* [Garbage Collection in the Java HotSpot Virtual Machine](http://www.devx.com/Java/Article/21977)
* [Minor GC vs Major GC vs Full GC](https://plumbr.eu/blog/garbage-collection/minor-gc-vs-major-gc-vs-full-gc)
* [Java technology, IBM style: Garbage collection policies, Part 1: Differing policies provide flexibility](http://www.ibm.com/developerworks/library/j-ibmjava2/)
* [InfoQ: Java Garbage Collection Distilled](http://www.infoq.com/articles/Java_Garbage_Collection_Distilled)
* [Understanding Java Garbage Collection](http://www.cubrid.org/blog/dev-platform/understanding-java-garbage-collection/)
* Tuning
  * JDK Official [Docs](http://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/sizing.html#sizing_generations) [Sizing the Generations](https://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/sizing.html)
    * [Adjusting Generation Sizes](http://www.oracle.com/technetwork/java/gc-tuning-5-138395.html#0.0.0.0.Adjusting%20Generation%20Sizes%7Coutline)
    * [More On The Incredible Shrinking JVM Heap](https://stopcoding.wordpress.com/2010/04/12/more-on-the-incredible-shrinking-jvm-heap/)
    * [What's the basis for Ergonomics setting the value of MaxNewSize](http://stackoverflow.com/q/22455562)
  * [Garbage Collection Optimization for High-Throughput and Low-Latency Java Applications](https://engineering.linkedin.com/garbage-collection/garbage-collection-optimization-high-throughput-and-low-latency-java-applications)
  * [Tuning Garbage Collection for Mission-Critical Java Applications](http://blog.mgm-tp.com/2013/03/garbage-collection-tuning/)
  * [Tuning Java Garbage Collection for Web Services](https://engineering.linkedin.com/26/tuning-java-garbage-collection-web-services)
  * [UseAdaptiveSizePolicy与CMS垃圾回收同时使用导致的JVM报错](http://www.cnblogs.com/moonandstar08/p/5751175.html)

### VM memory
	
* [jvmspec: Runtime Data Areas](http://docs.oracle.com/javase/specs/jvms/se7/html/jvms-2.html#jvms-2.5)
  * The pc Register
  * Java Virtual Machine Stacks
    * [insidejvm2: The Java Stack](http://www.artima.com/insidejvm/ed2/jvm8.html)
    * [insidejvm2: The Stack Frame](http://www.artima.com/insidejvm/ed2/jvm8.html)
  * Heap
    * [insidejvm2: The Heap](http://www.artima.com/insidejvm/ed2/jvm6.html)
  * Method Area
  * Runtime Constant Pool
  * Native Method Stacks
    * [insidejvm2: Native Method Stacks](http://www.artima.com/insidejvm/ed2/jvm9.html)
* [jvmspec: Frames](http://docs.oracle.com/javase/specs/jvms/se7/html/jvms-2.html#jvms-2.6)
  * Local Variables
  * Operand Stacks
  * Dynamic Linking
  * Normal Method Invocation Completion
  * Abrupt Method Invocation Completion
* [insidejvm2: The Lifetime of a Type](http://www.artima.com/insidejvm/ed2/lifetype.html)
* [insidejvm2: The Linking Model](http://www.artima.com/insidejvm/ed2/linkmod.html)
* [Understand Stack and Heap](http://www.itcsolutions.eu/2011/02/06/tutorial-java-8-understand-stack-and-heap/)
  * ![diagram: CallStack.gif](http://www.itcsolutions.eu/wp-content/uploads/2011/02/CallStack.gif)
  * ![diagram: StackHeapValues.png](http://www.itcsolutions.eu/wp-content/uploads/2011/02/StackHeapValues.png)
* [video: how memory is allocated in stack & heap](http://www.youtube.com/watch?feature=player_embedded&v=VQ4eZw6eVtQ)
* [From Java code to Java heap: Understanding and optimizing your application's memory usage](http://www.ibm.com/developerworks/java/library/j-codetoheap/index.html)
* [5 Tips for Proper Java Heap Size](http://architects.dzone.com/articles/5-tips-proper-java-heap-size)
* PermGen
  * [Java 7 features – PermGen removal](http://javaeesupportpatterns.blogspot.com/2011/10/java-7-features-permgen-removal.html)
    * [Java 7 Questions & Answers](http://javaeesupportpatterns.blogspot.com/2011/10/java-7-features-permgen-removal.html)
    * [Java Heap space - HotSpot VM](http://javaeesupportpatterns.blogspot.com/2011/08/java-heap-space-hotspot-vm.html)
  * [Java 8: From PermGen to Metaspace](http://java.dzone.com/articles/java-8-permgen-metaspace)

# 2. Performance Tuning Tips

## Identify thread cunsuming CPU

* [Figure out why is JAVA eating CPU?](http://javadrama.blogspot.com/2012/02/why-is-java-eating-my-cpu.html)
* [Identify Java code consuming high CPU in Linux (linking JVM thread and Linux PID)](https://blogs.manageengine.com/application-performance-2/appmanager/2011/02/09/identify-java-code-consuming-high-cpu-in-linux-linking-jvm-thread-and-linux-pid.html)
* [Which Java thread consumes my CPU?](http://www.nurkiewicz.com/2012/08/which-java-thread-consumes-my-cpu.html)
