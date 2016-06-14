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
* [hashcode/clone](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#hashCode%28%29)
* [wait/notify/notifyAll](http://tutorials.jenkov.com/java-concurrency/thread-signaling.html)

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

### Threads/Concurrency

* [insidejvm2: Thread Synchronization](http://www.artima.com/insidejvm/ed2/threadsynch.html)
* synchronized
  * [Synchronized vs Lock Performance](http://architects.dzone.com/articles/synchronized-vs-lock-0)
* volatile
  * [聊聊并发（一）——深入分析Volatile的实现原理](http://www.infoq.com/cn/articles/ftf-java-volatile)
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
* [Abstract Class Versus Interface in the JDK 8 Era](http://java.dzone.com/articles/abstract-class-versus)

### Java 9

* [jagsaw](http://openjdk.java.net/projects/jigsaw/)

## 2. JVM

