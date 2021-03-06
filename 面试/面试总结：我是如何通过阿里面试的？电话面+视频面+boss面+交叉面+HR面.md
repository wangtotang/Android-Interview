![](https://upload-images.jianshu.io/upload_images/15233854-1857f0fad93ac1db.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

>几个月前参加了19年的阿里春招，有幸最终拿到阿里offer，base杭州，岗位客户端开发。这段时间一直忙于其他事情，拿到意向已经过去几个月了其实，但是在其中也有在慢慢整理那次的面试内容，今天终于整理好了，在此分享一些关于面试的干货，攒一波RP，回馈社会。

从阿里面试说起，阿里的面试一般采用电话面试的形式。笔者一共参加五轮面试，一面电话面试+在线编程，二面视频面试+在线编程，三面部门boss面试，四面交叉面，五面HR。在此分享五轮面试的大概问题吧，笔者是android岗开发，所问题型会更偏android。

![](https://upload-images.jianshu.io/upload_images/15233854-4d3c692614171df4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###一面
阿里的面试官都很和蔼。一面面试官听声音感觉应该是入职两三年的感觉。上来自我介绍后直接开始问android相关问题。大概问题如下：

* android中的dp、px、dip相关概念
* handler机制，四个组成部分及源码解析
* 布局相关的控件作用及实现原理
* android中的布局优化
* relativelayout和LinearLayout在实现效果同等情况下选择使用哪个？为什么？
* view的工作原理及measure、layout、draw流程，要求了解源码
* 怎样自定义一个弹幕控件？
* 如果控件内部卡顿你如何去解决并优化？
* listview的缓存机制
* Invalidate、postInvalidate、requestLayout应用场景
* 多线程，5个线程内部打印hello和word，hello在前，要求提供一种方法使得5个线程先全部打印出hello后再打印5个word。
* 实现一个自定义view，其中含有若干textview，textview文字可换行且自定义- - - - view的高度可自适应拓展
* 编程题：将元素均为0、1、2的数组排序。在手打了一种直接遍历三种数目并打印的方法后让手写实现，手写实现后让再说一种稳定的方法，说了一种通过三个下标遍历一遍实现的方法，读者可自行百度，在此不赘述。

一面面完挺懵的，感受到阿里校招的火力，阿里的要求程度高于“知道、会用”那一层，你需要了解底层原理、机制才能过关。一面50min。一面面完，面试官说需要反馈面试过程后才能知道是否通过，后来了解到阿里的一面是“简历筛选”面，刷人不会太多。自我感觉良好，总体答出大概百分之八九十，面完便好好准备二面了。

###二面
二面很重要，二面很重要，二面很重要。二面对于你是否能通过面试，是否能最终从池子中被捞出来都很重要。一面面完的第二天下午收到来自杭州的电话，约了晚上九点的时间，且通知了视频面试和在线编程。一阵慌张……看了那么多面经，没见过谁连续两次编程的……晚上九点，准时登录视频网址后，面试官已经在线。二面面试官稍显严肃，给人感觉非常严谨。上来简单自我介绍后，他说一面评价比较好，他会面试得细致一点，可能时间会稍长。当时心神一紧，做好了鏖战的准备。二面问的内容非常多，且覆盖范围很广，大概问题如下：

####JVM方面

* java内存模型，五个部分，程序计数器、栈、本地栈、堆、方法区。

* 每个部分的概念、特点、作用。

* 类加载的过程，加载、验证、准备、解析、初始化。每个部分详细描述。

* 加载阶段读入.class文件，class文件时二进制吗，为什么需要使用二进制的方式？

* 验证过程是防止什么问题？验证过程是怎样的？加载和验证的执行顺序？符号引用的含义？

* 准备过程的静态成员变量分配空间和设置初始值问题。

* 解析过程符号引用替代为直接引用细节相关。

* 初始化过程jvm的显式初始化相关。

* 类卸载的过程及触发条件。

* 三种类加载器，如何自定义一个类加载器？

* 双亲委派机制。

* JVM内存分配策略，优先放于eden区、动态对象年龄判断、分配担保策略等。

* JVM垃圾回收策略，怎样判对象、类需要被回收？

* 四种垃圾回收算法标记-清除、复制、标记-整理、分代收集。

* JVM中的垃圾回收器，新生代回收器、老年代回收器、stop-the-world概念及解决方法。

* 四类引用及使用场景？

* 基本上JVM方面所有的大的概念全部问到，真的需要理解到位。JVM比较熟悉，全程巴拉巴拉不停地说，有惊无险。

* 集合类
   * 初始引起话题的问题：hashmap了解吗？心中一喜，开启侃侃而谈（胡吹）模式。讲到了以下的一些点：

   * hashmap实现的数据结构，数组、桶等。

   * hashmap的哈希冲突解决方法：拉链法等。拉链法的优缺点。

   * hashmap的参数及影响性能的关键参数：加载因子和初始容量。

   * Resize操作的过程。

   * hashmap容量为2次幂的原因。

   * 讲完一通之后，面试官挺满意，说了解地比较深挺好，抛出了下一个问题hashtable了解吗？又是心中一喜，一通介绍：

   * hashtable线程安全、synchronized加锁。

   * hashtable和hashmap异同。

   * 为什么hashtable被弃用？

   * 果断将话题扯到concurrenthashmap，讲了concurrenthashmap相比于hashtable做的优化、segment的概念、concurrenthashmap高效的原因。中间面试官问的问题：

   * 容器类中fastfail的概念。

   * concurrenthashmap的插入操作是直接操作数组中的链表吗？

   * 集合类相关over，由于都是自己主动在说，把握了主动权，相谈甚欢。

* 多线程

   * 由于上面提出了concurrenthashmap的概念，顺理成章聊起了多线程。有了上一部分的经验全程我主动讲，面试官针对性问了一些问题，大概内容如下：

   * 为什么要使用多线程？多线程需要注意的问题。上下文开销、死锁等。

   * java内存模型、导致线程不安全的原因。

   * volatile关键字，缓存一致性、指令重排序概念。

   * synchronize关键字，java对象头、Markword概念、synchronize底层monitorenter和moniterexit指令。

   * lock语句和synchronize对比。

   * 原子操作，CAS概念、相关参数。

   * 乐观锁、悲观锁概念及使用场景。

   * 线程池概念、实现原理等。

   * JVM锁的优化，偏向锁、轻量级锁概念及原理。

   * 多线程方面回答得比较好，面试官反馈比较满意。

* 数据库
数据库方面笔者水平较菜，没有深入了解。面试官问了一个问题，

   * SQL语句中对表或者字段取别名有什么好处？
并不知道怎么回答，面试官也没有再问数据库相关。之后面试官问了解操作系统，回答：没学过。面试官：好的 ，那不问了。心中感动得无法用言语形容。
* 通信协议
接下来是对通信协议的了解，大概问了下列问题：

   * TCP三次握手、四次挥手。
   * http请求报文结构、响应报文，状态码。
   * http2.0相比于http1.0的新特性，推送、多路复用、消息头压缩等。
   * 通信协议问得不是太深，了解得比较好即可。面试官反馈比较好。最后就是问android了，面试官说感觉你android应该挺厉害的，当时真的是受宠若惊。
* android
android是重头戏。由于之前已经了解挺多，android方面基础的没有多问，比较深入。大概有如下问题：

   * handler机制组成，handler机制每一部分的源码包括looper中的loop方法、    threadlocal概念、dispatchmessage方法源码，runnable封装message等。
   * listview缓存机制、recycleview缓存机制。
   * bitmap高效加载，三级缓存等。
   * binder机制原理。
   * view的工作原理及measure、layout、draw流程。哪一个流程可以放在子线程中去执行？
   * draw方法中需要注意的问题？
   * view的事件分发机制。
   * android性能优化：布局优化、绘制优化、内存泄露优化、bitmap、内存泄露等。
   * 内存泄露的概念？android中发生的场景？怎么解决？讲了handler、动画等。

面试android方面的时候已经真正地淡定下来了，有条不紊地和面试官说了自己所有的理解。反馈也挺好。

* 算法
最后是一题在线编程，题目比较常规，是一题最大连续子序列，需要注意全是负数的处理，在此不赘述可自行百度。

写算法的时候发生了一个小插曲，由于面试官直接面的都是以java写的，而笔者比较熟悉C++写算法，面试官也不太熟悉c++编译（g++），面面相觑一会儿才成功编译输出结果。真心非常感谢二面面试官的细致和耐心，最好的一次面试体验。面试官说他的这一面他过了，还会有一到两轮技术面试，礼貌地感谢面试官之后结束了，至此二面结束。二面108min。关闭连接后长呼一口气和女友分享了喜报，经此一役，我知道我的阿里之路已走完半程。

为什么说二面很重要呢？因为二面是所以技术面试中最为细致、考察最为最为深入的一轮面试，后面的面试官会很大程度上参考这一面试的结果，并且据说这一面很影响评级。

###三面
二面过后的第二天下午收到三面电话，约了三点的面试，由于之前的面试都是晚上可以在教室完成（在此感谢女友，没有你的陪伴就没有一个好的环境完成面试），三点的时间点是上课时间也基本找不到空教室，所以在教师休息的小房间完成了三面面试。

三面面试官感觉是部门主管级别，上来自我介绍后开始问问题。问了一下简历上在学校做的一个android的项目，说一个难点，讲了推送，巴拉巴拉讲了一通极光推送，感觉面试官不是很感冒，问了极光推送的实现原理，笔者一紧张竟然忘了讲长连接……又问了华为实习的项目，难点，怎么优化……我扯了一通字母树，感觉面试官还是不太感冒。这个时候已经有点慌张，然后……面试官开始问优缺点、之前签的公司、为什么想去杭州、你是怎么看待算法？还问了最优成就感的一件事情，你觉得为什么会获得一等奖？是不是因为对手太弱了（懵了……）？回答完直接问还有什么问题想问他…此时有点崩溃，感觉也答得不太好，问了还有哪些方面需要改善。然后结束了面试……三面29min。

面完三面挺难受的，感觉反馈不是很好，没发挥好。难过了一会儿吃了个饭回图书馆继续看书。

###四面
当晚上我还在图书馆感怀阿里离我远去的时候，一个杭州的电话来了……和四面面试官约好了时间，做一个技术和综合素质方面的面试。急匆匆和女友去找到了一个空教室，9点电话如约而至。四面面试官感觉斯文儒雅，上来介绍这是一轮交叉面，最后一轮技术面试。照例自我介绍后，问了如下问题：

通信协议

   * TCP保证可靠传输的实现：停止等待协议、滑动窗口协议、流量控制、拥塞控制等。
项目

   * 说一个你记忆比较深刻的功能：我讲了一个查看当前WiFi网络连接终端信息的功能的实现。
   * 说一下你遇到的问题：讲了一个十几万级别的字符串的匹配通过字母树优化的问题。面试官听了后和我详细分析了一下，得到了一个更好的实现方法……当时一阵汗颜，班门弄斧了。
   * 问了一下项目中使用到的三级缓存策略。
   * 获奖
   * 聊了聊获奖经历，中间是怎么学习的。面试官看了看前面的面试过程，说问了多线程了，那他就不问了……
数据库
数据库方面问了以下的问题：

索引的种类。

* B树、B+树、红黑树。
* B+树和B树相比有什么优点，应用场景？
* 红黑树的一些特点？怎样保持平衡？
* 问着数据库，问着问着扯到数据结构那边去了……说完之后面试官是感觉你这些都有所准备啊，我说对，毕竟是面阿里，面试官笑了说我本来还准备问你一下八大排序的现在感觉你应该都会，我很自信（jian zha）地说对，我都会。至此，面试官说技术方面他没什么问题想问的了，他这是一轮交叉面，集团内部要求的，他是后台开发方面的，不懂android，问我还有什么想问的。笔者抛出了万金油问题，您觉得我还有哪些方面需要优化的。面试官哈哈一笑，说你们这些学生现在问的都是套路问题，他基本上回答的都是这个问题，然后说了一通感觉深度和广度都有，继续保持就好了。四面48min。至此，笔者彻底放心。互道周末愉快后结束了面试。和女友分享喜报后，阿里之路的进度条已经走到80%了。至于为什么有交叉面，众说纷纭，不太清楚。

![](https://upload-images.jianshu.io/upload_images/15233854-4754f5f419aa6eea.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###五面(HR)
度过周末后照例去图书馆学习，在周一下午接到hr的电话。周末准备了一些常见的HR面试问题，结果一个都没问到，问到的问题大概如下：

* 关于之前一次笔试的编程题，为什么没有做出来？后来有思考过吗？
* 你签约的公司给的薪水是怎么样的？如果阿里给你offer，你是怎么考量这两个offer的？
* 为什么没有在之前实习的公司留下来？之前公司的主管是怎么评价你的？
* 你的优缺点？
* 最后日常问问题，万金油问题培养体系和晋升机制。

面完告知一到两周会有结果，要从池子里综合考量捞出一批人给offer（心中一慌，毕竟走到最后的对手都不容小觑）。随后HR面试官加了微信，有问题可以在微信上交流。

###后续
面完HR安心地在备胎池里面躺着。等待的日子总是很难熬，一天一天地过去，各种打听消息，听说有的前几批的拿到了意向（offer），心里拔凉拔凉。在过去四天后，周五的下午问了HR面试官后得知offer已在审批，据说比较稳，就是走个流程。联想到之前面完腾讯hr在offer审批等了很久还是心难安，在熬过周末，周一和周二，offer已经审批了三天，焦虑程度与日俱增。周二晚上十点半的时候，在宿舍无聊刷新闻的时候，突然收到一条短信和一封邮件，打开后发现是录用意向书。真的挺开心，长呼一口气，总算这条路走到了尽头。

以上是我的阿里春招之路的分享。

###总结
洋洋洒洒写到这边已经说了很多，也有一些经验和大家分享。找工作的日子真的很累，不过再累也要坚持。有幸参加过一些公司的面试，问的问题也都大同小异，主要是以下的一些方面：

* java基础
* 集合类
* 多线程
* JVM虚拟机
* 通信协议
* 数据库
* 操作系统
* 算法
* 你的技术方向
* 项目
* 关于每个方面的复习后续会给出分享

###一些感慨
说一些个人感受吧，找工作其实很容易，一些公司单凭学历就可以让你进去上班，现在太缺程序员了，简单到你面试根本不聊技术谈谈人生、聊聊奖项就可以给你发offer，但是找一个好工作不易，数十上百个人抢一两个岗位很常见。

主要你怎么定义你对于“好”的理解，工资高？公司技术氛围好？行业地位高？工作安稳福利好？不加班？仁者见仁智者见智，没必要强行拿自己的价值观去评判别人的工作，最适合的才是最好的。所以在找工作的时候想清楚自己到底想要一个怎样的工作也是挺重要的，定义一个目标，努力去做，才是最重要的。

###技巧小谈
关于面试的一些技巧，个人觉得最根本的还是拓展你的知识架构的宽度和广度，形成你的一套说辞架构。以多线程为例，问到你多线程？可以先从为什么要使用多线程？使用多线程有什么好处？使用多线程一定会比单线程好吗？多线程会导致什么问题？导致问题的java内存模型是怎样的？怎么解决这个问题？解决方法如volatile、synchronize关键字等它的底层实现是怎样的？你是怎么使用多线程的？使用线程池有什么好处……

如果你真正理解了并将它完善成一个体系，面试官让你说多线程，接下来10min，你可以一直讲完。面试的参照不是你和面试官相比如何，而是你和你的竞争者相比如何，如果上面这一套完善地讲完，面试官对你的评价可想而知。

## 最后

![](https://upload-images.jianshu.io/upload_images/15233854-e15b907c4ee04d2f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

总而言之，**成功是留给准备好的人的**。无论是参加什么面试，都要做好充足的准备，注意好面试的礼仪和穿着，向面试官表现出自己的热忱与真诚就好。即使最后没有过关，也要做好经验的总结，为下一次面试做好充足准备。

**这里我为大家准备了一些我在面试后整理的面试专题资料，除了面试题，还总结出了互联网公司Android程序员面试涉及到的绝大部分面试题及答案，并整理做成了文档，以及系统的进阶学习视频资料，免费分享给大家，希望能帮助到你面试前的复习，且找到一个好的工作，也节省大家在网上搜索资料的时间来学习。**

毕竟不管遇到什么样的面试官，去面试首先最主要的就是自己的实力，只要实力够硬，技术够强，就不怕面试拿不到offer！

想要面试顺通嘛，赶紧领取下面的面试资料为之后的面试做足准备叭！这里提前祝各位面试成功！

##### 资料领取方式： **加群免费获取 [Android架构设计](https://links.jianshu.com/go?to=https%3A%2F%2Fjq.qq.com%2F%3F_wv%3D1027%26k%3D5gyv0JM)（185873940）**

![](https://upload-images.jianshu.io/upload_images/15233854-5d1de7be7c073c30.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/759/format/webp)

![](https://upload-images.jianshu.io/upload_images/15233854-163c44dab8cf2095.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

> 为什么某些人会一直比你优秀，是因为他本身就很优秀还一直在持续努力变得更优秀，而你是不是还在满足于现状内心在窃喜！希望读到这的您能点个小赞和关注下我，以后还会更新技术干货，谢谢您的支持！

![](https://upload-images.jianshu.io/upload_images/15233854-f5bf4a7e0079639b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/259/format/webp)
