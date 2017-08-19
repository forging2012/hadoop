# hadoop

## 前言闲谈：

之前做CDN云计算公司来到美年大健康现在在一家医疗大数据公司负责运维部门大大小小的活，既然是医疗大数据当然离不开大数据存储的维护，现在也同时维护大数据运维相关工作 `hadoop,spark,sqoop,hue,hive,Hbase,zookeeper`等等 测试开发生产使用起来,从集群环境维护 提升数据稳定性 高可用维护。



### Hadoop、hbase、zookeeper、chukwa集群配置

```
首先我们要了解hadoop是什么？Hadoop能够做什么？Hadoop的使用场景是什么？Hadoop和大数据、云计算的关系是什么？如何使用hadoop？

当大家对这些问题有了基本的了解之后，接下来我们就要系统性的学习hadoop了。我个人建议大家不要一味的去学习理论知识，最好是理论和实践相结合，可以先跟着视频和文档去操作，先把伪分布式集群搭建起来，把wordcount实例运行起来，对hadoop集群的搭建过程和运行机制有个大概的了解和认知，然后从操作的过程中去发现自己在哪方面是薄弱点，有针对性的去弥补，这样学习就会更有针对性和目的性，学习效果也相对会更好一些，否则学习会很盲目、很痛苦的。

我们知道hadoop有单机模式，伪分布模式和分布式模式。同时hadoop的环境是Linux，所以我们还需要安装Linux系统。因为我们的习惯是使用windows，所以对于Linux上来就安装软件之类的，困难程度会很大。并且我们要搭建集群，需要多台硬件的，不可能为了搭建集群，去买三台电脑。所以从成本和使用的角度我们还需要懂虚拟化方面的知识。这里的虚拟化其实就是我们需要懂得虚拟机的使用。因为hadoop安装在Linux中，才能真正发挥作用。所以我们也不会使用windows。

```
### 基于以上内容。所以我们需要懂得:
```
虚拟化
Linux
java基础
```

### 下面我们来详细介绍： 虚拟化：我们选择的是VMware
```
Workstation，这里就要求我们会搭建虚拟机，安装linux（如centos）操作系统，这方面只要按照视频操作应该还是很简单的，难点在于虚拟机网络的配置，尤其是nat模式和bridge模式，因为hadoop要求主机与虚拟机与外部网络（能上网），这三者是相通的，都能够连接上网络，只有这样在安装的过程中，才不会遇到麻烦。

Linux：对于Linux的学习也是一个过程，因为可能你连最简单的开机和关机命令都不会，更不要谈配置网络。常用的linux命令也就20多种，我们需要做的就是在搭建集群的过程中不断地加强练习，在实践中去记忆。但是我们会遇到各种不会的命令，即使能查到命令，我们也不能使用。为什么会这样，因为有的命令，是需要使用安装包的。所以我们也要学会如何下载安装包。

我们需要使用一些命令，进行网络配置，但是在网络配置中，这里面又必须懂得虚拟机的一些知识，所以前面的虚拟机知识需要掌握扎实一些。

对于有linux基础的学员也可以选择hadoop运维工程师作为职业选择。

提醒大家切忌浮躁，我们不可能一两天就能完成上面的所有内容，我们至少需要花费一周的时间不断地去训练、强化。只要我们熟悉了Linux命令，熟悉了网络知识。后面我们的学习才会很轻松，很快速。

通过以上的学习我们已经会安装集群了，那么接下来我们就需要进入开发阶段。开发零基础，该怎么办呢？

hadoop编程是一个Java框架，同时也是编程的一次革命，使得传统开发运行程序由单台客户端（单台电脑）转换为可以由多个客户端运行（多台机器）运行，使得任务得以分解，这大大提高了效率。

hadoop既然是一个Java框架，因此就要求我们必须要懂Java，网上有大量的资料，所以学习Java不是件难事。但是学到什么程度，可能是我们零基础同学所关心的。

Java：我们需要具备javaSE基础知识，暂时不需要java Web及各种框架知识。如果没有javaSE基础，建议在学习hadoop之前或过程中要加强这方面的学习和训练。当然有java基础和开发经验的学员学习hadoop就会更快速、更轻松。
```

Hadoop相关文档：
可以查看我blog和留言我看到会帮你解答：blog.yangcvo.me

* ZooKeeper集群快速搭建与优化:[ZooKeeper集群快速搭建与优化](http://blog.yancy.cc)

* hadoop新增节点集群启动请求异常：Last contact：200[hadoop新增节点集群启动请求异常：Last contact：200](http://blog.yancy.cc)


