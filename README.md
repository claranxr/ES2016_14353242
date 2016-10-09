# 《嵌入式系统导论》实验报告1
**姓名：牛雪茹	班级：14C2	专业：软件工程（移动信息工程）	学号：14353242** 
***
## Description
####　　DOL是Distributed Operation Layer的缩写，是“分布式操作层”的意思。下面摘录了实验文档里面对于DOL的一些描述和层次的介绍。
>The distributed operation layer (DOL) is a framework that enables the (semi-) automatic mapping of applications onto the multiprocessor SHAPES architecture platform. The DOL consists of basically three parts:
>*  DOL Application Programming Interface: application programmers can write programs without having detailed knowledge about the underlying architecture.
>*  DOL Functional Simulation: to provide programmers a possibility to test their applications
>*  DOL Mapping Optimization: to compute a set of optimal mappings of an application onto the SHAPES architecture platform.

####　　阅读了实验文档的相关知识，我的理解是DOL是一个网络平台，包含应用程序接口，功能仿真和映射优化。应用程序接口可以实现在不了解底层架构的情况下进行程序的编写，功能仿真可以让程序员去测试应用，映射优化实现了从应用程序到结构层的映射。可以实现把一个项目分开来针对不同的部分进行操作，提高了针对性与效率。

## How to install
### 安装必要的环境(涉及到的操作代码如下)
>$   sudo apt-get update
>$   sudo apt-get install ant
>$   sudo apt-get install openjdk-7-jdk
>$   sudo apt-get install unzip

###下载dolethz.zip，systemc文件并解压（涉及到的操作代码如下）
>* mkdir dol   // 新建文件夹
>* unzip dol_ethz.zip -d dol  // 解压文件到dol文件中
>* tar -zxvf systemc-2.3.1.tgz  // 解压文件

### 编译systemc，并运行configure（涉及到的操作代码如下）
>* cd systemc-2.3.1
>* mkdir objdir
>* cd objdir 
>* ../configure CXX=g++ --disable-async-updates
>* sudo make install

### 编译dol（涉及到的操作代码如下）
>* cd /dol
>* ant -f build_zip.xml all

### 运行例子查看结果（涉及到的代码如下）
>* cd /dol/build/bin/main
>* ant -f runexample.xml -Dnumber=1

## Experimental experience
####　　因为自己的虚拟机不能做apt-get update这类的操作，会提示有连接不上这类的error，而且请教过TA之后换了几个源，重建了虚拟机都是不可以的。所以是直接用的TA配置好的虚拟机。但是重新进行了实验的步骤，观察了一下结果，尝试更好的理解DOL和实验。
####　　之后在TA配置好的虚拟机里面进行apt-get install git的操作还是不行，会有error，最后就用了windows环境下的Git Bash来进行github上内容的创建上传等操作。觉得在Git Bash上的语句和操作和linux平台进行的操作有类似之处。
