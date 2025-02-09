# java

## 知识预备

### Java背景知识

Java是美国Sun（斯坦福大学网络公司）公司在1995年推出的一门计算机**高级编程语言**。

但是在2009年是Sun公司被Oracle（甲骨文）公司给收购了，所以目前Java语言是Oracle公司所有产品。

Java早期又称为Oak（橡树），但是后来由于商标注册时，Oak商标已经其他公司注册了，所以后面改名为Java了。

Java创始人：**詹姆斯●高斯林**。

Java能做的事情非常多，它可以做桌面应用的开发、企业互联网应用开发、移动应用开发、服务器系统开发、大数据开发、游戏开发等等。**目前Java的主流开发方向是使用Java开发企业级互联网应用程序**

```
1.桌面应用开发：能够在电脑桌面运行的软件
	举例：财务管理软件、编写程序用的IDEA开发工具等，可以用Java语言开发
	
2.企业级应用开发：大型的互联网应用程序
	举例：淘宝、京东、大家每天都用的tlias教学管理系统等

3.移动应用开发：运行的Android手机端的软件
	举例：QQ客户端、抖音APP等

4.服务器系统：应用程序的后台（为客户端程序提供数据）
	举例：服务器系统为用户推荐那你喜爱的视频

5.大数据开发：大数据是一个互联网开发方向
	举例：目前最火的大数据开发平台是Hadoop，就是用Java语言开发的

6.游戏开发：游戏本质上是给用户提供娱乐的软件，有良好的交互感受
	举例：我的世界MineCraft就是用Java语言开发的
```

### Java语言发展

三个版本：

* Java5.0：这是Java的第一个大版本更新。
* Java8.0：这个是目前绝大数公司正在使用的版本。因为这个版本最为稳定。
* Java15.0：这个是我们学习的版本。

### Java的主要特性

- 面向对象

- 安全性

- 多线程

- 简单易用

- 开源

- 跨平台

  何为跨平台？

  - 操作系统本身其实是不认识Java语言的。
  - 但是针对于不同的操作系统，Java提供了不同的虚拟机。

  - 虚拟机会把Java语言翻译成操作系统能看得懂的语言。

### Java的技术体系

所谓技术体系，就是Java为了满足不同的应用场景提供了不同的技术版本，主要有三个版本。

- Java SE（Java Standard Edition）：叫做标准版，它是后面两个版本的基础，也就是学习后面两个版本必须先学习JavaSE。**我们现阶段学习的就是这个版本中的技术**。
- Java EE（Java Enterprise Edition）: 叫做企业版，它是为企业级应用开发提供的一套解决方案。**后期我们主要学习这个版本中的技术**。
- Java ME（Java Micro Edition）：叫做小型版，它为开发移动设备的应用提供了一套解决方案。**目前已经不被市场认可（淘汰），取而代之的是基于Android系统的应用开发**。

### JDK的安装

![image-20210923091544110](C:\Users\Lenovo\Desktop\Java基础-资料\day01-Java入门\笔记\assets\image-20210923091544110.png)

JVM（Java Virtual Machine），Java虚拟机

JRE（Java Runtime Environment），Java运行环境，包含了JVM和Java的核心类库（Java API）

JDK（Java Development Kit）称为Java开发工具，包含了JRE和开发工具

我们只需安装JDK即可，它包含了java的运行环境和虚拟机。

这里所说的Java开发环境，实际上就是Java官方提供的一个软件，叫做JDK（全称是Java Develop Kit），翻译过来意思就是Java开发工具包。**我们先要到官网上去下载JDK，然后安装在自己的电脑上，才可以在自己的电脑上使用JDK来开发Java程序**

这是JDK下载的官方网址 https://www.oracle.com/java/technologies/downloads/

进入网址后，选择JDK17版本，找到Windows标签，选择x64 Installer版本

双击安装包，按照引导进行安装工作·（最好修改一下安装目录）

​	1. 安装路径不要有中文，不要有空格等一些特殊的符号。

​	2. 以后跟开发相关的所有软件建议都安装在同一个文件夹中，方便管理。

**（需要注意的是安装JDK后不像你安装QQ一样会在桌面上显示一个图标，JDK安装后桌面上没有图标）**

安装完毕后，在文件资源管理器打开JDK的安装目录的bin目录，会发现有两个命令工具 `javac.exe` `java.exe` ，这就是JDK提供给我们使用的**编译工具和运行工具**

在JDK的bin目录，地址栏输入cmd，回车（或者右击，选择在终端打开），打开命令行窗口

**在命令行窗口中输入 `javac -version`回车，然后输入`java -version`回车，如果出现下面红色框框的提示正确版本号，和我们安装的JDK版本号一致，就说明JDK安装成功**

### JDK的安装目录介绍

| 目录名称 |                             说明                             |
| :------: | :----------------------------------------------------------: |
|   bin    | 该路径下存放了JDK的各种工具命令。javac和java就放在这个目录。 |
|   conf   |              该路径下存放了JDK的相关配置文件。               |
| include  |             该路径下存放了一些平台特定的头文件。             |
|  jmods   |                该路径下存放了JDK的各种模块。                 |
|  legal   |             该路径下存放了JDK各模块的授权文档。              |
|   lib    |            该路径下存放了JDK工具的一些补充JAR包。            |

### cmd常用命令（拓展）

快捷键：win + R。

```
E:  //切换到E盘
cd [目录]        //进入指定的目录
cd ..         //退回到上一级目录
cd /         //退回到根目录
dir             //显示当前目录下所有的内容
cls             //清空屏幕
exit         //退出命令提示符窗口
输入文件名        //启动某个文件，在windows操作系统当中，文件名或者文件夹名是忽略大小写的。
```

### Java入门程序

编写一个Java程序需要经过3个步骤：**编写代码，编译代码，运行代码**

- 编写代码：任何一个文本编辑器都可以些代码，如Windows系统自带的记事本
-  编译代码：将人能看懂的源代码（.java文件）转换为Java虚拟机能够执行的字节码文件（.class文件）
-  运行代码：将字节码文件交给Java虚拟机执行

下面演示用Windows自带的记事本完成hello world程序的编写：

1. 新建一个后缀为.java的文本文件`HelloWorld.java`，用记事本编写代码如下。

   ```java
   public class HelloWorld/*必须和文件名相对应*/ {
      public static void main(String[] args) {
        System.out.println(" HelloWorld ");
       }
   }
   ```

2. 进入`HelloWorld.java`文件所在目录，在地址栏输入cmd回车，即可在此处打开命令行窗口。
3. 在命令行窗口输入编译命令`javac HelloWorld.java`完成编译，编译后会生成一个`HelloWorld.class`文件。
4. 再接着输入`java HelloWorld`就可以运行了

> 用到两个命令：
>
> ​	javac + 文件名 + 后缀名 （就是编译java文件）
>
> ​	java + 文件名（运行编译之后的class文件）

#### 常见问题

1、非法字符问题。Java中的符号都是英文格式的。

2、大小写问题。Java语言对大小写敏感（区分大小写）。

3、在系统中显示文件的扩展名，避免出现HelloWorld.java.txt文件。

4、编译命令后的java文件名需要带文件后缀.java

5、运行命令后的class文件名（类名）不带文件后缀.class

### 环境变量

​    如果我想要在CMD的任意目录下，都可以启动某一个软件，那么就可以把这个软件的路径配置到环境变量中的PATH里面。

​    在启动软件的时候，操作系统会先在当前路径下找，如果在当前录课没有再到环境变量的路径中去找。如果都找不到就提示无法启动。

​    对于编写Java程序而言，开发Java程序，需要使用JDK提供的开发工具（比如javac.exe、java.exe等命令），而这些工具在JDK的安装目录的bin目录下，如果不配置环境变量，那么这些命令只可以在bin目录下使用，而我们想要在任意目录下都能使用，所以就要配置环境变量。

​    **注意：现在最新从官网上下载的JDK安装时会自动配置javac、java命令的路径到Path环境变量中去 ，所以javac、java可以直接使用。**

以前下载的老版本的JDK是没有自动配置的，而且自动配置的也只包含了4个工具而已，所以我们需要删掉已经配置完毕的，再次重新配置Path环境变量。

①**JAVA_HOME**：告诉操作系统JDK安装在了哪个位置（未来其他技术要通过这个找JDK）

![image-20210923091710450](C:\Users\Lenovo\Desktop\Java基础-资料\day01-Java入门\笔记\assets\image-20210923091710450.png)

②**Path**：告诉操作系统JDK提供的javac(编译)、java(执行)命令安装到了哪个位置

![image-20210923091721035](C:\Users\Lenovo\Desktop\Java基础-资料\day01-Java入门\笔记\assets\image-20210923091721035.png)

步骤：

- 右键我的电脑，选择属性。
- 点击左侧的高级系统设置
- 选择高级，再点击下面的环境变量。
- 找系统变量里面的PATH
- 把软件的完整路径，配置到PATH当中就可以了。
- （可做可不做）就是把自己配置的路径，移动到最上面。

### Notepad++

编写Java程序的一个软件，记事本的代替。

#### 使用方法：

右键点击java文件，选择edit with notepad++。

点击设置，再点击首选项。在弹出的页面当中，左侧选择新建，中间选择Java，右侧选择ANSI。

### IDEA简述

​	IDEA全称IntelliJ IDEA，是用于Java语言开发的集成环境，它是业界公认的目前用于Java程序开发最好的工具。

​	**集成环境：把代码编写，编译，执行，调试等多种功能综合到一起的开发工具。**

#### 下载与安装

- 到官方网站自行下载，网址为：https://www.jetbrains.com/idea。

- 到资料文件夹中，双击安装包。

- 点击next，准备安装。

- 点击Browse修改安装路径，再点击next。

- 勾选64-bit launcher，表示在桌面新建一个64位的快捷方式，其他的不要勾选，点击next。

- 点击Install，准备安装。

- 等进度条读取完毕之后，会有最终界面提示，点击finish即可。

- 第一次启动会询问，是否导入一些设置，选择第二个不导入，保持默认设置，再点击OK。

- 选择背景主题，左边是黑色背景，右边是白色背景，这个可以根据自己的喜好来选择，选择完毕点击右下角的next。

- 下个页面会让我们购买idea，因为我们是学习阶段，所以可以使用免费使用30天，点击第一排第二个，Evaluate for free。（后续使用学生认证可免费使用）

  资料在"E:\学习资料\大学（含ACM）\后端\JetBrains学生认证流程.pdf"

- 点击蓝色的Evaluate，就可以开始免费试用30天了。

#### IDEA中层级结构介绍

这些结构的划分，是为了方便管理类文件的。

- project（项目、工程）
- module（模块）
- package（包）
- class（类）

##### project（项目、工程）

​	淘宝、京东、黑马程序员网站都属于一个个项目，IDEA中就是一个个的Project。

##### module（模块）

​	在一个项目中，可以存放多个模块，不同的模块可以存放项目中不同的业务功能代码。在黑马程序员的官方网站中，至少包含了论坛模块，报名咨询模块等模块。为了更好的管理代码，我们会把代码分别放在两个模块中存放。

##### package（包）

​	一个模块中又有很多的业务。以黑马程序员官方网站的论坛模块为例，至少包含了发帖，评论等业务，为了把这些业务区分的更加清楚，就会用包来管理这些不同的业务。

##### class（类）

​	就是真正写代码的地方。

##### 小结

- 层级关系

  ​	project - module - package - class

- 包含数量

  ​	project中可以创建多个module
  ​	module中可以创建多个package
  ​	package中可以创建多个class

#### LDEA中的第一个代码

- 双击启动图标
- 点击creat new project
- 点击左下方的Empty Project，再点击右下角的next
- 输入项目的名称，输入项目的存放路径
- 点击ok，idea会帮助我们在本地创建一个项目文件夹
- 点击Module，准备新建一个模块
- 点击+，再点击New Module
- 新建一个Java模块，点击Java，再点击右下角的next
- 输入模块的名称，再点击右下角的Next
- 成功新建一个模块之后，中间就会出现刚刚新建的模块，点击右下角的OK
- 回到主界面，展开刚刚新建的模块，右键点击src，选择New，选择Java Class
- 输入类名，再按回车
- 编写代码
- 运行代码，右键空白处，点击Run
- 最下面会弹出控制台，所有输出语句中的内容，都会在控制台上展示。

#### 类的相关操作

- 新建类文件
- 删除类文件
- 修改类文件

#####  新建类文件

- 所有的Java代码都会写在src文件夹当中。

  所以，右键点击src，选择new，点击Java Class

  ![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建类1.png)

- 输入类名，再按回车

  ![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建类2.png)

- 新建完毕

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建类3.png)

##### 修改类名

- 右键点击想要修改的文件

  点击Refactor

  再点击Rename

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改类名1.png)

- 输入想要修改的名字

  输入完毕点击下面的Refactor

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改类名2.png)

- 文件名和类名均已修改成功

  ![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改类名3.png)

##### 删除类文件

- 想要删除哪个文件，就右键点击该文件

  选择Delete即可

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/删除类文件1.png)

- 在弹出的界面中点击OK，确定删除

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/删除类文件2.png)

> 小贴士：
>
> 此时删除是不走回收站的，直接从硬盘中删掉了。

#### 模块的相关操作

- 新建模块
- 删除模块
- 修改模块
- 导入模块

##### 新建模块

- 点击File，选择Project Structure

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块1.png)

- 选择Module

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块2.png)

- 点击+

  选择New Module

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块3.png)

- 要创建一个Java模块，所以选择第一个Java

  点击右下角的Next

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块4.png)

- 输入模块的名称

  点击右下角的Finish

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块5.png)

- 成功新建完毕之后，在中间空白区域就出现了刚刚新建的模块

  点击右下角的OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块6.png)

- 在主界面中，也会出现刚刚新建的模块

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建模块7.png)

##### 删除模块

- 右键点击模块

  选择Remove Module

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/删除模块1.png)

- 选择Remove，表示确定删除

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/删除模块2.png)

- 此时发现，在IDEA列表页面，删除的模块已经不在了。

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/删除模块3.png)

> 小贴士：
>
> 此时删除仅仅是从IDEA列表中的删除，在本地硬盘中还是存在的。

##### 修改模块

- 右键点击模块名

  选择Refactor

  再选择Rename

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改模块名1.png)

- 选择第三个修改模块名和本地文件夹名

  点击OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改模块名3.png)

- 输入要修改的新的模块名

  输入完毕点击Refactor

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改模块名4.png)

- 回到主界面，就发现模块名和文件夹名都已经修改完毕

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改模块名5.png)



##### 导入模块

- 点击File，选择Project Structure

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块1.png)

- 选择Module

  点击+

  选择Import Module

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块2.png)

- 从本地硬盘中选择要导入的模块

  再点击OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块3.png)

- 不断点击Next

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块4.png)

- 如果中间出现提示框，则点击Overwrite

  然后继续点击右下角的Next

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块5.png)

- 一直点到finish为止

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块6.png)

- 成功导入后，在中间位置就会出现导入的模块信息

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块7.png)

- 在主界面中也会出现导入的模块信息

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块8.png)



- 展开模块点击模块中的Java文件，会发现代码报错。

  是因为导入模块跟JDK没有关联导致。

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块9.png)



- 可以点击右上角的Setup SDK

  再选择已经安装的JDK版本即可

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块10.png)

- 导入完毕之后，代码就恢复正常不会报错了

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/导入模块11.png)

#### IDEA中项目的相关操作

- 关闭项目
- 打开项目
- 修改项目
- 新建项目

##### 关闭项目

- 点击File，选择Close Project即可

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/关闭项目1.png)

- 刚刚操作的项目就已经关闭了

  左侧是项目列表，如果要再次打开该项目，直接点击即可。

  右侧有create new project，可以再建一个新的项目

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/关闭项目2.png)

- 鼠标放在项目上，后面会出现一个叉。

  如果点击了这里的叉，会在IDEA的列表中删除。不会删除本地硬盘上的项目。

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/关闭项目3.png)

##### 打开项目

- 在本界面还可以打开本地已经存在的项目

  点击Open or Import

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/打开项目1.png)

- 选择要打开的项目

  点击OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/打开项目2.png)

- 项目就被打开了。

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/打开项目3.png)

##### 修改项目

- 点击File，选择Project Structure

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改项目1.png)

- 在这个界面，默认是Module

  所以，要先点击Project

  在右侧页面中，输入新的项目名称

  修改JDK版本和编译版本都变成JDK14

  再点击OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改项目2.png)

- 此时发现，项目名称已经修改完毕

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改项目3.png)

- 但是本地文件夹的名字还没有修改

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改项目4.png)

- 需要先关闭当前项目

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/关闭项目1.png)

- 点击项目后面的叉，从列表中移除项目

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/关闭项目3.png)

- 到本地硬盘中手动修改文件夹的名称

 ![计算机发展](F:/JavaSE%E6%9C%80%E6%96%B0%E7%89%88/day02-Java%E5%9F%BA%E7%A1%80%E6%A6%82%E5%BF%B5/%E7%AC%94%E8%AE%B0/img/%E4%BF%AE%E6%94%B9%E9%A1%B9%E7%9B%AE5.png)

- 点击Open or Import重新打开项目

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/打开项目1.png)

- 选择修改之后的项目

  点击OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改项目6.png)

- 此时会发现，项目名称和本地硬盘文件夹的名称都已经修改完毕了

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/修改项目7.png)

##### 新建项目

- 点击File

  选择New

  点击Project

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建项目1.png)

- 同样还是创建一个什么都没有的空项目

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建项目2.png)

- 输入项目的名称

  点击右下角的finish

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建项目3.png)

- IDEA循环是否需要帮我们在本地创建一个新的文件夹

  点击OK

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建项目4.png)

- 询问是在本窗口打开还是在一个新的窗口打开。

  可以点击New Window，在一个新的窗口打开。

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建项目5.png)

- 此时就出现了两个窗口，在一个新的窗口打开了新的项目

![计算机发展](C:/Users/Lenovo/Desktop/Java基础-资料/day02-Java基础概念/笔记/img/新建项目6.png)









## Java基础语法

### 注释

* 单行注释：

~~~java
// 这是单行注释文字
~~~

* 多行注释：

~~~java
/*
这是多行注释文字
这是多行注释文字
这是多行注释文字
*/
注意：多行注释不能嵌套使用。
~~~

* 文档注释（暂时用不到）：

```java
/**
这是多行注释文字
这是多行注释文字
这是多行注释文字
*/
```

### 关键字

被Java赋予了特定含义的英文单词。

| **abstract**   | **assert**       | **boolean**   | **break**      | **byte**   |
| -------------- | ---------------- | ------------- | -------------- | ---------- |
| **case**       | **catch**        | **char**      | **class**      | **const**  |
| **continue**   | **default**      | **do**        | **double**     | **else**   |
| **enum**       | **extends**      | **final**     | **finally**    | **float**  |
| **for**        | **goto**         | **if**        | **implements** | **import** |
| **instanceof** | **int**          | **interface** | **long**       | **native** |
| **new**        | **package**      | **private**   | **protected**  | **public** |
| **return**     | **strictfp**     | **short**     | **static**     | **super**  |
| **switch**     | **synchronized** | **this**      | **throw**      | **throws** |
| **transient**  | **try**          | **void**      | **volatile**   | **while**  |

#### class

表示定义一个类。创建一个类。

类是Java项目最基本的组成单元，一个完整的Java项目有可能会有成千上万个类来组成的。

class后面跟随的就是这个类的名字，简称：类名。在类名后面会有一对大括号，表示这个类的内容。

```java
public class HelloWorld{
	/*class表示定义类。
	类名：HelloWorld
	HelloWorld后面的大括号表示这个类的范围。
	*/
}
```

### 字面量

| **字面量类型** |                 **说明**                  |      **程序中的写法**      |
| :------------: | :---------------------------------------: | :------------------------: |
|      整数      |              不带小数的数字               |          666，-88          |
|      小数      |               带小数的数字                |        13.14，-5.21        |
|      字符      |     必须使用单引号，有且仅能一个字符      |     ‘A’，‘0’，   ‘我’      |
|     字符串     |       必须使用双引号，内容可有可无        | “HelloWorld”，“黑马程序员” |
|     布尔值     | 布尔值，表示真假，只有两个值：true，false |        true 、false        |
|      空值      |            一个特殊的值，空值             |         值是：null         |

### 变量

注意事项：

- 变量名不能重复
- 在一条语句中，可以定义多个变量。但是这种方式影响代码的阅读，所以了解一下即可。
- 变量在使用之前必须要赋值。

```java
public class VariableDemo1{
	public static void main(String[] args){
		//定义一个整数类型的变量
		//数据类型 变量名 = 数据值;
		int a = 16;
		System.out.println(a);//16
		//一条语句可以定义多个变量
        int b = 20, c = 20, d = 20;
        System.out.println(b);
		System.out.println(c);
        System.out.println(b+c);
		//先定义，后赋值
        int age;
        age = 18;
        System.out.println(age);
        //自定义变量
        class student{
            String name;
            String id;
        }  
}
```

### 数据类型

| 数据类型 | 关键字  | 内存占用 |                 取值范围                  |
| :------: | :-----: | :------: | :---------------------------------------: |
|   整数   |  byte   |    1     |  负的2的7次方 ~ 2的7次方-1**(-128~127)**  |
|          |  short  |    2     | 负的2的15次方 ~ 2的15次方-1(-32768~32767) |
|          |   int   |    4     |        负的2的31次方 ~ 2的31次方-1        |
|          |  long   |    8     |        负的2的63次方 ~ 2的63次方-1        |
|  浮点数  |  float  |    4     |        1.401298e-45 ~ 3.402823e+38        |
|          | double  |    8     |      4.9000000e-324 ~ 1.797693e+308       |
|   字符   |  char   |    2     |                  0-65535                  |
|   布尔   | boolean |    1     |                true，false                |

```java
public class VariableDemo2{
    public static void main(String[] args){
        byte number1 = 98;
        System.out.println(number1);
        /*btye是数字型变量中数据范围最小的一个，范围在-128到127之间*/
        long number2 = e+38L;
        System.out.println(number2);
        /*如果希望随便写一个整型字面量是long类型的，需要在其后面加上L/l，建议大写*/
        /*e+38表示是乘以10的38次方，同样，e-45表示乘以10的负45次方。*/
        int number3 = 123456;
        System.out.println(number3);
        /*int的范围大概在正负21亿之间*/

        /*整数类型和小数类型的取值范围大小关系：
        double > float > long > int（默认） > short > byte*/

        double number4 = 98.5;
        System.out.println(number4);
        /*在Java中double是默认浮点型类型*/
        float number5 = 98.5F;
        System.out.println(number5);
        /*随便写一个小数字面量，默认为double，如果希望是float类型，加f/F后缀，建议大写*/

        boolean flag = true;
        System.out.println(flag);
        /*在Java里布尔型数据类型书写要注意和C语言不同*/
        String name = "LiHua";
        System.out.println(name);
        /*S要大写*/
    }
}

```

### 进制

```java
/*不同进制在Java程序中的书写格式*/
System.out.println('a'+1);/*98*/
System.out.println(0b01100001);/*0b表示二进制，输出结果为97*/
System.out.println(0141);/*0表示八进制，输出结果为97*/
System.out.println(0x61);/*0x表示十六进制，输出结果为97*/
```

### 标识符（变量的命名规则）

#### 硬性要求

- 必须由数字、字母、下划线_、美元符号$组成。
- 数字不能开头
- 不能是关键字
- 区分大小写的。

#### 弹性要求

适用于变量名和方法名

* 如果是一个单词，那么全部小写，比如：name
* 如果是多个单词，那么从第二个单词开始，首字母大写，比如：firstName、maxAge

适用于类名

* 如果是一个单词，那么首字母大写。比如：Demo、Test。
* 如果是多个单词，那么每一个单词首字母都需要大写。比如：HelloWorld

#### 阿里巴巴命名规范细节：

1. 尽量不要用拼音。但是一些国际通用的拼音可视为英文单词。

   正确：alibaba、hangzhou、nanjing

   错误：jiage、dazhe

2. 平时在给变量名、方法名、类名起名字的时候，不要使用下划线或美元符号。

   错误：_name

   正确：name

### 键盘录入

​	键盘录入的实际功能Java已经帮我们写好了，不需要我们自己再实现了，而Java写好的功能都放在了Scanner这个类中，所以，我们只要直接使用Scanner这个类就可以了。

```java
//1.导包，其实就是先找到Scanner这个类在哪
import java.util.Scanner;
public class ScannerDemo1{
	public static void main(String[] args){
		//2.创建对象，其实就是申明一下，我准备开始用Scanner这个类了。
		Scanner sc = new Scanner(System.in);/*sc是这个键盘扫描器对象的名字*/
		//3.接收数据
		//当程序运行之后，我们在键盘输入的数据就会被变量i给接收了
		System.out.println("请输入一个数字");/*执行到这，会等待用户输入一个整数，直到按回车继续*/
		int i = sc.nextInt();
		System.out.println(i);
        System.out.println("请您输入您的名字：");
    	String name2 = sc.next();
        /*sc还有很多属性，输入的类型不一样调用的功能也不一样，比如输入字符串是sc.next();*/
    	System.out.println(name2 + "欢迎您进入系统~~");
	}
}
```

### 运算符

#### 算术运算符

```java
/*+ - * :跟小学数学中一模一样没有任何区别，此处不再做演示*/
int a2 = 5;
System.out.println("abc" + a2); // "abc5"
System.out.println(a2 + 5); //  10
System.out.println("itheima" + a2 + 'a'); // "itheima5a"
System.out.println(a2 + 'a' + "itheima"); // ”102itheima“
/*当+操作中出现了字符，会拿着字符到计算机内置的ASCII码表中去查对应的数字，然后再进行计算。*/
/*ASCII码表中：'a'   -----    97       'A'   -----    65*/
/*当+操作中出现字符串时，此时就是字符串的连接符，会将前后的数据进行拼接，并产生一个新的字符串。*/
System.out.println(1 + 2 + "abc" + 2 + 1);//“3abc21”
System.out.println(1 + 2 + "abc" + 2 + 1);//"1abc1"
/*当连续进行+操作时，从左到右逐个执行的。*/
String name = "黑默丁格";
System.out.println("我的名字是" + name);//我的名字是黑默丁格
/*当字符串跟变量相加的时候，实际上是跟变量里面的值进行拼接。*/
System.out.println(5 / 2); // 2.5 ==> 2
System.out.println(5.0 / 2); // 2.5
int k = 5;
int j = 2;
System.out.println(1.0 * k / j); // 2.5
/*整数相除结果只能得到整除，如果结果想要是小数，必须要有小数参数。*/
System.out.println(10.0 / 3);//3.3333333333333335
/*小数直接参与运算，得到的结果有可能是不精确的，所以在保证数据精准度的前提下，尽量避开浮点型数据*/
System.out.println(10 % 2);//0
System.out.println(10 % 3);//1
/*%：取模、取余。他做的也是除法运算，只不过获取的是余数而已。*/
```

##### 应用：数值拆分算法

```java
/*公式：获取任意一个数上每一位数。*/
//个位：数字 % 10
//十位：数字 / 10 % 10
//百位：数字 / 100 % 10
//千位：数字 / 1000 % 10
//以此类推
```

#### 自增自减运算符

* 放在变量的前面，我们叫做先++。 比如：++a
* 放在变量的后面，我们叫做后++。 比如：a++
* 不管是先++，还是后++。单独写在一行的时候，运算结果是一模一样的。

```java
int a = 10;
a++;//就是让变量a里面的值 + 1
System.out.println(a);//11
++a;//就是让变量a里面的值 + 1
System.out.println(a);//12
//System.out.println(2++);
//上面的写法是错误的，自增自减只能对变量进行操作，不能操作字面量。
```

#### 赋值运算符

```java
public class OperatorDemo6 {
    public static void main(String[] args) {
        //1.最为简单的赋值运算符用法
        int a = 10;//就是把10赋值给变量a
        System.out.println(a);

        //2.如果等号右边需要进行计算。
        int b = 20;
        int c = a + b;//先计算等号右边的，把计算的结果赋值给左边的变量
        System.out.println(c);

        //3.特殊的用法
        a = a + 10;//先计算等号右边的，把计算的结果赋值给左边的变量
        System.out.println(a);//20
        
        //4.扩展赋值运算符
        int a = 10;
        int b = 20;
        a += b;
        // 把左边和右边相加，再把最终的结果赋值给左边，对右边没有任何影响，+=、-=、*=、/=、%=同理
        // 相当于 a = a + b;
        System.out.println(a);//30
        System.out.println(b);//20
        
        //5.扩展的赋值运算符中隐层还包含了一个强制转换
        byte x = 10;
    	byte y = 30;
    	x+=3; 
        //这句代码没有问题，因为这里有隐含的强制类型转换
    	//x+=3; 等价于 byte x = (byte)(x+y);
    	x = x + y; 
        //这句代码有问题，因为两个byte类型数据相加，会提升为int类型;
    }
}
```

#### 关系运算符

又叫比较运算符，其实就是拿着左边跟右边进行了判断而已。

| 符号 |                             解释                             |
| :--: | :----------------------------------------------------------: |
|  ==  | 就是判断左边跟右边是否相等，如果成立就是true，如果不成立就是false |
|  !=  | 就是判断左边跟右边是否不相等，如果成立就是true，如果不成立就是false |
|  >   | 就是判断左边是否大于右边，如果成立就是true，如果不成立就是false |
|  >=  | 就是判断左边是否大于等于右边，如果成立就是true，如果不成立就是false |
|  <   | 就是判断左边是否小于右边，如果成立就是true，如果不成立就是false |
|  <=  | 就是判断左边是否小于等于右边，如果成立就是true，如果不成立就是false |

重点敲黑板！！！

​	**关系运算符最终的结果一定是布尔类型的。要么是true，要么是false**

​	**在写==的时候，千万不要写成=**

#### 逻辑运算符

```java
//&两边都是真，结果才是真。
System.out.println(true & true);//true
System.out.println(false & false);//false
System.out.println(true & false);//false
System.out.println(false & true);//false
//|两边都是假，结果才是假，如果有一个为真，那么结果就是真。
System.out.println(true | true);//true
System.out.println(false | false);//false
System.out.println(true | false);//true
System.out.println(false | true);//true
//^左右不相同，结果才是true，左右相同结果就是false
System.out.println(true ^ true);//false
System.out.println(false ^ false);//false
System.out.println(true ^ false);//true
System.out.println(false ^ true);//true
//false取反就是true，true取反就是false
System.out.println(!false);//true
System.out.println(!true);//false
System.out.println(!!false);//注意点：取反最多只用一个。
/*运算顺序非与或，我们只需要记忆：小括号优先于所有。*/
```

#### 短路逻辑运算符

短路的逻辑核心：

**当左边不能确定整个表达式的结果，右边才会执行。**

**当左边能确定整个表达式的结果，那么右边就不会执行了。从而提高了代码的运行效率。**

```java
/*注意 单个&或者单个|称逻辑与/逻辑或，&&或者||称作短路与/短路或，顾名思义，带有短路属性*/
int i = 10;
int j = 20;
System.out.println(i > 100 && ++j > 99);
System.out.println(i > 100 & ++j > 99);
System.out.println(j);//j为21，第一个短路逻辑与的后半部分代码没有被执行
int m = 10;
int n = 30;
System.out.println(m > 3 || ++n > 40);
System.out.println(m > 3 | ++n > 40);
System.out.println(n);//n为31，第一个短路逻辑或的后半部分代码没有被执行
```

#### 三元运算符

关系表达式 ？ 表达式1 ：表达式2 ；

* 计算关系表达式的值。
* 如果关系表达式的值为真，那么执行表达式1。
* 如果关系表达式的值为假，那么执行表达式2。

**三元运算符的最终结果一定要被使用，要么赋值给一个变量，要么直接打印出来。**

```java
public class OperatorDemo12 {
    public static void main(String[] args) {
        //需求：求两个数的较大值
        int a = 10;
        int b = 20;
        //格式：关系表达式 ？ 表达式1 ： 表达式2 ；
        //注意点：
        //三元运算符的最终结果一定要被使用。
        //要么赋值给一个变量，要么直接输出。
       int max =  a > b ? a : b ;
        System.out.println(max);
        System.out.println(a > b ? a : b);
    }
}
```

##### 应用：三个数找最大值算法

```java
int num1 = 150;
int num2 = 210;
int num3 = 165;
//2.利用三元运算符求出两个数中的较大值。
int temp = num1 > num2 ? num1 : num2;
//3.求出最终的结果
int max = temp > num3 ? temp : num3;
System.out.println(max);
```

### 表达式

用运算符把常量或者变量连接起来的，符合Java语法的式子就是表达式。

比如：a + b 这个整体就是表达式。

而其中+是算术运算符的一种，所以这个表达式也称之为算术表达式。

### 隐式转换（自动类型提升）

​	把一个取值范围小的数据或者变量，赋值给另一个取值范围大的变量。此时不需要我们额外写代码单独实现，是程序自动帮我们完成的。

​	**byte   short   int   long   float   double依次从小到大**

​	**byte，short，char 三种类型数据在和其他类型数据运算时，都会转换为int类型再运算**

```java
double d = 10;
System.out.println(d);//10.0
/*10是整数，整数默认是int类型的，double比int大，所以自动转为double*/
byte b = 100;
int i = b;//可以成功赋值
/*因为byte的取值范围是小的，int的取值范围是大的，在底层进行了隐式转换，不需要我们额外写代码单独实现，是可以直接赋值。*/
int i = 10;
long n = 20L;
long result = i + n;
System.out.println(result);
/*变量i里面的值会自动提升为long类型，最终的结果其实就是两个long相加，那么最终的result是long类型的。*/
byte b1 = 110;
byte b2 = 80;
int b3 = b1 + b2;
System.out.println(b3);
/*即使两个byte运算，结果也会提升为int*/
char ch = 'a';
long i = ch;
System.out.println(i);//97
/*特殊地 char可以转换成int 再进行第二次转换*/
/*第一步，char自动转换为int，第二步，int + long，结果自动转换为long*/
int i = 10;
long n = 100L;
double d = 20.0;
double result = i + n + d;
/*多种数据类型参与运算，其结果以大的数据类型为准，这里最大的是double，所以结果是double*/
```

### 强制转换

​	如果要把一个取值范围大的数据或者变量赋值给另一个取值范围小的变量。是不允许直接操作。

​	如果一定要这么干，就需要加入强制转换。

```java
/*区别于自动类型转换的小转大 强制类型转换发生于需要大转小的场景 可能有数据丢失的风险*/
public class OperatorDemo2 {
    public static void main(String[] args) {
        double a = 12.3;
        int b = (int) a;
        /*发生强制类型转换*/
        System.out.println(b);
        /*结果为12，小数部分缺失*/
    }
}
```

### 流程控制语句

#### 顺序结构

​	顺序结构是程序中最简单最基本的流程控制，没有特定的语法结构，按照代码的先后顺序，依次执行，程序中大多数的代码都是这样执行的。

#### 分支结构之判断与选择结构

##### If语句

```java
/*格式1：
if (关系表达式) {
    语句体;	
}*/
```

```java
/*格式2：
if (关系表达式) {
    语句体1;	
} else {
    语句体2;	
}*/
```

```java
/*格式3：
if (关系表达式1) {
    语句体1;	
} else if (关系表达式2) {
    语句体2;	
} 
…
else {
    语句体n+1;
}*/
```

```java
Scanner temperate = new Scanner(System.in);
int temp = temperate.nextInt();
if (temp > 37) {
    System.out.println("他发烧了");
}
/*注意点：*/
/*1.if条件后面没有分号(;) */
/*2.if后的大括号内只有一行代码时，大括号可省略*/
/*3.如果我们要对一个布尔类型的变量进行判断，不要写==，直接把变量写在小括号中即可*/
```

##### switch语句

```java
switch (表达式) {
	case 1:
		语句体1;
		break;
	case 2:
		语句体2;
		break;
	...
	default:
		语句体n+1;
		break;
}
/*注意点如下*/
//1.表达式不支持double、float;JDK5开始支持枚举，JDK7开始支持String。
//2.case给出的值不允许重复，且不能是变量。
//3.正常使用switch的时候，不要忘记写break，否则会出现穿透现象。
//4.default可以放在任意位置，也可以省略
```

```java
int number = 10;
switch (number) {
    case 1 -> System.out.println("一");
    case 2 -> System.out.println("二");
    case 3 -> System.out.println("三");
    default -> System.out.println("其他");
}
//switch在JDK12的新特性
```

#### 循环结构

##### for循环

```java
for (初始化语句;条件判断语句;条件控制语句) {
	循环体语句;
}
//- 初始化语句：  用于表示循环开启时的起始状态，简单说就是循环开始的时候什么样
//- 条件判断语句：用于表示循环反复执行的条件，简单说就是判断循环是否能一直执行下去
//- 循环体语句：  用于表示循环反复执行的内容，简单说就是循环反复执行的事情
//- 条件控制语句：用于表示循环执行中每次变化的内容，简单说就是控制循环是否能执行下去
```

```java
//需求：打印3行Hello World
for(int i = 0; i < 3; i++) {
    System.out.println("Hello World");
}
/*不多说，用法和C语言里一样*/
```

##### while循环

```java
/*初始化语句;
while(条件判断语句){
	循环体;
	条件控制语句;
}*/
```

```java
// 需求：打印5行Hello World
int i = 0;
while (i < 5) {
    // i = 0 1 2 3 4
    System.out.println("Hello World");
    i++;
}
/*也不多说，用法和C语言里一样*/
```

##### do...while循环

```java
/*初始化语句;
do{
    循环体;
    条件控制语句;
}while(条件判断语句);*/
```

```java
int i = 0;
do {
    System.out.println();
    i++;
}while (i < 3);
/*do-while和while最大的特点就是，一个是先执行再判断，一个是先判断后执行*/
```

##### 无限循环（死循环）

```java
/*情况一*/
for(;;){
    System.out.println("这是个死循环");
}
//初始化语句可以空着不写，表示循环之前不定义任何的控制变量。
//条件判断语句可以空着不写，如果不写，默认表示true，循环一直进行。
//条件控制语句可以空着不写，表示每次循环体执行完毕后，控制变量不做任何变化。
/*情况二*/
while(true){
    System.out.println("循环执行一直在打印内容");
}
//小括号里面就不能省略了，true一定要写出来，否则代码会报错。
/*情况三*/
do{
    System.out.println("循环执行一直在打印内容");
}while(true);
```

##### 循环嵌套

外部循环每循环一次，内部循环会全部执行完一轮

###### 应用：冒泡查找

### 条件控制语句

#### break

```java
//1.吃1~5号包子
for (int i = 1; i <= 5; i++) {
    System.out.println("在吃第" + i + "个包子");
    //2.吃完第三个的时候就不吃了
    if(i == 3){
        break;//结束整个循环。
    }
}
/*break只能用于结束所在循环，或者结束所在switch分支的执行*/
```

#### continue

```java
//1.吃1~5号包子
for (int i = 1; i <= 5; i++) {
    //2.第3个包子有虫子就跳过，继续吃下面的包子
    if(i == 3){
        //跳过本次循环（本次循环中，下面的代码就不执行了），继续执行下次循环。
        continue;
    }
    System.out.println("在吃第" + i + "个包子");
}
/*continue只能在循环中使用*/
```

### Random

Random跟Scanner一样，也是Java提前写好的类

我们不需要关心是如何实现的，只要直接使用就可以了

```java
//1.导包
import java.util.Random;
public class RandomDemo1 {
    public static void main(String[] args) {
        //2.创建对象
        Random r = new Random();
        //3.生成随机数
        int number = r.nextInt(100);//包左不包右，包头不包尾
        //0 ~ 99
        System.out.println(number);

    }
}
```

### 数组

#### 概念

指的是一种容器，可以同来存储同种数据类型的多个值。

**但是数组容器在存储数据的时候，需要结合隐式转换考虑，比如以下这个例子：**

​	定义了一个int类型的数组。那么boolean。double类型的数据是不能存到这个数组中的，

​	但是byte类型，short类型，int类型的数据是可以存到这个数组里面的。

建议：

​	容器的类，和存储的数据类型保持一致。

#### 数组的静态初始化

```java
/*简化定义静态数组*/
int[] array = {10,20,30,40};
String[] names= {"牛二", "西门", "全蛋"};
```

```java
/*标准定义静态数组*/
double[] scores = new double[]{89.9, 99.5, 59.5, 88.0};
//new：就是给数组在内存中开辟了一个空间。
//等号前后的数据类型必须保持一致。
//不管是哪一中创建方法，数组一旦创建之后，长度不能发生变化。
```

```java
/*不常用的数组写法，了解即可，不是错误代码*/
int ages[] = {12, 24, 36};
```

#### 地址值

```java
int[] arr = {1,2,3,4,5};
System.out.println(arr);//[I@6d03e736
double[] arr2 = {1.1,2.2,3.3};
System.out.println(arr2);//[D@568db2f2
/*
以[I@6d03e736为例：
[ ：表示现在打印的是一个数组。
I：表示现在打印的数组是int类型的。
@：仅仅是一个间隔符号而已。
6d03e736：就是数组在内存中真正的地址值。（十六进制的）
但是，我们习惯性会把[I@6d03e736这个整体称之为数组的地址值。
*/
```

打印数组的时候，实际出现的是数组的地址值。

数组的地址值：就表示数组在内存中的位置。

地址值对于我们来说，作用不大，简单了解。

#### 访问数组与修改数组

```java
public class ArrDemo2 {
    public static void main(String[] args) {
       int[] arr = {1,2,3,4,5};
       //需求1：获取arr数组中，3索引上的值
        int number = arr[3];
        System.out.println(number);
        System.out.println(arr[3]);

       //需求2：将arr数组中，3索引上的值修改为10
        arr[3] = 10;
        //一旦修改之后，原来的值就会被覆盖了
        System.out.println("修改之后为:" + arr[3]);

    }
}
```

#### 索引

也叫角标、下标

就是数组容器中每一个小格子对应的编号。

```java
double[] scores = new double[]{89.9, 99.5, 59.5, 88.0};
System.out.println(scores.length);
/*访问数组元素个数*/
System.out.println(scores.length - 1);
/*获取数组的最大索引*/
```

#### 数组的遍历

```java
for (int i = 0; i < scores.length; i++) {
    // i的取值 = 0,1,2
    System.out.println(scores[i]);
}
/*数组的遍历*/
```

#### 数组的默认初始化值

```java
//整数类型：0
//小数类型：0.0
//布尔类型：false
//字符类型：'\u0000'
//引用类型：null
```

#### 数组的动态初始化

静态初始化：手动指定数组的元素，系统会根据元素的个数，计算出数组的长度。

动态初始化：手动指定数组长度，由系统给出默认初始化值。

```java
/*数组的动态初始化*/
int[] arr = new int[3];
/*数组中的元素默认值是0，3是数组长度*/
int[] arr1 = {11, 22, 33};
int[] arr2 = arr1;// 把int类型的数组变量arr1赋值给int类型的数组变量arr2
System.out.println(arr1);//结果为[I@4c873330
System.out.println(arr2);//结果为[I@4c873330
arr2[1] = 99;
System.out.println(arr1[1]);//结果为99，修改arr2也会修改arr1，arr1和arr2指向同一个地址
arr2 = null; // 拿到的数组变量中存储的值是null
System.out.println(arr2);//结果为null
System.out.println(arr1);//结果为[I@4c873330
System.out.println(arr1[1]);//结果为99
//System.out.println(arr2[0]);
//System.out.println(arr2.length);
/*以上这两行代码都会报错*/
/*两个变量指向同一个数组时，两个变量记录的是同一个地址值。*/
/*当一个变量修改数组中的元素时，另一个变量去访问数组中的元素，元素已经被修改过了。*/
```

#### 数组的录入

```java
int[] codes = new int[5];
Scanner sc = new Scanner(System.in);
for (int i = 0; i < codes.length; i++) {
    // i = 0 1 2 3 4
    System.out.println("请您输入第" + (i + 1) +"个员工的工号：");
    int code = sc.nextInt();
    codes[i] = code;
}
```

#### 数组题目练习

交换数据

```java
//1.定义数组存储数据
int[] arr = {1,2,3,4,5};
//2.利用循环去交换数据
for(int i = 0,j = arr.length - 1; i < j; i++,j--){
    //交换变量i和变量j指向的元素
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}
//当循环结束之后，那么数组中的数据就实现了头尾交换
for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i] + " ");
}
```

打乱数据

```java
//1.定义数组存储1~5
int[] arr = {1, 2, 3, 4, 5};
//2.循环遍历数组，从0索引开始打乱数据的顺序
Random r = new Random();
for (int i = 0; i < arr.length; i++) {
    //生成一个随机索引
    int randomIndex = r.nextInt(arr.length);
    //拿着随机索引指向的元素 跟 i 指向的元素进行交换
    int temp = arr[i];
    arr[i] = arr[randomIndex];
    arr[randomIndex] = temp;
}
//当循环结束之后，那么数组中所有的数据已经打乱顺序了
for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i] + " ");
}
```

### 方法

方法（method）是程序中最小的执行单元

* 方法必须先创建才可以使用，该过程成为方法定义
* 方法创建后并不是直接可以运行的，需要手动使用后，才执行，该过程成为方法调用

#### 无参数方法

```java
public class MethodTest {
    public static void main(String[] args) {
        //在main()方法中调用定义好的方法
        getMax();
    }

    //定义一个方法，用于打印两个数字中的较大数，例如getMax()
    public static void getMax() {
        //方法中定义两个变量，用于保存两个数字
        int a = 10;
        int b = 20;

        //使用分支语句分两种情况对两个数字的大小关系进行处理
        if(a > b) {
            System.out.println(a);
        } else {
            System.out.println(b);
        }
    }
}
```

#### 带参数方法

方法定义时，参数中的数据类型与变量名都不能缺少，缺少任意一个程序将报错

方法定义时，多个参数之间使用逗号( ，)分隔

方法调用时，参数的数量与类型必须与方法定义中的设置相匹配，否则程序将报错 

```java
public class MethodTest {
    public static void main(String[] args) {
        //在main()方法中调用定义好的方法（使用常量）
        getMax(10,20);
        //调用方法的时候，人家要几个，你就给几个，人家要什么类型的，你就给什么类型的
        //getMax(30);//报错
        //getMax(10.0,20.0);//报错

        //在main()方法中调用定义好的方法（使用变量）
        int a = 10;
        int b = 20;
        getMax(a, b);
    }

    //定义一个方法，用于打印两个数字中的较大数，例如getMax()
    //为方法定义两个参数，用于接收两个数字
    public static void getMax(int a, int b) {
        //使用分支语句分两种情况对两个数字的大小关系进行处理
        if(a > b) {
            System.out.println(a);
        } else {
            System.out.println(b);
        }
    }
}
```

#### 带返回值方法

```java
public class MethodTest {
    public static void main(String[] args) {
        //在main()方法中调用定义好的方法并使用变量保存
        int result = getMax(10,20);
        //方法的返回值通常会使用变量接收，否则该返回值将无意义
        System.out.println(result);

        //在main()方法中调用定义好的方法并直接打印结果
        System.out.println(getMax(10,20));
    }

    //定义一个方法，用于获取两个数字中的较大数
    public static int getMax(int a, int b) {
        //使用分支语句分两种情况对两个数字的大小关系进行处理
        //根据题设分别设置两种情况下对应的返回结果
        if(a > b) {
            return a;
        } else {
            return b;
        }
    }
}
```

###### 拓展  return的单独用法

```java
public static void chu(int a , int b){
    if(b == 0){
        System.err.println(“您的数据有误！！不执行！！”);
        return; // 直接跳出并结束当前chu方法的执行
    }
    int c = a / b;
    System.out.println("除法结果是："+c);
}
```

#### 方法中的一些注意点！！！

```java
/*1.方法没有先后顺序，但是不能把一个方法定义在另一个方法中。（嵌套）*/
public class MethodDemo {
    public static void main(String[] args) {

    }

    public static void methodOne() {
		public static void methodTwo() {
       		// 这里会引发编译错误!!!
    	}
    }
}
```

```java
/*2.返回值类型写void（无返回申明）时，方法内不能使用return返回数据，如果方法的返回值类型写了具体类型，方法内部则必须使用return返回对应类型的数据。*/
/*3.return语句的下面，不能编写代码，属于无效的代码，执行不到这儿。*/
public class MethodDemo {
    public static void main(String[] args) {

    }
    public static void methodTwo() {
        //return 100; 编译错误，因为没有具体返回值类型
        return;	
        //System.out.println(100); return语句后面不能跟数据或代码
    }
}
```

```java
/*4.调用无返回值的方法，只有1种方式： 只能直接调用。*/
public class MethodDemo {
	public static void main(String[] args) {
		judge(7); //调用后打印：7是一个奇数
    	judge(8); //调用后打印：8是一个偶数
    }
	public static void judge(int number){
        if(number % 2 == 0){
            System.out.println(number + "是一个偶数！");
        }else {
            System.out.println(number + "是一个奇数！");
        }
    }
}   
```

```java
/*5.基本类型的参数传递存储的数据值，引用类型的参数传递存储的地址值。*/
```

#### 向方法内传递数组

```java
// 目标：完成判断两个int类型的数组是否一样。
public class MethodDemo {
	public static void main(String[] args) {
		int[] arr1 = {10, 20, 30};
		int[] arr2 = {10, 20, 30};
		System.out.println(equals(arr1, arr2));
    }
	public static boolean equals(int[] arr1, int[] arr2){
        // 1、判断arr1和arr2是否都是null.
        if (arr1 == null && arr2 == null) {
            return true; // 相等的
        }
        // 2、判断arr1是null，或者arr2是null.
        if (arr1 == null || arr2 == null) {
            return false; // 不相等
        }
        // 3、判断2个数组的长度是否一样，如果长度不一样，直接返回false.
        if (arr1.length != arr2.length) {
            return false; // 不相等
        }
        // 4、两个数组的长度是一样的，接着比较它们的内容是否一样。
        for (int i = 0; i < arr1.length; i++) {
            // 判断当前位置2个数组的元素是否不一样，不一样直接返回false
            if (arr1[i] != arr2[i]) {
                return false; // 不相等的
            }
        }
        return true; // 两个数组是一样的。
	}
} 
```

#### 方法的通用格式

```java
public static 返回值类型 方法名(参数) {
   方法体; 
   return 数据 ;
}
```

* 解释：

  * public static 	修饰符，目前先记住这个格式
  * 返回值类型	   方法操作完毕之后返回的数据的数据类型，如果方法操作完毕，没有数据返回就写void，而且方法体中一般不写return
  * 方法名		   调用方法时候使用的标识
  * 参数		       由数据类型和变量名组成，多个参数之间用逗号隔
  * 方法体		   完成功能的代码块
  * return		   如果方法操作完毕，有数据返回，用于把数据返回给调用者

* 定义方法时，要做到两个明确

  * 明确返回值类型：主要是明确方法操作完毕之后是否有数据返回，如果没有，写void；如果有，写对应的数据类型
  * 明确参数：主要是明确参数的类型和数量

* 调用方法时的注意：

  * void类型的方法，直接调用即可
  * 非void类型的方法，推荐用变量接收调用

### 形参与实参

1. 形参：方法定义中的参数

​          等同于变量定义格式，例如：int number

2. 实参：方法调用中的参数

​          等同于使用变量或常量，例如： 10  number

### 方法重载

* 方法重载概念

  方法重载指同一个类中定义的多个方法之间的关系，满足下列条件的多个方法相互构成重载

  * 多个方法在同一个类中
  * 一个类中，多个方法的名称相同，但它们形参列表不同
  * 形参列表不同指的是：形参的个数、类型、顺序不同，不关心形参的名称

* 注意：

  * 重载仅对应方法的定义，与方法的调用无关，调用方式参照标准格式
  * 重载仅针对同一个类中方法的名称与参数进行识别，与返回值无关，换句话说不能通过返回值来判定两个方法是否相互构成重载

```java
/*正确重载*/
public class MethodDemo {
	public static float fn(int a) {
    	//方法体
    }
    public static int fn(int a , int b) {
    	//方法体
    }
}
/*错误重载1*/
public class MethodDemo {
	public static void fn(int a) {
    	//方法体
    }
    public static int fn(int a) { 	/*错误原因：重载与返回值无关*/
    	//方法体
    }
}
/*错误重载2*/
public class MethodDemo01 {
    public static void fn(int a) {
        //方法体
    }
} 
public class MethodDemo02 {
    public static int fn(double a) { /*错误原因：这是两个类的两个fn方法*/
        //方法体
    }
}
```

#### 应用：全类型判断补充算法

```java
/*需求：使用方法重载的思想，设计比较两个整数是否相同的方法，兼容全整数类型（byte,short,int,long） */
public class MethodTest {
    public static void main(String[] args) {
        //调用方法
        System.out.println(compare(10, 20));
        System.out.println(compare((byte) 10, (byte) 20));
        System.out.println(compare((short) 10, (short) 20));
        System.out.println(compare(10L, 20L));
    }

    //int
    public static boolean compare(int a, int b) {
        System.out.println("int");
        return a == b;
    }

    //byte
    public static boolean compare(byte a, byte b) {
        System.out.println("byte");
        return a == b;
    }

    //short
    public static boolean compare(short a, short b) {
        System.out.println("short");
        return a == b;
    }

    //long
    public static boolean compare(long a, long b) {
        System.out.println("long");
        return a == b;
    }

}
```

## 面向对象

在之前我们接触的算法大多都是面向过程的。

### 类

* 类

  * 类的理解

    * 类是对现实生活中一类具有共同属性和行为的事物的抽象
    * 类是对象的数据类型，类是具有相同属性和行为的一组对象的集合
    * 简单理解：类就是对现实事物的一种描述

  * 类的组成

    * 属性：指事物的特征，例如：手机事物（品牌，价格，尺寸）

      ​	在类中通过成员变量来体现（类中方法外的变量）

    * 行为：指事物能执行的操作，例如：手机事物（打电话，发短信）

      ​	在类中通过成员方法来体现（和前面的方法相比去掉static关键字即可）

* 类和对象的关系

  * 类：类是对现实生活中一类具有共同属性和行为的事物的抽象
  * 对象：是能够看得到摸的着的真实存在的实体
  * 简单理解：**类是对事物的一种描述，对象则为具体存在的事物**

```java
public class 类名 {
	// 成员变量
	变量1的数据类型 变量1；
	变量2的数据类型 变量2;
	…
	// 成员方法
	方法1;
	方法2;	
}
```

```java
/*手机类*/
public class Phone {
    //成员变量
    String brand;
    int price;

    //成员方法
    public void call() {
        System.out.println("打电话");
    }
	/*在对象里面设置方法，该方法成为该对象的一个属性*/
    public void sendMessage() {
        System.out.println("发短信");
    }
}
```

```java
/*学生类*/
/*假设文件名为Demo1.java，这个文件中假设有两个类Demo1类和Student类，代码如下*/
class Student{
    String name;
    double chinese;
    double math;
    public void printTotalScore(){
        System.out.println(name + "同学的各科总分是：" + (chinese + math));
    }
}
public class Demo1{
    Student s1 = new Student();
    s1.name = "LiHua";
    s1.chinese = 100;
    s1.math = 100;
    s1.printTotalScore();
}
/*有点类似C语言中的结构体*/
```

### 对象

```java
public class PhoneDemo {
    public static void main(String[] args) {
        //创建对象
        Phone p = new Phone();

        //使用成员变量
        System.out.println(p.brand);
        System.out.println(p.price);

        p.brand = "小米";
        p.price = 2999;

        System.out.println(p.brand);
        System.out.println(p.price);

        //使用成员方法
        p.call();
        p.sendMessage();
    }
}
```

### 面向对象三大特点之一：封装

1. 封装概述
   是面向对象三大特征之一（封装，继承，多态）

   **对象代表什么，就得封装对应的数据，并提供数据对应的行为** 

2. 封装代码实现
   将类的某些信息隐藏在类内部，不允许外部程序直接访问，而是通过该类提供的方法来实现对隐藏信息的操作和访问
   成员变量private，提供对应的getXxx()/setXxx()方法

#### private关键字

```java
/*
    学生类
 */
/*注意两个类是同级关系*/
class Student {
    //成员变量
    private String name;
    private int age;

    //get/set方法
    public void setName(String n) {
        name = n;
    }

    public String getName() {
        return name;
    }

    public void setAge(int a) {
        age = a;
    }

    public int getAge() {
        return age;
    }

    public void show() {
        System.out.println(name + "," + age);
    }
}
/*
    学生测试类
 */
/*一个代码文件中，可以写多个class类，但是只能有一个是public修饰，且public修饰的类必须和文件名相同。*/
public class StudentDemo {
    public static void main(String[] args) {
        //创建对象
        Student s = new Student();

        //使用set方法给成员变量赋值
        s.setName("林青霞");
        s.setAge(30);

        s.show();

        //使用get方法获取成员变量的值
        System.out.println(s.getName() + "---" + s.getAge());
        System.out.println(s.getName() + "," + s.getAge());

    }
}
```

```java
/*代码封装*/
/*private就好像把这个数据封锁，只能从类的内部访问，如果在外部访问需要通过该类里面的方法来调用*/
Student s1 = new Student();
s1.setScore(99);
/*s1.score = 99;*/
System.out.println(s1.getScore());
/*System.out.println(s1.score)*/
public class Student {
    private double score;
    public void setScore(double score) {
        if (score >=0 && score <=100) {
            this.score = score;
        }else{
            System.out.println("wrong");
        }
    }
    public  double getScore(){
        return score;
    }
}
```

#### this关键字

this修饰的变量用于指代成员变量，其主要作用是（区分局部变量和成员变量的重名问题）

**成员变量在类中方法外，而局部变量在方法中。**

* 方法的形参如果与成员变量同名，不带this修饰的变量指的是形参，而不是成员变量
* 方法的形参没有与成员变量同名，不带this修饰的变量指的是成员变量

```java
/*this关键字*/
/*哪一个对象调用方法方法中的this就是哪一个对象*/
Student s3 = new Student();
s3.score = 325;
s3.printPass(250);
public void printPass(double score) {
    if (this.score > score){
        /*this.score等效于s3.score*/
        System.out.println("you win");
    }else {
        System.out.println("you lose");
    }
}
```

```java
public class Student {
    private String name;
    private int age;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public int getAge() {
        return age;
    }

    public void show() {
        System.out.println(name + "," + age);
    }
}
```

#### 构造器

```java
/*构造器*/
/*在生成一个类时，如果我们不写构造器，Java会自动生成一个无参数构造器*/
/*一旦定义了有参数构造器，Java就不再提供空参数构造器，此时建议自己加一个无参数构造器*/
/*定义new对象就是在执行构造方法*/
Student s1 = new Student();
s1.name = "LiHua";
s1.score = "100";
Student s2 = new Student("HanMeiMei",59);
public class Student {
    String name;
    double score;
    //无参数构造器
    public Student() {
        System.out.println("无参数构造器被触发");
    }
    //有参数构造器
    public Student(String name,double score) {
        System.out.println("有参数构造器被触发");
        this.name = name;
        this.score = score;
    }
} 
```

```
/*
    学生类
 */
class Student {
    private String name;
    private int age;

    public Student() {}

    public Student(String name) {
        this.name = name;
    }

    public Student(int age) {
        this.age = age;
    }

    public Student(String name,int age) {
        this.name = name;
        this.age = age;
    }

    public void show() {
        System.out.println(name + "," + age);
    }
}
/*
    测试类
 */
public class StudentDemo {
    public static void main(String[] args) {
        //创建对象
        Student s1 = new Student();
        s1.show();

        //public Student(String name)
        Student s2 = new Student("林青霞");
        s2.show();

        //public Student(int age)
        Student s3 = new Student(30);
        s3.show();

        //public Student(String name,int age)
        Student s4 = new Student("林青霞",30);
        s4.show();
    }
}
```

#### 实体JavaBean

​	JavaBean实体类中除了有给对象存、取值的方法就没有提供其他方法了。所以实体类仅仅只是用来封装数据用的。
​	实体类要求：这个类中的成员变量都要私有，并且要对外提供相应的getxxx，setxxx方法，同时类中必须要有一个公共的无参的构造器。

## API(Application Programming Interface)应用程序编程接口

​	Java中的API指的就是 JDK 中提供的各种功能的 Java类，这些类将底层的实现封装了起来，我们不需要关心这些类是如何实现的，只需要学习这些类如何使用即可。

​	类似C++里的STL。

```java
/*建包的语法格式*/
package com.itheima.javabean;
public class 类名{
    //代码区
}
/*如果当前程序中，要调用自己所在包下的其他程序，可以直接调用。（同一个包下的类，互相可以直接调用）*/
/*如果当前程序中，要调用其他包下的程序，则必须在当前程序中导包, 才可以访问！*/
/*导包格式： import 包名.类名*/
/*如果当前程序中，要调用Java.lang包下的程序，不需要我们导包的，可以直接使用。*/
/*如果当前程序中，要调用多个不同包下的程序，而这些程序名正好一样，此时默认只能导入一个程序，另一个程序必须带包名访问。*/
```

### API帮助文档

自己上网查。

### String类

#### String类的创建


```java
/*法一，直接双引号得到字符串对象，封装字符串数据*/
/*只要字符序列相同(顺序和大小写)，无论在程序代码中出现几次，JVM 都只会建立一个 String 对象，并在字符串池中维护*/
/*此时字符串abc是存在字符串常量池中的。*/
/*先检查字符串常量池中有没有字符串abc，如果有，不会创建新的，而是直接复用。如果没有abc，才会创建一个新的。*/
/*所以，直接赋值的方式，代码简单，而且节约内存。*/
String ss1 = "abc";
String ss2 = "黑马程序员";
/*法二，new String创建字符串对象，并调用构造器初始化字符串*/
/*通过 new 创建的字符串对象，每一次 new 都会申请一个内存空间，虽然内容相同，但是地址值不同*/
/*看到new关键字，一定是在堆里面开辟了一个小空间。*/
/*rs2记录的是new出来的，在堆里面的地址值。*/
String rs1 = new String();
System.out.println(rs1); // ""，为空串
String rs2 = new String("itheima");
System.out.println(rs2);
/*法三，根据字符数组的内容，来创建字符串对象*/
char[] chars = {'a', '黑', '马'};
String rs3 = new String(chars);
System.out.println(rs3);
/*法四，根据字节数组的内容，来创建字符串对象*/
byte[] bytes = {97, 98, 99};
String rs4 = new String(bytes);
System.out.println(rs4);
```

#### String类的常用方法


```java
String rs5 = new String("wangxiaolei");
int length = rs5.length();
/*获取长度*/
char c = rs5.charAt(1);
/*提取字符串中某个索引位置处的字符*/
/*应用：遍历字符串，桶计算统计字符次数*/
//'0' --->  48


String s1 = new String("黑马");
String s2 = new String("黑马");
System.out.println(s1 == s2); // false
/* 比较基本数据类型：比较的是具体的值*/
/* 比较引用数据类型：比较的是对象地址值*/
/*结论：==只能用于比较基本数据类型。不能比较引用数据类型。*/
System.out.println(s1.equals(s2)); // true
/*判断字符串内容，内容一样就返回true*/
/*应用：用户登录页面*/


String c1 = "34AeFG";
String c2 = "34aEfg";
System.out.println(c1.equals(c2)); // false
System.out.println(c1.equalsIgnoreCase(c2)); // true
/*忽略大小写比较字符串内容*/


String s3 = "Java是最好的编程语言之一";
String rs = s3.substring(0, 8);//从索引为0到索引为7
String rs1 = s3.substring(7);//从索引为7到最后
System.out.println(rs);
System.out.println(rs1);
/*截取字符串内容 (包前不包后的),切片*/
/*应用：手机号屏蔽*/
String rs2 = s3.substring(5);
System.out.println(rs2);
/*从当前索引位置一直截取到字符串的末尾*/


String info = "这个电影简直是个垃圾，垃圾电影！！";
String rs3 = info.replace("垃圾", "**");
System.out.println(rs3);
/*把字符串中的某个内容替换成新内容，并返回新的字符串对象给我们*/
/*应用：敏感词替换，身份证信息查看*/



String info2 = "Java是最好的编程语言之一，我爱Java,Java不爱我！";
System.out.println(info2.contains("Java"));
System.out.println(info2.contains("java"));
System.out.println(info2.contains("Java2"));
/*判断字符串中是否包含某个关键字*/
/*拓展：多个敏感词替换*/
public class Test10多个敏感词替换 {
    public static void main(String[] args) {
        //实际开发中，敏感词会有很多很多
        //1.先键盘录入要说的话
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入要说的话");
        String talk = sc.next();//后裔你玩什么啊，TMD,GDX,ctmd,ZZ
        //2.定义一个数组用来存多个敏感词
        String[] arr = {"TMD","GDX","ctmd","ZZ","lj","FW","nt"};
        //3.把说的话中所有的敏感词都替换为***
        for (int i = 0; i < arr.length; i++) {
            //i 索引
            //arr[i] 元素 --- 敏感词
            talk = talk.replace(arr[i],"***");
        }
        //4.打印结果
        System.out.println(talk);//后裔你玩什么啊，***,***,***,***
    }
}


String rs4 = "张三丰";
System.out.println(rs4.startsWith("张"));
System.out.println(rs4.startsWith("张三"));
System.out.println(rs4.startsWith("张三2"));
/*判断字符串是否以某个字符串开头。*/


String rs5 = "张无忌,周芷若,殷素素,赵敏";
String[] names = rs5.split(",");
for (int i = 0; i < names.length; i++) {
    System.out.println(names[i]);
}
/*把字符串按照某个指定内容分割成多个字符串，放到一个字符串数组中返回给我们*/
```

#### String类的注意事项

- 字符串不可变，它们的值在创建后不能被更改
- 虽然 String 的值是不可变的，但是它们可以被共享
- 字符串效果上相当于字符数组( char[] )，但是底层原理是字节数组( byte[] )

### StringBuilder

StringBuilder 可以看成是一个容器，创建之后里面的内容是可变的。

当我们在拼接字符串和反转字符串的时候会使用到

#### 字符串的反转

```java
public class StringBuilderDemo3 {
    public static void main(String[] args) {
        //1.创建对象
        StringBuilder sb = new StringBuilder("abc");

        //2.添加元素
        /*sb.append(1);
        sb.append(2.3);
        sb.append(true);*/

        //反转
        sb.reverse();

        //获取长度
        int len = sb.length();
        System.out.println(len);


        //打印
        //普及：
        //因为StringBuilder是Java已经写好的类
        //java在底层对他做了一些特殊处理。
        //打印对象不是地址值而是属性值。
        System.out.println(sb);
    }
}

/*例：对称字符串*/
public class StringBuilderDemo6 {
    //使用StringBuilder的场景：
    //1.字符串的拼接
    //2.字符串的反转

    public static void main(String[] args) {
        //1.键盘录入一个字符串
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入一个字符串");
        String str = sc.next();

        //2.反转键盘录入的字符串
        String result = new StringBuilder().append(str).reverse().toString();

        //3.比较
        if(str.equals(result)){
            System.out.println("当前字符串是对称字符串");
        }else{
            System.out.println("当前字符串不是对称字符串");
        }

    }
}
```

#### 字符串的拼接

```java
package com.itheima.stringbuilderdemo;

public class StringBuilderDemo7 {
    public static void main(String[] args) {
        //1.定义数组
        int[] arr = {1,2,3};

        //2.调用方法把数组变成字符串
        String str = arrToString(arr);

        System.out.println(str);

    }


    public static String arrToString(int[] arr){
        StringBuilder sb = new StringBuilder();
        sb.append("[");

        for (int i = 0; i < arr.length; i++) {
            if(i == arr.length - 1){
                sb.append(arr[i]);
            }else{
                sb.append(arr[i]).append(", ");
            }
        }
        sb.append("]");

        return sb.toString();
    }
}
```

#### 链式编程

```java
public class StringBuilderDemo4 {
    public static void main(String[] args) {
        //1.创建对象
        StringBuilder sb = new StringBuilder();

        //2.添加字符串
        sb.append("aaa").append("bbb").append("ccc").append("ddd");

        System.out.println(sb);//aaabbbcccddd

        //3.再把StringBuilder变回字符串
        String str = sb.toString();
        System.out.println(str);//aaabbbcccddd

    }
}
```

### StringJoiner

* StringJoiner跟StringBuilder一样，也可以看成是一个容器，创建之后里面的内容是可变的。
* 作用：提高字符串的操作效率，而且代码编写特别简洁，但是目前市场上很少有人用。 
* JDK8出现的

```java
/*基本使用*/
//1.创建一个对象，并指定中间的间隔符号
StringJoiner sj = new StringJoiner("---");
//2.添加元素
sj.add("aaa").add("bbb").add("ccc");
//3.打印结果
System.out.println(sj);//aaa---bbb---ccc

//1.创建对象
StringJoiner sj = new StringJoiner(", ","[","]");
//2.添加元素
sj.add("aaa").add("bbb").add("ccc");
int len = sj.length();
System.out.println(len);//15
//3.打印
System.out.println(sj);//[aaa, bbb, ccc]
String str = sj.toString();
System.out.println(str);//[aaa, bbb, ccc]
```

### 关于字符串的小扩展

1. 字符串存储的内存原理

   String s = “abc”；直接赋值

   特点：

   ​	此时字符串abc是存在字符串常量池中的。

   ​	先检查字符串常量池中有没有字符串abc，如果有，不会创建新的，而是直接复用。如果没有abc，才会创建一个新的。

   所以，直接赋值的方式，代码简单，而且节约内存。

2. new出来的字符串

   看到new关键字，一定是在堆里面开辟了一个小空间。

   String s1 = new String（“abc”）；

   String s2 = “abc”；

   s1记录的是new出来的，在堆里面的地址值。

   s2是直接赋值的，所以记录的是字符串常量池中的地址值。

3. ==号比较的到底是什么？

   如果比较的是基本数据类型：比的是具体的数值是否相等。

   如果比较的是引用数据类型：比的是地址值是否相等。

   结论：==只能用于比较基本数据类型。不能比较引用数据类型。

## ArrayList集合

### 概述

集合提供一种存储空间可变的存储模型，存储的容量可以发生改变

长度可以变化，但只能存储引用数据类型

使用泛型用于约束集合中存储元素的数据类型

添加数据的时候不需要考虑索引，默认将数据添加到末尾

### 常用方法

| 方法名                                | 说明                                   |
| ------------------------------------- | -------------------------------------- |
| public ArrayList()                    | 创建一个空的集合对象                   |
| public boolean add(要添加的元素)      | 将指定的元素追加到此集合的末尾         |
| public boolean remove(要删除的元素)   | 删除指定元素,返回值表示是否删除成功    |
| public E  remove(int   index)         | 删除指定索引处的元素，返回被删除的元素 |
| public E   set(int index,E   element) | 修改指定索引处的元素，返回被修改的元素 |
| public E   get(int   index)           | 返回指定索引处的元素                   |
| public int   size()                   | 返回集合中的元素的个数                 |

```java
public class ArrayListDemo02 {
    public static void main(String[] args) {
        //创建集合
        ArrayList<String> array = new ArrayList<String>();

        //添加元素
        array.add("hello");
        array.add("world");
        array.add("java");

        //public boolean remove(Object o)：删除指定的元素，返回删除是否成功
        //        System.out.println(array.remove("world"));
        //        System.out.println(array.remove("javaee"));

        //public E remove(int index)：删除指定索引处的元素，返回被删除的元素
        //        System.out.println(array.remove(1));

        //IndexOutOfBoundsException
        //        System.out.println(array.remove(3));

        //public E set(int index,E element)：修改指定索引处的元素，返回被修改的元素
        //        System.out.println(array.set(1,"javaee"));

        //IndexOutOfBoundsException
        //        System.out.println(array.set(3,"javaee"));

        //public E get(int index)：返回指定索引处的元素
        //        System.out.println(array.get(0));
        //        System.out.println(array.get(1));
        //        System.out.println(array.get(2));
        //System.out.println(array.get(3)); //？？？？？？ 自己测试

        //public int size()：返回集合中的元素的个数
        System.out.println(array.size());

        //输出集合
        System.out.println("array:" + array);
    }
}
```

### 实战：ArrayList存储字符串/对象并遍历

```java
public class ArrayListDemo4 {
    public static void main(String[] args) {
        //1.创建集合对象，用来存储数据
        ArrayList<Student> list = new ArrayList<>();

        //2.创建学生对象
        Student s1 = new Student("zhangsan",16);
        Student s2 = new Student("lisi",15);
        Student s3 = new Student("wangwu",18);

        //3.把学生对象添加到集合中
        list.add(s1);
        list.add(s2);
        list.add(s3);

        //4.遍历
        for (int i = 0; i < list.size(); i++) {
            //i 依次表示集合中的每一个索引
            Student stu = list.get(i);
            System.out.println(stu.getName() + ", " + stu.getAge());
        }



    }
}
```

```java
public class ArrayListDemo3 {
    public static void main(String[] args) {
        //1.创建集合对象
        ArrayList<String> list = new ArrayList<>();

        //2.添加元素
        list.add("aaa");
        list.add("bbb");
        list.add("ccc");
        list.add("ddd");

        //3.遍历
        //快捷键: list.fori 正向遍历
        //list.forr 倒着遍历
        System.out.print("[");
        for (int i = 0; i < list.size(); i++) {
            //i 依次表示集合里面的每一个索引

            if(i == list.size() - 1){
                //最大索引
                System.out.print(list.get(i));
            }else{
                //非最大索引
                System.out.print(list.get(i) + ", ");
            }
        }
        System.out.print("]");
    }
}
```

### 实战：查找用户索引

```java
public class ArrayListDemo6 {
    public static void main(String[] args) {
        /*需求：
        1，main方法中定义一个集合，存入三个用户对象。
        用户属性为：id，username，password
        2，要求：定义一个方法，根据id查找对应的学生信息。
        如果存在，返回索引
        如果不存在，返回-1*/


        //1.创建集合对象
        ArrayList<User> list = new ArrayList<>();

        //2.创建用户对象
        User u1 = new User("heima001", "zhangsan", "123456");
        User u2 = new User("heima002", "lisi", "1234");
        User u3 = new User("heima003", "wangwu", "1234qwer");

        //3.把用户对象添加到集合当中
        list.add(u1);
        list.add(u2);
        list.add(u3);

        //4.调用方法，通过id获取对应的索引
        int index = getIndex(list, "heima001");

        System.out.println(index);

    }


    //1.我要干嘛？  根据id查找对应的学生信息
    //2.我干这件事情需要什么才能完成？   集合 id
    //3.方法的调用处是否需要继续使用方法的结果？
    //要用必须返回，不要用可以返回也可以不返回
    //明确说明需要有返回值 int
    public static int getIndex(ArrayList<User> list, String id) {
        //遍历集合得到每一个元素
        for (int i = 0; i < list.size(); i++) {
            User u = list.get(i);
            String uid = u.getId();
            if(uid.equals(id)){
                return i;
            }
        }
        //因为只有当集合里面所有的元素都比较完了，才能断定id是不存在的。
        return -1;
    }
}
```

### 实战：判断数据的存在性

```java
public class ArrayListDemo5 {
    public static void main(String[] args) {
       /* 需求：
        1，main方法中定义一个集合，存入三个用户对象。
        用户属性为：id，username，password
        2，要求：定义一个方法，根据id查找对应的学生信息。
        如果存在，返回true
        如果不存在，返回false*/

        //1.定义集合
        ArrayList<User> list = new ArrayList<>();

        //2.创建对象
        User u1 = new User("heima001","zhangsan","123456");
        User u2 = new User("heima002","lisi","12345678");
        User u3 = new User("heima003","wangwu","1234qwer");

        //3.把用户对象添加到集合当中
        list.add(u1);
        list.add(u2);
        list.add(u3);

        //4.调用方法，查询id是否存在
        boolean result = contains(list, "heima001");
        System.out.println(result);

    }

    //定义在测试类中的方法需要加static
    //1.我要干嘛？ 我要根据id查询学生是否存在
    //2.我干这件事情，需要什么才能完成？ 集合 id
    //3.方法的调用处是否需要使用方法的结果？
    //如果要用，必须返回，如果不用，可以返回也可以不返回
    //但是本题明确说明需要返回
    public static boolean contains(ArrayList<User> list, String id){
        //循环遍历集合，得到集合里面的每一个元素
        //再进行判断

        for (int i = 0; i < list.size(); i++) {
            //i 索引  list.get(i); 元素
            User u = list.get(i);
            //判断id是否存在，我是拿着谁跟谁比较
            //需要把用户对象里面的id拿出来再进行比较。
            String uid = u.getId();
            if(id.equals(uid)){
                return true;//return 关键字：作用就是结束方法。
            }
        }
        //只有当集合里面所有的元素全部比较完毕才能认为是不存在的。
        return false;
    }

}

```

## 面向对象进阶1

学习目标：

- [ ] 能够掌握static关键字修饰的变量调用方式
- [ ] 能够掌握static关键字修饰的方法调用方式
- [ ] 知道静态代码块的格式和应用场景

- [ ] 能够写出类的继承格式
- [ ] 能够说出继承的特点
- [ ] 能够区分this和super的作用
- [ ] 能够说出方法重写的概念
- [ ] 能够说出方法重写的注意事项

### static关键字

static是静态的意思。 static可以修饰成员变量或者修饰方法。

```java
public class Student {
    public static String schoolName = "传智播客"； // 属于类，只有一份。
    public static void study(){
    	System.out.println("我们都在黑马程序员学习");   
    }
}
public static void  main(String[] args){
    System.out.println(Student.schoolName); // 传智播客
    Student.schoolName = "黑马程序员";
    System.out.println(Student.schoolName); // 黑马程序员
    Student.study();//我们都在黑马程序员学习
}
```

### 静态变量

由static修饰的变量称为静态变量。

静态变量可以被类里所有的对象共享使用，这个静态成员变量在内存区域中也只存在一份。

使用时只需要用类名访问。

注意点：

1. 任何对象都可以更改该静态变量的值或者访问静态方法。但是不推荐这种方式去访问。因为静态变量或者静态方法直接通过类名访问即可，完全没有必要用对象去访问。
2. static修饰的成员属于类，会存储在静态区，是随着类的加载而加载的，且只加载一次，所以只有一份，节省内存。

### 实例变量

无static修饰的成员方法属于每个对象的，这个成员方法也叫做**实例方法**。

实例方法是属于每个对象，必须创建类的对象才可以访问。  

```java
public class Student {
    // 实例变量
    private String name ;
    // 2.方法：行为
    // 无 static修饰，实例方法。属于每个对象，必须创建对象调用
    public void run(){
        System.out.println("学生可以跑步");
    }
	// 无 static修饰，实例方法
    public  void sleep(){
        System.out.println("学生睡觉");
    }
    public static void study(){
        
    }
}
public static void main(String[] args){
    // 创建对象 
    Student stu = new Student ;
    stu.name = "徐干";
    // Student.sleep();// 报错，必须用对象访问。
    stu.sleep();
    stu.run();
}
```

### 面向对象三大特点之二：继承

假如多个类中存在相同属性和行为时，我们可以将这些内容抽取到单独一个类中，那么多个类无需再定义这些属性和行为，只要**继承**那一个类即可。

其中，多个类可以称为**子类**，单独被继承的那一个类称为**父类**、**超类（superclass）**或者**基类**。

![1](C:\Users\Lenovo\Desktop\Notes\assets_java\1.jpg)

核心：子类继承父类的**属性**和**行为**，使得子类对象可以直接具有与父类相同的属性、相同的行为。子类可以直接访问父类中的**非私有**的属性和行为。

好处：提高**代码的复用性**（减少代码冗余，相同代码重复利用），使类与类之间产生了关系。

```
class 父类 {
	...
}

class 子类 extends 父类 {
	...
}
```

#### 实例

请使用继承定义以下类:

1. 学生类
   属性:姓名，年龄
   行为:吃饭，睡觉
2. 老师类
   属性:姓名，年龄，薪水
   行为:吃饭，睡觉，教书
3. 班主任
   属性:姓名,年龄，薪水
   行为:吃饭，睡觉，管理

![360截图20181202211331250](C:\Users\Lenovo\Desktop\Notes\assets_java\360截图20181202211331250.jpg)

```java
 /*父类Human类*/
 public class Human {
    // 合理隐藏
    private String name ;
    private int age ;
	
    // 合理暴露
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
 }
 
 /*子类Teacher类*/
 public class Teacher extends Human {
    // 工资
    private double salary ;
    
    // 特有方法
    public void teach(){
        System.out.println("老师在认真教技术！")；
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }
}

/*子类Student类*/
public class Student extends Human{
 
}

/*子类BanZhuren类*/
public class Teacher extends Human {
    // 工资
    private double salary ;
    
       // 特有方法
    public void admin(){
        System.out.println("班主任强调纪律问题！")；
    }
    
    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }
}

/*测试类*/
public class Test {
  public static void main(String[] args) {
      Teacher dlei = new Teacher();
      dlei.setName("播仔");
      dlei.setAge("31");
      dlei.setSalary(1000.99);
      System.out.println(dlei.getName());
      System.out.println(dlei.getAge());
      System.out.println(dlei.getSalary());
      dlei.teach();

      BanZhuRen linTao = new BanZhuRen();
      linTao.setName("灵涛");
      linTao.setAge("28");
      linTao.setSalary(1000.99);
      System.out.println(linTao.getName());
      System.out.println(linTao.getAge());
      System.out.println(linTao.getSalary());
      linTao.admin();

      Student xugan = new Student();
      xugan.setName("播仔");
      xugan.setAge("31");
      //xugan.setSalary(1000.99); // xugan没有薪水属性，报错！
      System.out.println(xugan.getName());
      System.out.println(xugan.getAge());
  }
}
```

#### 注意点

并不是父类的所有内容都可以给子类继承的。

**子类不能继承父类的构造方法。（私有or公有）**

如果父级使用了私有成员（变量和方法），对于私有变量，子类无法直接访问但是可以通过get和set来访问，而私有方法无法访问。

```java
public class Demo03 {
    public static void main(String[] args) {
        Zi z = new Zi();
        System.out.println(z.num1);
//		System.out.println(z.num2); // 私有的子类无法使用
        // 通过getter/setter方法访问父类的private成员变量
        System.out.println(z.getNum2());

        z.show1();
        // z.show2(); // 私有的子类无法使用
    }
}

class Fu {
    public int num1 = 10;
    private int num2 = 20;

    public void show1() {
        System.out.println("show1");
    }

    private void show2() {
        System.out.println("show2");
    }

    public int getNum2() {
        return num2;
    }

    public void setNum2(int num2) {
        this.num2 = num2;
    }
}

class Zi extends Fu {
}
```

#### 发生继承时的特点

1. 子父类中出现了同名的成员变量时，子类会优先访问自己对象中的成员变量

   ```java
   class Fu1 {
   	// Fu中的成员变量。
   	int num = 5;
   }
   class Zi1 extends Fu1 {
   	// Zi中的成员变量
   	int num = 6;
       //int num2 = 6;
     
   	public void show() {
   		// 访问父类中的num
   		System.out.println("Fu num=" + num);
   		// 访问子类中的num
   		System.out.println("Zi num=" + num);
           // 访问子类中的num2
   		System.out.println("Zi num2="+num2);
   	}
   }
   class Demo04 {
   	public static void main(String[] args) {
         	// 创建子类对象
   		Zi1 z = new Zi1(); 
         	// 调用子类中的show方法
   		z1.show(); 
   	}
   }
   演示结果：
   Fu num = 6
   Zi num = 6
   ```

   ```java
   /*用super解决问题*/
   class Fu {
   	// Fu中的成员变量。
   	int num = 5;
   }
   
   class Zi extends Fu {
   	// Zi中的成员变量
   	int num = 6;
     
   	public void show() {
           int num = 1;
         
           // 访问方法中的num
           System.out.println("method num=" + num);
           // 访问子类中的num
           System.out.println("Zi num=" + this.num);
           // 访问父类中的num
           System.out.println("Fu num=" + super.num);
   	}
   }
   
   class Demo04 {
   	public static void main(String[] args) {
         	// 创建子类对象
   		Zi1 z = new Zi1(); 
         	// 调用子类中的show方法
   		z1.show(); 
   	}
   }
   
   演示结果：
   method num=1
   Zi num=6
   Fu num=5
   ```

2. 子类父类中出现**重名**的成员方法，则创建子类对象调用该方法的时候，子类对象会优先调用自己的方法。

   ```java
   class Fu {
   	public void show() {
   		System.out.println("Fu show");
   	}
   }
   class Zi extends Fu {
   	//子类重写了父类的show方法
   	public void show() {
   		System.out.println("Zi show");
   	}
   }
   public class ExtendsDemo05{
   	public static void main(String[] args) {
   		Zi z = new Zi();
        	// 子类中有show方法，只执行重写后的show方法
   		z.show();  // Zi show
   	}
   }
   ```

   ```java
   /*方法重写*/
   /*子类中出现与父类一模一样的方法时（返回值类型，方法名和参数列表都相同），会出现覆盖效果，也称为重写或者复写。*/
   /*子类方法覆盖父类方法，必须要保证权限大于等于父类权限，且返回值类型、函数名和参数列表都要一模一样。*/
   
   /*我们定义了一个动物类代码*/
   public class Animal  {
       public void run(){
           System.out.println("动物跑的很快！");
       }
       public void cry(){
           System.out.println("动物都可以叫~~~");
       }
   }
   
   /*然后定义一个猫类，猫可能认为父类cry()方法不能满足自己的需求*/
   public class Cat extends Animal {
       @Override  //相当于是方法重写的一种注解，提示代码阅读者后面的代码是方法重写。
       //建议重写都加上这句代码，可以提高代码的可读性。如果后面的方法不是方法重写的话就会报错哦。
       public void cry(){
           System.out.println("我们一起学猫叫，喵喵喵！喵的非常好听！");
       }
   }
   
   public class Test {
   	public static void main(String[] args) {
         	// 创建子类对象
         	Cat ddm = new Cat()；
           // 调用父类继承而来的方法
           ddm.run();
         	// 调用子类重写的方法
         	ddm.cry();
   	}
   }
   ```

3. **继承后子类构方法器特点:子类所有构造方法的第一行都会默认先调用父类的无参构造方法。**

   ```java
   class Person {
       private String name;
       private int age;
   
       public Person() {
           System.out.println("父类无参");
       }
   
       // getter/setter省略
   }
   
   class Student extends Person {
       private double score;
   
       public Student() {
           //super(); // 调用父类无参,默认就存在，可以不写，必须再第一行
           System.out.println("子类无参");
       }
       
        public Student(double score) {
           //super();  // 调用父类无参,默认就存在，可以不写，必须再第一行
           this.score = score;    
           System.out.println("子类有参");
        }
   
   }
   
   public class Demo07 {
       public static void main(String[] args) {
           Student s1 = new Student();
           System.out.println("----------");
           Student s2 = new Student(99.9);
       }
   }
   
   输出结果：
   父类无参
   子类无参
   ----------
   父类无参
   子类有参
       
   /*原因：子类是无法继承父类构造方法的，因为构造方法的名字是与类名一致的。而构造方法的作用是初始化对象成员变量数据的。所以子类的初始化过程中，必须先执行父类的初始化动作。子类的构造方法中默认有一个super()，表示调用父类的构造方法，父类成员变量初始化后，才可以给子类使用。（先有爸爸，才能有儿子）*/
   ```

#### super（）和this（）

```
super(...) -- 调用父类的构造方法，根据参数匹配确认
this(...) -- 调用本类的其他构造方法，根据参数匹配确认
```

```java
class Person {
    private String name ="凤姐";
    private int age = 20;

    public Person() {
        System.out.println("父类无参");
    }
    
    public Person(String name , int age){
        this.name = name ;
        this.age = age ;
    }

    // getter/setter省略
}

class Student extends Person {
    private double score = 100;

    public Student() {
        //super(); // 调用父类无参构造方法,默认就存在，可以不写，必须再第一行
        System.out.println("子类无参");
    }
    
     public Student(String name ， int age，double score) {
        super(name ,age);// 调用父类有参构造方法Person(String name , int age)初始化name和age
        this.score = score;    
        System.out.println("子类有参");
     }
      // getter/setter省略
}

public class Demo07 {
    public static void main(String[] args) {
        // 调用子类有参数构造方法
        Student s2 = new Student("张三"，20，99);
        System.out.println(s2.getScore()); // 99
        System.out.println(s2.getName()); // 输出 张三
        System.out.println(s2.getAge()); // 输出 20
    }
}
```

**注意：**

**子类的每个构造方法中均有默认的super()，调用父类的空参构造。手动调用父类构造会覆盖默认的super()。**

**super() 和 this() 都必须是在构造方法的第一行，所以不能同时出现。**

super(..)是根据参数去确定调用父类哪个构造方法的。

![2](C:\Users\Lenovo\Desktop\Notes\assets_java\2.jpg)

```
package com.itheima._08this和super调用构造方法;
/**
 * this(...):
 *    默认是去找本类中的其他构造方法，根据参数来确定具体调用哪一个构造方法。
 *    为了借用其他构造方法的功能。
 *
 */
public class ThisDemo01 {
    public static void main(String[] args) {
        Student xuGan = new Student();
        System.out.println(xuGan.getName()); // 输出:徐干
        System.out.println(xuGan.getAge());// 输出:21
        System.out.println(xuGan.getSex());// 输出： 男
    }
}

class Student{
    private String name ;
    private int age ;
    private char sex ;

    public Student() {
  // 很弱，我的兄弟很牛逼啊，我可以调用其他构造方法：Student(String name, int age, char sex)
        this("徐干",21,'男');
    }

    public Student(String name, int age, char sex) {
        this.name = name ;
        this.age = age   ;
        this.sex = sex   ;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public char getSex() {
        return sex;
    }

    public void setSex(char sex) {
        this.sex = sex;
    }
}
```

注意：

this（）默认是去找本类中的其他构造方法，根据参数来确定具体调用哪一个构造方法。目的是为了借用其他构造方法的功能。

#### 继承特点

Java只支持单继承，不支持多继承。

```java
// 一个类只能有一个父类，不可以有多个父类。
class A {}
class B {}
class C1 extends A {} // ok
// class C2 extends A, B {} // error
```

一个类可以有多个子类。

```java
// A可以有多个子类
class A {}
class C1 extends A {}
class C2 extends  A {}
```

可以多层继承。

```java
class A {}
class C1 extends A {}
class D extends C1 {}
/*顶层父类是Object类。所有的类默认继承Object，作为父类。*/
```

## 面向对象进阶2

学习目标：

- [ ] 能够说出使用多态的前提条件
- [ ] 理解多态的向上转型
- [ ] 理解多态的向下转型
- [ ] 能够知道多态的使用场景

- [ ] 包的作用
- [ ] public和private权限修饰符的作用
- [ ] 描述final修饰的类的特点
- [ ] 描述final修饰的方法的特点
- [ ] 描述final修饰的变量的特点

### 面向对象三大特点之三：多态

**多态是出现在继承或者实现关系中的**。

有了多态之后，方法的形参就可以定义为共同的父类Person。

**要注意的是：**

* 当一个方法的形参是一个类，我们可以传递这个类所有的子类对象。
* 当一个方法的形参是一个接口，我们可以传递这个接口所有的实现类对象（后面会学）。
* 而且多态还可以根据传递的不同对象来调用不同类中的方法。

```java
父类：
public class Person {
    private String name;
    private int age;

    空参构造
    带全部参数的构造
    get和set方法

    public void show(){
        System.out.println(name + ", " + age);
    }
}

子类1：
public class Administrator extends Person {
    @Override
    public void show() {
        System.out.println("管理员的信息为：" + getName() + ", " + getAge());
    }
}

子类2：
public class Student extends Person{

    @Override
    public void show() {
        System.out.println("学生的信息为：" + getName() + ", " + getAge());
    }
}

子类3：
public class Teacher extends Person{

    @Override
    public void show() {
        System.out.println("老师的信息为：" + getName() + ", " + getAge());
    }
}

测试类：
public class Test {
    public static void main(String[] args) {
        //创建三个对象，并调用register方法

        Student s = new Student();
        s.setName("张三");
        s.setAge(18);


        Teacher t = new Teacher();
        t.setName("王建国");
        t.setAge(30);

        Administrator admin = new Administrator();
        admin.setName("管理员");
        admin.setAge(35);



        register(s);
        register(t);
        register(admin);


    }



    //这个方法既能接收老师，又能接收学生，还能接收管理员
    //只能把参数写成这三个类型的父类
    public static void register(Person p){
        p.show();
    }
}
```

### 多态的运行特点

多态体现的格式：

```java
父类类型 变量名 = new 子类/实现类构造器;
变量名.方法名();
```

多态的前提：

```
1. 有继承或者实现关系
2. 方法的重写【意义体现：不重写，无意义】
3. 父类引用指向子类对象【格式体现】
```

多态的运行特点：

调用成员变量时：编译看左边，运行看左边

调用成员方法时：编译看左边，运行看右边

```java
Fu f = new Zi()；
//编译看左边的父类中有没有name这个属性，没有就报错
//在实际运行的时候，把父类name属性的值打印出来
System.out.println(f.name);
//编译看左边的父类中有没有show这个方法，没有就报错
//在实际运行的时候，运行的是子类中的show方法
f.show();
```

特例：如果子类有些独有的功能，此时**多态的写法就无法访问子类独有功能了**。

```
class Animal{
    public  void eat()｛
        System.out.println("动物吃东西！")
    ｝
}
class Cat extends Animal {  
    public void eat() {  
        System.out.println("吃鱼");  
    }  
   
    public void catchMouse() {  
        System.out.println("抓老鼠");  
    }  
}  

class Dog extends Animal {  
    public void eat() {  
        System.out.println("吃骨头");  
    }  
}

class Test{
    public static void main(String[] args){
        Animal a = new Cat();
        a.eat();
        a.catchMouse();//编译报错，编译看左边，Animal没有这个方法
    }
}
```

### 引用类型转换

为了解决这个问题（想要调用子类特有的方法），必须做向下转型。

应用类型转换分为向上转型（自动转换）和向下转型（强制转换）

有点类似数据的类型转换：

- 自动转换: 范围小的赋值给范围大的.自动完成:double d = 5; 
- 强制转换: 范围大的赋值给范围小的,强制转换:int i = (int)3.14 

#### 向上转型（自动转换）

多态本身是子类类型向父类类型向上转换（自动转换）的过程，这个过程是默认的。
当父类引用指向一个子类对象时，便是向上转型。

```
父类类型  变量名 = new 子类类型();
如：Animal a = new Cat();
```

父类类型相对与子类来说是大范围的类型，Animal是动物类，是父类类型。Cat是猫类，是子类类型。Animal类型的范围当然很大，包含一切动物。**所以子类范围小可以直接自动转型给父类类型的变量。

#### 向下转型（强制转换）

一个已经向上转型的子类对象，将父类引用转为子类引用，可以使用强制类型转换的格式，便是向下转型。

```
子类类型 变量名 = (子类类型) 父类变量名;
如:Aniaml a = new Cat();
   Cat c =(Cat) a;  
```

#### 综合演示

```java
abstract class Animal {  
    abstract void eat();  
}  

class Cat extends Animal {  
    public void eat() {  
        System.out.println("吃鱼");  
    }  
    public void catchMouse() {  
        System.out.println("抓老鼠");  
    }  
}  

class Dog extends Animal {  
    public void eat() {  
        System.out.println("吃骨头");  
    }  
    public void watchHouse() {  
        System.out.println("看家");  
    }  
}

public class Test {
    public static void main(String[] args) {
        // 向上转型  
        Animal a = new Cat();  
        a.eat(); 				// 调用的是 Cat 的 eat

        // 向下转型  
        Cat c = (Cat) a;       
        c.catchMouse(); 		// 调用的是 Cat 的 catchMouse
        
        //错误示范
        //Dog d = (Dog)a;       
        //d.watchHouse();        // 调用的是 Dog 的 watchHouse 【运行报错】
        //这段代码可以通过编译，但是运行时，却报出了 `ClassCastException` ，类型转换异常！这是因为，明明创建了Cat类型对象，运行时，当然不能转换成Dog对象的。
    }  
}
```

### instanceof关键字

为了避免ClassCastException的发生，Java提供了 `instanceof` 关键字，给引用变量做类型的校验，格式如下：

```
变量名 instanceof 数据类型 
如果变量属于该数据类型或者其子类类型，返回true。
如果变量不属于该数据类型或者其子类类型，返回false。
```

所以，转换前，我们最好先做一个判断，代码如下：

```java
public class Test {
    public static void main(String[] args) {
        // 向上转型  
        Animal a = new Cat();  
        a.eat();               // 调用的是 Cat 的 eat

        // 向下转型  
        if (a instanceof Cat){
            Cat c = (Cat)a;       
            c.catchMouse();        // 调用的是 Cat 的 catchMouse
        
        
        //JDK14的新特性，判断和强转合并成了一行
        //if (a instanceof Cat c){
        //    c.catchMouse(); 
        //}
            
        else if (a instanceof Dog){
            Dog d = (Dog)a;       
            d.watchHouse();       // 调用的是 Dog 的 watchHouse
        }
    }  
}
```

### 包

包在操作系统中其实就是一个文件夹。**包是用来分门别类的管理技术，不同的技术类放在不同的包下**，方便管理和维护。

**包名的命名规范**：

```
路径名.路径名.xxx.xxx
// 例如：com.itheima.oa
```

- 包名一般是公司域名的倒写。例如：黑马是www.itheima.com,包名就可以定义成com.itheima.技术名称。
- 包名必须用”.“连接。
- 包名的每个路径名必须是一个合法的标识符，而且不能是Java的关键字。

#### 导包

什么时候需要导包？

​	情况一：在使用Java中提供的非核心包中的类时

​	情况二：使用自己写的其他包中的类时

什么时候不需要导包？

​	情况一：在使用Java核心包（java.lang）中的类时

​	情况二：在使用自己写的同一个包中的类时

#### 使用不同包下的相同类怎么办？

```java
//使用全类名的形式即可。
//全类名：包名 + 类名
//拷贝全类名的快捷键：选中类名crtl + shift + alt + c 或者用鼠标点copy，再点击copy Reference
com.itheima.homework.demo1.Student s1 = new com.itheima.homework.demo1.Student();
com.itheima.homework.demo2.Student s2 = new com.itheima.homework.demo2.Student();
```

### 权限修饰符

在Java中提供了四种访问权限，使用不同的访问权限修饰符修饰时，被修饰的内容会有不同的访问权限。

|                  | public | protected | 默认（不加权限修饰符） | private |
| :--------------: | :----: | :-------: | :--------------------: | :-----: |
|     同一类中     |   √    |     √     |           √            |    √    |
|   同一包中的类   |   √    |     √     |           √            |         |
|   不同包的子类   |   √    |     √     |                        |         |
| 不同包中的无关类 |   √    |           |                        |         |

编写代码时，如果没有特殊的考虑，建议这样使用权限：

- 成员变量使用`private` ，隐藏细节。
- 构造方法使用` public` ，方便创建对象。
- 成员方法使用`public` ，方便调用方法。

### final关键字

> 被final修饰的常量名称，一般都有书写规范，所有字母都**大写**。

规则一：final修饰的类，不能被继承。

```java
final class Fu {
}
// class Zi extends Fu {} // 报错,不能继承final的类
```

查询API发现像 `public final class String` 、`public final class Math` 、`public final class Scanner` 等，很多我们学习过的类，都是被final修饰的，目的就是供我们使用，而不让我们所以改变其内容。

规则二：final修饰的方法，不能被重写。

```java
class Fu2 {
	final public void show1() {
		System.out.println("Fu2 show1");
	}
	public void show2() {
		System.out.println("Fu2 show2");
	}
}

class Zi2 extends Fu2 {
//	@Override
//	public void show1() {
//		System.out.println("Zi2 show1");
//	}
	@Override
	public void show2() {
		System.out.println("Zi2 show2");
	}
}
```

规则三：基本类型的局部变量，被final修饰后，只能赋值一次，不能再更改。

```java
public class FinalDemo1 {
    public static void main(String[] args) {
        // 声明变量，使用final修饰
        final int a;
        // 第一次赋值 
        a = 10;
        // 第二次赋值
        a = 20; // 报错,不可重新赋值

        // 声明变量，直接赋值，使用final修饰
        final int b = 10;
        // 第二次赋值
        b = 20; // 报错,不可重新赋值
        
        //此代码无错，因为每次循环，都是一次新的变量c
        for (int i = 0; i < 10; i++) {
            final int c = i;
            System.out.println(c);
        }
    }
}
```

规则四：成员变量涉及到初始化的问题，初始化方式有显示初始化和构造方法初始化，只能选择其中一个

```java
/*显示初始化(在定义成员变量的时候立马赋值)（常用）*/
public class Student {
    final int num = 10;
}

/*构造方法初始化(在构造方法中赋值一次)（不常用，了解即可）*/
/*注意：每个构造方法中都要赋值一次！*/
public class Student {
    final int num = 10;
    final int num2;

    public Student() {
        this.num2 = 20;
//     this.num2 = 20;
    }
    
     public Student(String name) {
        this.num2 = 20;
//     this.num2 = 20;
    }
}
```

## 面向对象进阶3

学习目标：

- [ ] 能够写出抽象类的格式
- [ ] 能够写出抽象方法的格式
- [ ] 能说出抽象类的应用场景
- [ ] 写出定义接口的格式
- [ ] 写出实现接口的格式
- [ ] 说出接口中成员的特点
- [ ] 能说出接口的应用场景
- [ ] 能说出接口中为什么会出现带有方法体的方法
- [ ] 能完成适配器设计模式

### 抽象类

在方法重写中，父类可能知道子类应该有哪个功能，但是功能具体怎么实现父类是不清楚的（由子类自己决定），父类只需要提供一个没有方法体的定义即可，具体实现交给子类自己去实现。

**我们把没有方法体的方法称为抽象方法。Java语法规定，包含抽象方法的类就是抽象类**。

**注意：抽象类不一定有抽象方法，但是有抽象方法的类必须定义成抽象类。**

#### abstract关键字

使用`abstract` 关键字修饰方法，该方法就成了抽象方法，抽象方法只包含一个方法名，而没有方法体。

```java
/*修饰符 abstract 返回值类型 方法名 (参数列表)；*/
public abstract void run()；
```

#### 抽象类的使用

**要求**：继承抽象类的子类**必须重写父类所有的抽象方法**。否则，该子类也必须声明为抽象类。

```java
// 父类,抽象类
abstract class Employee {
	private String id;
	private String name;
	private double salary;
	
	public Employee() {
	}
	
	public Employee(String id, String name, double salary) {
		this.id = id;
		this.name = name;
		this.salary = salary;
	}
	
	// 抽象方法
	// 抽象方法必须要放在抽象类中
	abstract public void work();
}

// 定义一个子类继承抽象类
class Manager extends Employee {
	public Manager() {
	}
	public Manager(String id, String name, double salary) {
		super(id, name, salary);
	}
	// 2.重写父类的抽象方法
	@Override
	public void work() {
		System.out.println("管理其他人");
	}
}

// 定义一个子类继承抽象类
class Cook extends Employee {
	public Cook() {
	}
	public Cook(String id, String name, double salary) {
		super(id, name, salary);
	}
	@Override
	public void work() {
		System.out.println("厨师炒菜多加点盐...");
	}
}

// 测试类
public class Demo10 {
	public static void main(String[] args) {
		// 创建抽象类,抽象类不能创建对象
		// 假设抽象类让我们创建对象,里面的抽象方法没有方法体,无法执行.所以不让我们创建对象
//		Employee e = new Employee();
//		e.work();
		
		// 3.创建子类
		Manager m = new Manager();
		m.work();
		
		Cook c = new Cook("ap002", "库克", 1);
		c.work();
	}
}
```

此时的方法重写，是子类对父类抽象方法的完成实现，我们将这种方法重写的操作，也叫做**实现方法**。

**特别需要注意的是：抽象类失去了创建对象的能力。**

#### 抽象类的细节

不需要背，只要当idea报错之后，知道如何修改即可。

关于抽象类的使用，以下为语法上要注意的细节，虽然条目较多，但若理解了抽象的本质，无需死记硬背。

1. 抽象类**不能创建对象**，如果创建，编译无法通过而报错。只能创建其非抽象子类的对象。

   > 理解：假设创建了抽象类的对象，调用抽象的方法，而抽象方法没有具体的方法体，没有意义。

2. 抽象类中，可以有构造方法，是供子类创建对象时，初始化父类成员使用的。

   > 理解：子类的构造方法中，有默认的super()，需要访问父类构造方法。

3. 抽象类中，不一定包含抽象方法，但是有抽象方法的类必定是抽象类。

   > 理解：未包含抽象方法的抽象类，目的就是不想让调用者创建该类对象，通常用于某些特殊的类结构设计。

4. 抽象类的子类，必须重写抽象父类中**所有的**抽象方法，否则子类也必须定义成抽象类，编译无法通过而报错。 

   > 理解：假设不重写所有抽象方法，则类中可能包含抽象方法。那么创建对象后，调用抽象的方法，没有意义。

5. 抽象类存在的意义是为了被子类继承。

   > 理解：抽象类中已经实现的是模板中确定的成员，抽象类不确定如何实现的定义成抽象方法，交给具体的子类去实现。

### 接口

**接口是更加彻底的抽象，JDK7之前，包括JDK7，接口中全部是抽象方法。接口同样是不能创建对象的**。

```java
//接口的定义格式：
interface 接口名称{
    // 抽象方法
}

// 接口的声明：interface
// 接口名称：首字母大写，满足“驼峰模式”
```

#### 实现接口 interface

1. 接口中的抽象方法默认会自动加上public abstract修饰程序员无需自己手写
2. 在接口中定义的成员变量默认会加上： public static final修饰，也就是说在接口中定义的成员变量实际上是一个常量，必须给初始值。
3. 常量命名规范建议字母全部大写，多个单词用下划线连接。


```java
public interface InterF {
    // 抽象方法！
    //    public abstract void run();
    void run();

    //    public abstract String getName();
    String getName();

    //    public abstract int add(int a , int b);
    int add(int a , int b);


    // 它的最终写法是：
    // public static final int AGE = 12 ;
    int AGE  = 12; //常量
    String SCHOOL_NAME = "黑马程序员";
}
```

#### 类实现接口

类与接口的关系为实现关系，即**类实现接口**，该类可以称为接口的实现类，也可以称为接口的子类。实现的动作类似继承，格式相仿，只是关键字不同，实现使用 ` implements`关键字。

```java
/**接口的实现：
    在Java中接口是被实现的，实现接口的类称为实现类。
    实现类的格式:*/
class 类名 implements 接口1,接口2,接口3...{

}
```

#### 类实现接口的要求和意义

1. 必须重写实现的全部接口中所有抽象方法。
2. 如果一个类实现了接口，但是没有重写完全部接口的全部抽象方法，这个类也必须定义成抽象类。
3. **意义：接口体现的是一种规范，接口对实现类是一种强制性的约束，要么全部完成接口申明的功能，要么自己也定义成抽象类。这正是一种强制性的规范。**

#### 案例一：单接口

```java
/**
   接口：接口体现的是规范。
 * */
public interface SportMan {
    void run(); // 抽象方法，跑步。
    void law(); // 抽象方法，遵守法律。
    String compittion(String project);  // 抽象方法，比赛。
}

package com.itheima._03接口的实现;
/**
 * 接口的实现：
 *    在Java中接口是被实现的，实现接口的类称为实现类。
 *    实现类的格式:
 *      class 类名 implements 接口1,接口2,接口3...{
 *
 *
 *      }
 * */
public class PingPongMan implements SportMan {
    @Override
    public void run() {
        System.out.println("乒乓球运动员稍微跑一下！！");
    }

    @Override
    public void law() {
        System.out.println("乒乓球运动员守法！");
    }

    @Override
    public String compittion(String project) {
        return "参加"+project+"得金牌！";
    }
}

public class TestMain {
    public static void main(String[] args) {
        // 创建实现类对象。
        PingPongMan zjk = new PingPongMan();
        zjk.run();
        zjk.law();
        System.out.println(zjk.compittion("全球乒乓球比赛"));
    }
}
```

#### 案例二：多接口

```java
/** 法律规范：接口*/
public interface Law {
    void rule();
}

/** 这一个运动员的规范：接口*/
public interface SportMan {
    void run();
}

/**
 * Java中接口是可以被多实现的：
 *    一个类可以实现多个接口: Law, SportMan
 *
 * */
public class JumpMan implements Law ,SportMan {
    @Override
    public void rule() {
        System.out.println("尊长守法");
    }

    @Override
    public void run() {
        System.out.println("训练跑步！");
    }
}
```

#### 接口与接口的多继承

Java中，接口与接口之间是可以多继承的：也就是一个接口可以同时继承多个接口。

接口继承接口就是把其他接口的抽象方法与本接口进行了合并。

注意：**类与接口是实现关系**，**接口与接口是继承关系**

```java
public interface Abc {
    void go();
    void test();
}

/** 法律规范：接口*/
public interface Law {
    void rule();
    void test();
}

 *
 *  总结：
 *     接口与类之间是多实现的。
 *     接口与接口之间是多继承的。
 * */
public interface SportMan extends Law , Abc {
    void run();
}
```

#### 接口细节

不需要背，只要当idea报错之后，知道如何修改即可。

关于接口的使用，以下为语法上要注意的细节，虽然条目较多，但若理解了抽象的本质，无需死记硬背。

1. 当两个接口中存在相同抽象方法的时候，该怎么办？

> 只要重写一次即可。此时重写的方法，既表示重写1接口的，也表示重写2接口的。

2. 实现类能不能继承A类的时候，同时实现其他接口呢？

> 继承的父类，就好比是亲爸爸一样
> 实现的接口，就好比是干爹一样
> 可以继承一个类的同时，再实现多个接口，只不过，要把接口里面所有的抽象方法，全部实现。

3. 实现类能不能继承一个抽象类的时候，同时实现其他接口呢？

> 实现类可以继承一个抽象类的同时，再实现其他多个接口，只不过要把里面所有的抽象方法全部重写。

4. 实现类Zi，实现了一个接口，还继承了一个Fu类。假设在接口中有一个方法，父类中也有一个相同的方法。子类如何操作呢？

> 处理办法一：如果父类中的方法体，能满足当前业务的需求，在子类中可以不用重写。
> 处理办法二：如果父类中的方法体，不能满足当前业务的需求，需要在子类中重写。

5. 如果一个接口中，有10个抽象方法，但是我在实现类中，只需要用其中一个，该怎么办?

> 可以在接口跟实现类中间，新建一个中间类（适配器类）
> 让这个适配器类去实现接口，对接口里面的所有的方法做空重写。
> 让子类继承这个适配器类，想要用到哪个方法，就重写哪个方法。
> 因为中间类没有什么实际的意义，所以一般会把中间类定义为抽象的，不让外界创建对象

### 内部类

将一个类A定义在另一个类B里面，里面的那个类A就称为**内部类**，B则称为**外部类**。可以把内部类理解成寄生，外部类理解成宿主。

#### 分类

按定义的位置来分

1. **成员内部内**，类定义在了成员位置 (类中方法外称为成员位置，无static修饰的内部类)
2. **静态内部类**，类定义在了成员位置 (类中方法外称为成员位置，有static修饰的内部类)
3. **局部内部类**，类定义在方法内
4. **匿名内部类**，没有名字的内部类，可以在方法中，也可以在类中方法外。

#### 成员内部类

**获取成员内部类对象的两种方式**：

方式一：外部直接创建成员内部类的对象

```
外部类.内部类 变量 = new 外部类（）.new 内部类（）;
```

方式二：在外部类中定义一个方法提供内部类的对象

演示：

```java
方式一：
public class Test {
    public static void main(String[] args) {
        //  宿主：外部类对象。
       // Outer out = new Outer();
        // 创建内部类对象。
        Outer.Inner oi = new Outer().new Inner();
        oi.method();
    }
}

class Outer {
    // 成员内部类，属于外部类对象的。
    // 拓展：成员内部类不能定义静态成员。
    public class Inner{
        // 这里面的东西与类是完全一样的。
        public void method(){
            System.out.println("内部类中的方法被调用了");
        }
    }
}


方式二：
public class Outer {
    String name;
    private class Inner{
        static int a = 10;
    }
    public Inner getInstance(){
        return new Inner();
    }
}

public class Test {
    public static void main(String[] args) {
        Outer o = new Outer();
        System.out.println(o.getInstance());


    }
}
```

#### 细节

编写成员内部类的注意点：

1. 成员内部类可以被一些修饰符所修饰，比如： private（外界无法直接获取内部类的对象，需要方法二获取内部类的对象，被其他权限修饰符修饰的内部类一般用方式一直接获取内部类的对象），默认，protected，public，static等。
2. 内部类被static修饰是成员内部类中的特殊情况，叫做静态内部类，后续单独学习。
3. 在成员内部类里面，JDK16之前不能定义静态变量，JDK16开始才可以定义静态变量。
4. 创建内部类对象时，对象中有一个隐含的Outer.this记录外部类对象的地址值。
5. 内部类如果想要访问外部类的成员变量，外部类的变量必须用final修饰，JDK8以前必须手动写final，JDK8之后不需要手动写，JDK默认加上。

#### 静态内部类

​	
