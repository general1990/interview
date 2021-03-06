<h1>中高级java面试题整理<h1>

 # 一 前端
 
* 简述一下HTTP请求的在客户端和服务端的请求过程
 
 	 解答: [一次完整的HTTP请求过程](https://www.cnblogs.com/engeng/articles/5959335.html)
	 
* get和post的基本区别？说说 tcp/ip协议、三次握手、窗口滑动机制


	 解答: [总结get和post区别](https://www.cnblogs.com/longm/p/7205318.html?utm_source=itdadao&utm_medium=referral)
	 
	 解答: [认识tcp/ip协议中的http协议](https://blog.csdn.net/xc1158840657/article/details/77942832)
	 
	 解答: [滑动窗口机制](https://blog.csdn.net/yujun00/article/details/636495)
	 

* 说说http,https协议；

	 解答: [http协议与https协议](https://blog.csdn.net/hla199106/article/details/46987401)

* osi五层网络协议；

	 解答: [五层网络协议，各层功能，各层协议](https://blog.csdn.net/qq_22238021/article/details/80279001)

* tcp，udp区别；

	 解答: [TCP和UDP的最完整的区别](https://blog.csdn.net/li_ning_/article/details/52117463)


 # 二 java知识点
 
 ## java基础

 * 开发中Java用了比较多的数据结构有哪些
 
	 解答: [java 中几种常用数据结构](https://blog.csdn.net/qq_31615049/article/details/80545713)

 * Java 中的排序工具有哪些；有什么区别？
 	* Collections.sort算法调用的是合并排序。
	* Arrays.sort() 采用了2种排序算法 -- 基本类型数据使用快速排序法，对象数组使用归并排序。
	
	[《Arrays.sort和Collections.sort实现原理解析》](https://www.cnblogs.com/zhanht/p/5450325.html)
	
 * String,StringBuffer和StringBuilder的区别；
 
	 解答: [String，StringBuilder，StringBuffer三者的区别](https://www.cnblogs.com/su-feng/p/6659064.html)
 	

* Object的方法有哪些：比如有wait方法，为什么会有；

 	 解答: [Object有哪些基本的方法](http://www.cnblogs.com/Java3y/p/8985368.html)


* wait和sleep的区别，必须理解！！！

 	解答: [sleep和wait的区别](https://www.cnblogs.com/plmnko/archive/2010/10/15/1851854.html)


* 强引用，软引用和弱引用的区别；

	解答: [Java四种引用](https://www.cnblogs.com/yw-ah/p/5830458.html)

* java的多态表现在哪里；
 	* 接口=实现类
	* Parent=Child； 
	
	[《java中的多态表现》](https://blog.csdn.net/bauterujj/article/details/73091113)

* 接口有什么用；

	解答: [Java 中的接口有什么作用](https://www.zhihu.com/question/20111251/answer/14012223)
	

* ThreadLocal可以用来共享数据吗；
	* ThreadLocal设计的目的就是为了能够在当前线程中有属于自己的变量，并不是为了解决并发或者共享变量的问题
	
	解答: [ThreadLocal就是这么简单](https://mp.weixin.qq.com/s?__biz=MzI4Njg5MDA5NA==&mid=2247484118&idx=1&sn=da3e4c4cfd0642687c5d7bcef543fe5b&chksm=ebd743d7dca0cac19a82c7b29b5b22c4b902e9e53bd785d066b625b4272af2a6598a0cc0f38e#rd)

* Exception和Error有什么区别

	解答: [Error与Exception的区别](https://blog.csdn.net/min996358312/article/details/65729617)

* 谈谈final,finally,finalize有什么不同

	解答: [final、finally、finalize 的区别](https://blog.csdn.net/qwdafedv/article/details/47164577)

* Java有集中文件拷贝方式？哪一种最高效
	解答: [java有几种文件拷贝方式？哪一种最高效？](https://blog.csdn.net/qweqwruio/article/details/81359618)

* AtomicInteger底层实现原理是什么？如何在自己的产品代码中应用CAS操作

	解答: [AtomicInteger源码分析——基于CAS的乐观锁实现](https://blog.csdn.net/qfycc92/article/details/46489553)

 ## java集合

 * collection的理解，选择一种说下底层实现

 * 集合类：List和Set比较，各自的子类比较（ArrayList，Vector，LinkedList；HashSet，TreeSet）；

 * HashMap的底层实现，之后会问ConcurrentHashMap的底层实现；

* 如何实现HashMap顺序存储：可以参考LinkedHashMap的底层实现；

* HashTable和ConcurrentHashMap的区别；

* 对比Vector，ArrayList,LinkedList有何区别

* 对比Hashtable,HashMap,TreeMap有什么不同

* 谈谈你对HashMap的理解，底层的基本实现。HashMap是怎么解决碰撞问题的？这些数据结构中是线程安全的吗？

* Set的实现原理

* concurrentMap,TreeMap的机制

	* 必问题，每个同学都应该看看源码，对以上全部问题都应该答出来
	
        解答: [Java集合类，从源码解析底层实现原理](https://my.oschina.net/90888/blog/1624758)

## jvm
 * 结合内存说下多线程、进程、线程的区别

* JVM的内存结构，JVM的算法；

* 数组在内存中如何分配；

* 请写一段栈溢出、堆溢出的代码；

* 线程的实现方式、什么是锁重入

* JVM运行时划分

* JVM 内存模型，jvm加载原理

* 简单说说类加载过程，里面执行了哪些操作？GC和内存管理，平时在tomcat里面有没有进行过相关的配置

* 如何线上排查JVM的相关问题

* 请介绍类加载过程，什么是双亲委派模型？

* 谈谈JVM内存区域的划分，哪些区域可能发生OutOfMemoryError？

* 如何监控和诊断JVM堆外内存使用？

* java常见的垃圾收集器有哪些？

* 谈谈你的GC调优思路？

* java内存模型中的happen-before是什么？

* 你知道JVM 几天的内部机制吗？

* java后台服务明显变慢，谈谈你的诊断思路？ 

* JVM老年代和新生代的比例？

* jstack,jmap,jutil分别的意义？如何线上排查JVM的相关问题



## 多线程

* 如何保证集合是线程安全的？ConcurrentHashMap如何实现高效的线程安全？

* 并发包中的ConcurrentLinkedQueue和LinkedBlockingQueue有什么区别

* 说说阻塞队列的实现：可以参考ArrayBlockingQueue的底层实现（锁和同步都行）；

* 进程通讯的方式：消息队列，共享内存，信号量，socket通讯等；

* 用过并发包的哪些类；

* 什么地方用了多线程；

* Excutors可以产生哪些线程池；

* 为什么要用线程池；

* 简单说说线程池的原理和实现

* 线程池的构造类的方法的5个参数的具体意义

* volatile关键字的用法：使多线程中的变量可见；

* synchronized和ReentrantLock有什么区别？

* synchronized底层如何实现？什么是锁升级，降级？

* 一个线程二次调用start()方法会出现什么情况

* 什么情况下java程序会产生死锁？如何定位，修复？

* java并发包提供了哪些并发工具类

* java并发类库提供的线程池有哪几种？分别有什么特点？
 
 
 # 三. IO:
 
* java提供哪些IO方式，NIO如何实现多路复用？
 
*  bio，nio，aio的区别；

* nio框架：dubbo的实现原理；

* 熟悉IO么？与NIO的区别，阻塞与非阻塞的区别


 # 四. 算法：

* java中常说的堆和栈，分别是什么数据结构；另外，为什么要分为堆和栈来存储数据。

* TreeMap如何插入数据：二叉树的左旋，右旋，双旋；

* 一个排序之后的数组，插入数据，可以使用什么方法？答：二分法；问：时间复杂度是多少？

* 平衡二叉树的时间复杂度；

* Hash算法和二叉树算法分别什么时候用；

* 图的广度优先算法和深度优先算法：详见jvm中垃圾回收实现；

* 简诉 快速排序


 # 五. 数据库相关（mysql）：

* msyql优化经验：

* mysql的语句优化，使用什么工具；

* mysql的索引分类：B+，hash；什么情况用什么索引；

* mysql的存储引擎有哪些，区别是什么；

* 说说事务的特性和隔离级别；

* 悲观锁和乐观锁的区别，怎么实现；

* SQL语句的执行顺序

* 开发中用了哪些数据库？ mysql存储引擎有哪些？区别有哪些？悲观锁和乐观锁使用场景、分布式集群实现的原理？

* mysql查询字段区不区分大小写？
解答：不区分，哪怕值也不区分（我当时还反问了，区不区分大小的应用含义有哪些，面试官没说得出来）

* 存储过程的结构和优点
解答：大概结构  
存储过程的优缺点

* 触发器的原理和作用


 # 六. mq：

* mq的原理是什么：有点大。。都可以说；

* mq如何保证实时性；

* mq的持久化是怎么做的；


 # 七. nosql相关（主要是redis）:

* redis和memcache的区别；

* 用redis做过什么；

* rdeis中的基本存储类型、事务、使用场景

* redis是如何持久化的：rdb和aof；

* redis集群如何同步；

* redis的数据添加过程是怎样的：哈希槽；

* redis的淘汰策略有哪些；

* redis有哪些数据结构；



 # 八. zookeeper:

* zookeeper是什么；

* Zookeeper有哪些作用

* zookeeper哪里用到；

* zookeeper的选主过程；

* zookeeper集群之间如何通讯；

* 你们的zookeeper的节点加密是用的什么方式；


 # 九. linux相关：
* linux常用的命令有哪些；

* 如何获取java进程的pid；

* 如何获取某个进程的网络端口号；

* 如何实时打印日志；

* 如何统计某个字符串行数；


 # 十、 三大框架方面问题
  
* springMVC和mybatis的工作原理，底层源码理解多少？

* springAOP，IOC的实现原理，以及他的应用是实现

* Spring 事务的隔离性，并说说每个隔离性的区别

* Spring事务的传播行为，并说说每个传播行为的区别

* hibernate跟Mybatis/ ibatis 的区别，为什么选择？

* struts跟spring mvc的优缺点，让你选会如何选

* 简单说说Spring 事务机制

* Spring 4.0新特性

* spring要把一个组件注入spring中应该怎么做

* spring 使用了哪些设计模式

* springmvc的核心是什么，请求的流程是怎么处理的，控制反转怎么实现的；

* spring里面的aop的原理是什么；

* 谈谈Spring Bean的生命周期和作用域？

* MyBatis如何分页；如何设置缓存；MySQL分页

*  mybatis如何处理结果集：反射，建议看看源码；


# 十一、极客java核心36问

* 有哪些方法可以在运行时动态生成一个Java类？

* 你了解java应用开发中的注入攻击吗？

* 如何写出安全的java代码？

* 谈谈你对java平台的理解

* 动态代理是基于什么原理



# 十五、架构

* 简述一下生产者消费者模式。

* 常见的加密解密

* 如何保障请求的执行顺序

* 分布式事务与分布式锁怎样保障扣款不出现负数

* 分布式session如何设置的

* 分布式session一致性

* 分布式接口的幂等性设计（不能重复扣款）

* 画一下项目技术架构图

* 单机上一个线程池正在处理服务如果忽然断电怎么办?(正在处理和阻塞队列里的请求怎么处理)

* 使用无界阻塞队列会出现什么问题

* 接口如何处理重复请求

* 如何保证共享变量修改时的原子性

* 设计一个对外服务的接口实现类，在1，2，3三个主机（不同ip）上实现负载均衡和顺序轮询机制（考虑并发）

* 高并发下分布式的缓存一致性？

* 手机扫二维码登录的实现原理

* 用过哪些设计模式，手写一个（除单例）；

* 用过哪些加密算法：对称加密，非对称加密算法；

* cookie和session的区别，分布式环境怎么保存用户状态；

* git，svn区别；

* 谈谈你知道的设计模式

* 谈谈乐观锁和悲观锁的原理和应用场景？

* 什么场景下需要用到Netty？对比java标准NIO类库，你知道Netty如何时间更高性能吗？

* 谈谈你了解的常用的风不是id的设计方案？

* 分布式锁实现方式

* CAP简介

* 什么是幂等性

* 常用数据库连接池

* Nginx+Tomcat+Redis实现负载均衡、资源分离、session共享 

* nginx配置文件详解——nginx.conf

*  web如何项目优化

* 单例模式有几种？ 如何优化？

* 分布式锁的实现过程；

* 项目并发如何处理？

*  消息队列的原理和实现

* 重构过代码没有？说说经验；

* 一千万的用户实时排名如何实现；

* 五万人并发抢票怎么实现；

* 单体应用和微服务的区别和目前实现方式

* 简单说说数据库集群和负载均衡、分布式

* mysql大表优化方案

* 数据库垂直和水平拆分


# 模拟面试(连环炮)

#### java集合的数据结构方面。

比如，面试官先问你HashMap是不是有序的？

你肯定回答说，不是有序的。那面试官就会继续问你，有没有有顺序的Map实现类？
	
你如果这个时候说不知道的话，那这个问题就到此结束了。如果你说有TreeMap和LinkedHashMap。

那么面试官接下来就可能会问你，TreeMap和LinkedHashMap是如何保证它的顺序的？
	
如果你回答不上来，那么到此为止。如果你依然回答上来了，那么面试官还会继续问你，你觉得它们两个哪个的有序实现比较好？
	
如果你依然可以回答的话，那么面试官会继续问你，你觉得还有没有比它更好或者更高效的实现方式？

如果你还能说出来的话，那么就你所说的实现方式肯定依然可以问你很多问题。
	
以上就是一个面试官一步一步提问的例子。所以，如果你了解的不多，千万不要敷衍，因为可能下一个问题你就暴露了，还不如直接说不会，把这个问题结束掉，赶紧切换到你熟悉的领域。

#### Java并发包当中的类，它们都有哪些作用，以及它们的实现原理，这些类就是java.concurrent包下面的。

比如面试官可能会先问你，如果想实现所有的线程一起等待某个事件的发生，当某个事件发生时，所有线程一起开始往下执行的话，有什么好的办法吗？

这个时候你可能会说可以用栅栏（Java的并发包中的CyclicBarrier），那么面试官就会继续问你，你知道它的实现原理吗？

如果你继续回答的话，面试官可能会继续问你，你还知道其它的实现方式吗？

如果你还能说出很多种实现方式的话，那么继续问你，你觉得这些方式里哪个方式更好？

如果你说出来某一个方式比较好的话，面试官依然可以继续问你，那如果让你来写的话，你觉得还有比它更好的实现方式吗？

如果你这个时候依然可以说出来你自己更好的实现方式，那么面试官肯定还会揪着这个继续问你。

为什么说面试的时候要引导面试官，原因就在这了。因为面试官的提问很多时候都是有迹可循的，你如果抓住了他的轨迹，能够猜到他下面很可能会问什么，那你在回答的时候就可以往你想要谈的方向去说。这样面试时就会显得更加从容，更加的游刃有余。

#### IO包和NIO包中的内容。这部分里面NIO会是重点，IO包大部分都会比较熟悉，因此可能会直接略过，直接问你NIO的内容。

IO包和NIO包的内容相对来说不是很多，首先NIO模型要熟悉，特别是其中的selector一定要非常清楚它的职责和实现原理。其实NIO的核心是IO线程池，一定要记住这个关键点。有的时候，面试官可能也会问你IO包的设计模式（装饰器模式），为什么要这样设计？


有的面试官还会问你有没有更好的设计，这个时候如果你不知道请果断说自己现在的水平有限，想不出来更好的设计，千万不要信口开河，随意YY。

#### Java的虚拟机的内容。这部分主要包括三部分，GC、类加载机制，以及内存。

面试官可以先问你什么时候一个对象会被GC？

接着继续问你为什么要在这种时候对象才会被GC？

接着继续问你GC策略都有哪些分类？

你如果说出来了，继续问你这些策略分别都有什么优劣势？都适用于什么场景？

你继续说出来了以后，给你举个实际的场景，让你选择一个GC策略？

你如果选出来了，继续问你，为什么要选择这个策略？

#### 关于类加载机制的简单连环炮。

首先肯定是先问你Java的类加载器都有哪些？

回答了这些以后，可能会问你每个类加载器都加载哪些类？

说完以后，可能会问你这些类加载之间的父子关系是怎样的？

你在回答的时候可能会提到双亲委派模型，那么可以继续问你什么是双亲委派模型？

你解释完了以后，可能会继续问你，为什么Java的类加载器要使用双亲委派模型？

你回答完以后，可能会继续问你如何自定义自己的类加载器，自己的类加载器和Java自带的类加载器关系如何处理？

#### 关于内存的连环炮。

首先肯定就是问你内存分为哪几部分，这些部分分别都存储哪些数据？

然后继续问你一个对象从创建到销毁都是怎么在这些部分里存活和转移的？

接着可能会问你，内存的哪些部分会参与GC的回收？

完事以后，可能还会问你Java的内存模型是怎么设计的？

你回答了以后，还会继续问你为什么要这么设计？

问完以后，还可能会让你结合内存模型的设计谈谈volatile关键字的作用？

你在谈的时候，肯定会提到可见性，那么接着可见性这三个字，还可以继续问你并发的内容。


# 特别感谢
以上内容整理选自：

[各大公司Java后端开发面试题总结](https://blog.csdn.net/sinat_35512245/article/details/59056120)

[历年阿里面试题汇总](https://blog.csdn.net/sinat_35512245/article/details/60325685)

[2017年小米春招内推面试面经](https://blog.csdn.net/sinat_35512245/article/details/58209966)

[最近5年133个Java面试问题列表](http://www.importnew.com/17232.html)

[面试总结 —— 高级JAVA工程师](https://bbs.csdn.net/topics/391909962)

[阿里面试回来，想和Java程序员谈一谈](http://www.importnew.com/22056.html)

[面试的角度诠释Java工程师（一）](http://www.importnew.com/23549.html)

[面试的角度诠释Java工程师（二）](http://www.importnew.com/23557.html)

[后端架构师技术图谱](https://github.com/xingshaocheng/architect-awesome)

