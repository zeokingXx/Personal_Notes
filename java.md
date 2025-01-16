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

### 封装思想

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

