# MOS 2022 HTML培训		

![2](https://s2.loli.net/2022/03/03/3B2qNIEsjDKU8L5.png)

![image-20220304194516773](https://s2.loli.net/2022/03/04/W3w1nhO4PFCRUc2.png)

本次课程不会非常详细的讲述html的各种标签，主要是带大家过一遍流程，让大家有一个整体的认知。

> ​                                                                                                                                                                                                                                  **信管1901 龚皓靖**

## 1.HTML概述

### a.网站是什么？

#### 举个例子：

​		一个网站由很多网页组成，可以将多个网页放在一个文件夹中，这个文件夹还可以嵌套其它子文件夹，最终形成一个树状结构，如下图所示：

![image-20220303194006142](https://s2.loli.net/2022/03/03/5WuvDS7Iir3aj1l.png)

​		如果我们给顶级目录 program 绑定一个域名 www.domain.com，那么用户就可以通过 www.domain.com 来访问 program 文件夹中的所有文件（包括子文件夹），例如：

- www.domain.com/demo.html
- www.domain.com/python/for.html
- www.domain.com/java/spring.html
- www.domain.com/java/maven/profile.html

​		可以简单认为，**网站就是一个绑定了域名的文件夹，该文件夹中可以包含子文件夹以及各种各样的文件**，这些文件都可以通过域名来访问。当我们在地址栏中输入一个 **URL** 时，它其实已经展示了服务器上的目录结构，例如www.domain.com/python/for.html，就表示访问 linux 目录下的 for.html 文件。

![image-20220303194517295](https://s2.loli.net/2022/03/03/L4kbYB8DCxnFTOi.png)

#### **URL**

URL是URI的一个子集。它是Uniform Resource Locator的缩写，译为“统一资源定位 符”。

通俗地说，URL是Internet上描述信息资源的字符串，主要用在各种WWW客户程序和服务器程序上。

采用URL可以用一种统一的格式来描述各种信息资源，包括文件、服务器的地址和目录等。**URL是URI概念的一种实现方式**。

URL的一般格式为(带方括号[]的为可选项)：

protocol :// hostname[:port] / path /xxx.html

URL的格式由三部分组成： 

①第一部分是协议(或称为服务方式)。

②第二部分是存有该资源的主机IP地址(有时也包括端口号)。

③第三部分是主机资源的具体地址，如目录和文件名等。

第一部分和第二部分用“://”符号隔开，

第二部分和第三部分用“/”符号隔开。

第一部分和第二部分是不可缺少的，第三部分有时可以省略。 

---

> 网站的本质特征就是**超链接!!! **WWW服务的基础是**Web页**，WWW的核心是**Web服务器**。

+ **WWW**是以超文本标记语言 **HTML**（HyperText Markup Language）与超文本传输协议 **HTTP**（ Hyper Text Transfer Protocol)为基础，向用户提供统一访问界面的信息浏览系统。

+ **网页**：网页是单个的HTML文件，是WWW服务器上公布信息的单位。
+ **网站**：网站是存放在WWW服务器上的展现特定内容的相关**网页**和其它**网络文件**的集合。
+ **主页**：主页是一个特殊的网页，是整个网站信息的起始点和汇总点。主页是访问者浏览网站信息文件的开始点。主页的文件名为index，后缀名为.htm 或.html

#### 静态网页与动态网页：

​		在Internet早期，Web站点是由静态web页组成，静态页面只能固定地显示事先设计好的页面内容。随着Web业务处理越来越多，业务需求层次越来越高，比如商业网站中客户资料的获得、产品信息的查询、信息的反馈等，HTML的局限性日益明显。因此，能够与用户进行动态交互的技术就应运而生了。动态网页页面内容是经过了服务端处理，完成了动态的个性化设置。但是，客户端用户所接收到的结果以HTML格式显示，与传统页面没有任何区别。

![image-20220304200036843](https://s2.loli.net/2022/03/04/RQurNlyqfMdGAkY.png)

![image-20220303192918413](https://s2.loli.net/2022/03/03/N5wtR6sqdQG4VZT.png)

###### 常见的动态网页技术：

+ CGI （Common Gateway Interface），公用网关接口。用来实现CGI应用程序的编程语言有许多种，如Visual Basic、 C/C++、Perl等。CGI方式编程困难且效率低，网站的每个客户在访问CGI程序时Web服务器都要单独建立一个应用进程，加重了服务器负荷。CGI多用在安全级别要求高的Web应用中。
+ ASP（Active Server Pages）是微软公司推出的Web应用程序开发技术。ASP允许用服务器端VBScript脚本语言编程，利用ASP内建对象和组件进一步扩展HTML，实现动态网页。ASP文件运行在服务器端，经过服务器解析之后将结果返回给客户浏览器。ASP的工作环境是微软的IIS应用服务器。一般与Access或My SQL、SQL Server数据库配合使用。
+ ASP.net技术是Microsoft.net技术框架中组成部分之一。可用任何与.net兼容的语言（包括C#、VB.net、JScript.net等）开发应用程序。文件一般以.aspx或.ashx结尾。运行环境是微软的IIS应用服务器。
+ JSP（Java Server Pages）是由Sun公司推出的，基于Java Servlet以及整个Java体系的Web开发技术。JSP可以创建安全和跨平台的动态网站。JSP代码被编译成Servlet并由Java虚拟机执行。① 通用性好，主流系统平台都支持JSP。② JSP使得页面内容与其显示相互独立。③ JSP继承Java技术的优点，包括存储管理和安全性。**不少大型企业使用Java EE平台提供的JSP技术构建Web系统。**
+  PHP（Hypertext Preprocessor）----超文本预处理器。文件后缀名一般为 .php，运行于Apache Tomcat服务器。①  跨平台，PHP程序可以运行在Unix、Linux、Windows操作系统。 ② 语法简单，实用性强，它混合了C/C++、Java、Perl及PHP式的新语法。③ 效率高，PHP消耗较少的系统资源。④ 良好的数据库支持，只要数据库支持ODBC连接标准就行，一般与My SQL数据库配合使用。

#### Web服务器:

Web服务器也可以称为**网站服务器**，可以用来放置网站文件，供用户浏览。目前最主流的Web服务器有**IIS**、**Apache**和**Nginx**，此外**Tomcat**的使用也比较常见，另外还有kangle、WebSphere和Weblogic等类型。

##### Windows IIS:

IIS是Internet Information Server（信息服务）的缩写，也是微软主推的web服务器产品，适用于windows系统，很多著名网站都采用IIS搭建，ASP、.net开发的程序一般也只能在IIS上运行。

IIS提供了一个图形界面的管理工具，称为 Internet服务管理器，可用于监视配置和控制Internet服务，其中包括Web服务器、FTP服务器、NNTP服务器和SMTP服务器，分别用于网页浏览、文件传输、新闻服务和邮件发送等方面，IIS的使用让网络（包括互联网和局域网）上的信息发布变得非常简单。同时，IIS还提供ISAPI（Intranet Server API）作为扩展Web服务器功能的编程接口，并提供一个Internet数据库连接器，可以实现对数据库的查询和更新。

##### Apache:

Apache是目前世界上最流行的Web服务器之一，支持跨平台应用，可以运行在几乎所有的Unix、windows、linux系统平台上，尤其对linux的支持相当完美。

Apache是开源免费的，有很多开发者都参与了设计和改进，推动了产品的持续完善。Apache的特点是简单、高速、性能稳定，可作代理服务器使用。到目前为止，Apache仍然是世界上用的最多的Web服务器，其成功之处主要在于源码开放、强大的社区支持、跨平台应用以及可移植性等方面。不过，Apache是以进程为基础的结构，要比线程消耗更多的系统开支，不太适合于多处理器环境，还有就是并发不强，流量大了就容易出现500错误。

##### Nginx:

Nginx是一种高性能的HTTP和反向代理web服务器，支持高并发和负载均衡，以稳定性、丰富的功能集、示例配置文件和低系统资源的消耗而闻名。

Nginx可以在大多数Unix/Linux上编译运行，并有Windows移植版。Nginx的安装简单、配置文件简洁（支持perl语法），同时Bug非常少，几乎可以做到7*24不间断运行，支持在不间断服务的情况下进行软件版本升级。在连接高并发的情况下，Nginx是Apache服务不错的替代品。同时Nginx的模块也非常丰富，能够满足不同的需求，适合做静态使用。另外Nginx还提供了IMAP/POP3/SMTP服务，是一个非常优秀的邮件代理服务器。

##### Tomcat:

Tomcat是一个开放源代码、运行servlet和JSP Web应用软件、并基于Java的Web应用软件容器。由于技术先进、性能稳定，而且免费，深受Java 爱好者欢迎，同时，也得到了部分软件开发商认可，成为目前比较流行的Web应用服务器。

Tomcat 属于轻量级应用服务器，在中小型系统和并发访问用户不是很多的场合下被普遍使用，是开发和调试JSP 程序的首选。和IIS等Web服务器一样，tomcat也有处理HTML页面的功能，另外它还是一个Servlet和JSP容器（默认模式下为独立的Servlet容器）。不过，Tomcat处理静态HTML的能力不如Apache服务器，目前Tomcat最新版本为9.0。

##### 其他:

**Kangle**是一款跨平台、功能强大、易操作的高性能web服务器和反向代理服务器，也是一款专为做虚拟主机研发的web服务器，实现虚拟主机独立进程、独立身份运行与用户安全隔离，支持php、asp、[http://asp.net](https://link.zhihu.com/?target=http%3A//asp.net)、java、ruby等多种动态开发语言。

**WebSphere**是IBM 的软件平台，包含了编写、运行和监视全天候的工业强度的随需应变Web应用程序和跨平台、跨产品解决方案所需要的整个中间件基础设施，如服务器、服务和工具。WebSphere 是一个模块化的平台，基于业界支持的开放标准，并可在 Intel、Linux 和 z/OS等多平台运行。

**WebLogic**是Oracle出品的一款多功能、基于标准的web应用服务器，是一款基于JAVAEE架构的中间件，用于开发、集成、部署和管理大型分布式Web应用、网络应用和数据库应用，将Java的动态功能和安全标准引入大型网络应用的开发、集成、部署和管理之中，为企业构建自己的应用提供了坚实的基础。

### b.什么是html：

>“html”是“Hyper Text Markup Language”的缩写，即**“超文本标记语言”**，是标准通用标记语言下的一个应用。html并不是一种编程语言，它是一种标记语言，是由一些标签组成，主要是用来制作网页的。为什么说是超文本语言呢？“超文本”指的是它的内容可以是一些非文本的内容，比如：图片、链接、声音等等。HTML是一种解释执行的语言，无需编译。它与操作系统平台的选择无关，只要有浏览器就可以运行HTML文档，显示网页内容

#### 1) 超文本

也即超越纯文本，这意味着 HTML 文档不仅能包含文本（文字），还能包含图片、音视频、表格、列表、链接、按钮、输入框等高级内容。

#### 2) 标记语言

HTML 是一种计算机语言，但它不能编程，只能用来标记网页中的内容。HTML 通过不同的标签来标记不同的内容、格式、布局等，例如：

- <img> 标签表示一张图片；

- <a> 标签表示一个链接；

- <table> 标签表示一个表格；

- <input> 标签表示一个输入框；

- \<p>  标签表示一段文本；

- <strong> 标签表示文本加粗效果；

- \<div> 标签表示块级布局。

#### 总结

HTML 是一种用来开发网页的计算机语言，它通过标签（标记式指令）将文本、音视频、图片、表格、按钮、输入框等内容显示出来。**也就是说，HTML 是用来给网页内容进行排版和布局的。**



![image-20220303202322368](https://s2.loli.net/2022/03/03/wJj7mPUCpzDERfc.png)

#### DHTML技术：

![image-20220303202718060](https://s2.loli.net/2022/03/03/dwo8DhVi2p9Q7CP.png)

![image-20220303202732080](https://s2.loli.net/2022/03/03/Kj5R9LFZwq8APcC.png)

DHTML使HTML专注于文档结构整理，CSS来专注于信息的视觉表现。
HTML+CSS，可使网页内容(Content)与表现(Design)完全分离，以更好的结构来展示信息，使信息易于展现并易于修改。

JavaScript 脚本语言，可以用来为Web增加交互性。

#### HTML5和HTML:

HTML代表超文本标记语言，用于使用标记语言设计网页。HTML是超文本和标记语言的组合，超文本定义了网页之间的链接；标记语言用于定义标记内的文本文档，该文档定义网页的结构。此语言用于注释（在计算机注释中）文本，以便机器可以理解它并相应地操作文本。【推荐阅读：[html参考手册](http://html.cn/doc/html/)】

大多数标记（例如HTML）语言都是人类可读的。该语言使用标签来定义必须对文本进行哪些操作。它用于在网页上构造和呈现内容。

HTML5是HTML的第五个版本，HTML5中删除或修改了许多元素。

###### HTML和HTML5的区别

（1）HTML5支持SVG，画布和其他虚拟矢量图形，而在HTML中，只有将它与Flash，Silver-light等不同技术结合在一起才能使用矢量图形。

（2）HTML5使用Web SQL数据库，可用于临时存储数据但在HTML中只有浏览器缓存才可用于此目的。

（3）HTML5支持新的表单控件，例如：日期和时间，电子邮件，数字，范围，电话，网址，搜索等。

（4）HTML 5是否允许音频和视频控件以及标签，HTML不允许音频

（5）在HTML 5中，Doctype声明非常简单易用，Doctype声明在HTML中太长且复杂，html5:文档声明相对来说更为简便，有利于程序员快速阅读和开发。<!DOCTYPE html>

（6）charset，async和ping的属性是HTML 5的一部分，HTML中不存在charset，async和ping等属性

（7）增强了对Web应用程序功能的支持：在HTML5允许浏览器作为应用程序平台运行不需要使用任何基于JS或Flash的方法，因为HTML5中固有的元素提供了所有功能。

（8）新增加<menu>和<menuitem>元素

### c.开发工具：

> ​		只要是有编辑功能的编辑器，基本都可以用来开发html，甚至可以使用电脑自带的记事本、word等编辑器，只要记住把文档的后缀名改为.html就可以了。当然不建议使用比如记事本之类的编辑器，因为这类编辑器没有提示也没有格式，使用起来开发效率低。如果是刚开始学习的话，可以使用这种编辑器，会帮助你记忆（写多了自然就记住了）。
>
> 我平常主要使用vscode.通过安装插件vscode开发起html,cs,js等各种语言十分方便。
>
> 强烈推荐这个编辑器，通过安装插件可以开发前端，java，Python，c#,c/c++等各种语言，也可以用来开发Arduino,stm32,esp-idf等。

#### Vscode配置教程：

https://blog.csdn.net/caohongxing/article/details/108632859 ||https://blog.csdn.net/caohongxing/article/details/108632859



---



#### 一、Visual Studio Code
下载地址：https://code.visualstudio.com/

功能介绍：

微软在2015年4月30日Build 开发者大会上正式宣布了 Visual Studio Code 项目：一个运行于 Mac OS X、Windows和 Linux 之上的，针对于编写现代 Web 和云应用的跨平台源代码编辑器。

Visual Studio Code软件功能非常强大，界面简洁明晰、操作方便快捷，设计得很人性化。软件主要改进了文档视图，完善了对 Markdown的支持，新增PHP语法高亮。

![image-20220303205915676](https://s2.loli.net/2022/03/03/mqxvW9BTEhF6PGz.png)

#### 二、hbuilder
下载地址：http://www.dcloud.io/

功能介绍：

前端开发小白入门首选，hbuilder是国产的一款前端开发工具而且是免费的，对于英语不好的前端工程师是一个不错的消息。

优点是有强大的其他语言支持和开发webapp等功能，强大到没朋友。在语法提示、转到定义、重构、调试等方面都非常高效。缺点也是有一些的，就是其有些稳定，有时可能会有些卡顿的现象

![image-20220303205759147](https://s2.loli.net/2022/03/03/ciIdJRjqr7b3HBT.png)

#### 三、sublime text3
下载地址：http://www.sublimetext.com/

功能介绍：

sublime text是一个轻量级的编辑器，也是支持各种编程语言，sublime text所有的强大功能都是支持插件的，而且快捷键十分的好用，可以极大的减少开发的劳动程度，使用sublime就是要使用其快捷键和插件。

sublime text3的优点的轻量级但是功能强大，优雅小巧启动速度快，有着丰富的第三方支持，能够满足各种各样的扩展缺点是对于项目的管理等不是很方便，但代码提示不如hubuilder强大。

![image-20220303210220430](https://s2.loli.net/2022/03/03/FwYHoEda6b34KLm.png)

#### 四、WebStorm
下载地址：https://www.jetbrains.com/webstorm/

功能介绍：

WebStorm 是jetbrains公司旗下一款JavaScript 开发工具。官方提供的插件支持，满足许多不会配置的同学，ESlint，词法高亮，emmet，CSS预处理器，新版本也添加了对ES6的支持，内建了服务器调试。

目前已经被广大中国JS开发者誉为“Web前端开发神器”、“最强大的HTML5编辑器”、“最智能的JavaScript IDE”等。与IntelliJ IDEA同源，继承了IntelliJ IDEA强大的JS部分的功能。

![image-20220303205823471](https://s2.loli.net/2022/03/03/qWgGm431aETsdJF.png)

#### 五、Atom
下载地址：https://atom.io/

功能介绍：

Atom 是github专门为程序员推出的一个跨平台文本编辑器。平易近人,但可删节的核心工具定制做任何事,也可以使用有效不沾一个配置文件。为开源而生。

具有简洁和直观的图形用户界面，并有很多有趣的特点：支持CSS，HTML，JavaScript等网页编程语言。它支持宏，自动完成分屏功能，集成了文件管理器。

![image-20220303205833749](https://s2.loli.net/2022/03/03/xCMBUGHSuF4WcA3.png)

#### 六 ：Dreamweaver CC 2017
下载地址：https://www.adobe.com/products/dreamweaver.html

功能介绍：

老牌的IDE ，曾经以PS+DW+FW称霸网页领域，号称网页三剑客，然而之前的版本更新较慢，版本陈旧，已经满足不了广大前端开发者的项目需求，逐渐被市场淘汰。

好在2017版本及时修正，外观、界面、语法高亮等已经很漂亮，并且添加了CSS预处理器支持，同时保留了部分预制组件，方便对语法还不熟悉的同学，对于不会node的同学也有提供实时预览，适合对前端有进一步了解的同学。

![image-20220303205849362](C:\Users\immortal\AppData\Roaming\Typora\typora-user-images\image-20220303205849362.png)

### d.学习方法与资料：

> 学习html很简单，就是学习一些标签的用法，但是需要我们多写，多练才能熟悉，才能灵活的应用。

一些好用的学习网站:

+ W3school:https://www.w3school.com.cn/html/index.asp
+ 菜鸟教程：https://www.runoob.com/html/html-tutorial.html
+ c语言中文网：http://c.biancheng.net/html/



## 2.浏览器开发者工具使用：

![image-20220305104314851](https://s2.loli.net/2022/03/05/1FdZM5msiYgpN4W.png)

F12打开开发者工具

Chrome开发者工具中，调试时使用最多的三个功能页面是：元素（ELements）、控制台（Console）、源代码（Sources），此外还有网络（Network）等。

+ **元素（Elements）**：用于查看或修改HTML元素的属性、CSS属性、监听事件、断点等。css可以即时修改，即时显示。大大方便了开发者调试页面
+ **控制台（Console）**：控制台一般用于执行一次性代码，查看JavaScript对象，查看调试日志信息或异常信息。还可以当作Javascript API查看用。例如我想查看console都有哪些方法和属性，我可以直接在Console中输入"console"并执行Sources:断点调试JS。
+ **源代码（Sources）**：该页面用于查看页面的HTML文件源代码、JavaScript源代码、CSS源代码，此外最重要的是可以调试JavaScript源代码，可以给JS代码添加断点等。
+ **网络（Network）**：记录当前页面请求加载信息，并记录各个请求资源信息（包括状态、资源类型、大小、所用时间等），可以根据这个进行网络性能优化。
+ **性能（Performance）:**用来对当前页面进行性能分析。
+ **内存（Memory）:**用于分析当前页面内存消耗。
+ **应用（Application）:**记录网站加载的所有资源信息，包括存储数据（Local Storage、Session Storage、IndexedDB、Web SQL、Cookies）、缓存数据等。
+ **安全（Security）:**判断当前网页是否安全。
+ **审计（Audits）:**对当前网页进行网络利用情况、网页性能方面的诊断，并给出一些优化建议。

## 3.HTML基本语法：

Html标签语法简单，本次课程通过菜鸟教程网站进行HTML5基本语法教学，选择性的讲解常用的html标签，帮助大家节省初次学习的时间，课程结束后可根据需要自己按需进行学习。

https://www.runoob.com/html/html-tutorial.html

## 4.Http协议：

### a.网络通讯原理：

**学习资料：**https://www.cnblogs.com/zyx110/p/11891335.html

计算机网络是由通信介质将地理位置不同的且相互独立的计算机连接起来，实现数据通信与资源共享。互联网的本质就是一系列的协议，总称为‘互联网协议’（Internet Protocol Suite).互联网协议的功能：定义计算机如何接入internet，以及接入internet的计算机通信的标准。

互联网协议按照功能的不同，分为 osi 七层， tcp / ip 五层， tcp / ip 四层协议。如下图：

![image-20220303223109565](https://s2.loli.net/2022/03/03/xcz65KtPUAI8F3k.png)



**OSI七层协议数据传输的封包与解包过程**

![](https://s2.loli.net/2022/03/03/1cOHP2CXZByKhQn.gif)

**osi 的七层协议体系结构的概念清楚，理论也比较完善，但它既复杂又不实用， ISO 制定的 osi 协议参考模型的过于庞大、复杂招致了许多批评。于此对照，由技术人员自己开发的 TCP / IP 协议获得了更为广泛的应用。因此，我们只需要弄明白 TCP / IP 五层协议 就能了解和明白计算机最底层的通信是怎么回事。**

##### TCP/IP五层协议

![image-20220303223350905](https://s2.loli.net/2022/03/03/l9NapIUSkHtnC3Z.png)

如图，从最下方的物理层到最上方的应用层，对于我们用户而言，最直接的是应用层。从上到下每一层都依赖于下一层

### b.TCP/IP协议族：

互联网协议族（Internet Protocol Suite，缩写IPS）是一个网络通信模型，以及一整个网络传输协议家族，为互联网的基础通信架构。它常被通称为TCP/IP协议族（TCP/IP Protocol Suite，或TCP/IP Protocols），简称TCP/IP。

TCP/IP 模型包含了 TCP、IP、UDP、Telnet、FTP、SMTP 等上百个互为关联的协议，其中 TCP 和 IP 是最常用的两种底层协议，所以把它们统称为“TCP/IP 协议族”。

![image-20220303223835617](https://s2.loli.net/2022/03/03/MbKZu8E2BD5LSvA.png)

![image-20220303223855051](https://s2.loli.net/2022/03/03/XPpAM9qLcsJf7KU.png)

在上面，通常我们是把TCP/IP协议族分为四层，但是如果是五层的话就是在链路层下再加个物理层。下面是对各层的详细介绍。

![image-20220303224035631](https://s2.loli.net/2022/03/03/flQ8d4Tm5BsFarv.png)

![image-20220303224154206](https://s2.loli.net/2022/03/03/4SEq6yvV7z38dC1.png)

如上图所示，当应用程序采用TCP传送数据时，数据被送入协议栈中，然后，通过每一层直到被当做一串比特流传入网络中。其中每一层收到数据都会对数据增加一些首部信息（有的还需要尾部信息）。TCP传给IP的数据单元称为TCP报文段或简称为TCP段（UDP传给IP的数据单元称为UDP数据段），IP传给网络接口层的数据单元称为IP数据报。通过以太网传输的比特流称为帧。

当目的主机收到了一个以太网的数据帧时，数据要从协议栈中，由底往上，同时去掉各层协议上的报文首部，如下图所示：

![image-20220303224238944](https://s2.loli.net/2022/03/03/XLrgfIAevwknQzO.png)



### c.Scoket:

学习资料：http://c.biancheng.net/view/2123.html

![image-20220303224731252](https://s2.loli.net/2022/03/03/JSidQWUKRBZFPej.png)

#### 什么是Socket?:

​		socket 的原意是“插座”，在计算机通信领域，socket 被翻译为“套接字”，它是计算机之间进行通信的一种约定或一种方式。通过 socket 这种约定，一台计算机可以接收其他计算机的数据，也可以向其他计算机发送数据。

​		socket 的典型应用就是 Web 服务器和浏览器：浏览器获取用户输入的 URL，向服务器发起请求，服务器分析接收到的 URL，将对应的网页内容返回给浏览器，浏览器再经过解析和渲染，就将文字、图片、视频等元素呈现给用户。

​		简单来说，就是操作系统实现了TCP/IP协议族的各种通讯协议，然后通过Socket这个接口开放给用户，使用户和应用程序具有访问网络的能力。

![image-20220303225239399](https://s2.loli.net/2022/03/03/iHgURtzuoDnNQbh.png)

Socket是应用层与TCP/IP协议族通信的中间软件抽象层，它是一组接口。在设计模式中，Socket其实就是一个门面模式，它把复杂的TCP/IP协议族隐藏在Socket接口后面，对用户来说，一组简单的接口就是全部，让Socket去组织数据，以符合指定的协议。

#### Socket使用教程：

![image-20220303225955305](https://s2.loli.net/2022/03/03/XJIhFr7BTPy4f6V.png)

先从服务器端说起。服务器端先初始化Socket，然后与端口绑定(bind)，对端口进行监听(listen)，调用accept阻塞，等待客户端连接。在这时如果有个客户端初始化一个Socket，然后连接服务器(connect)，如果连接成功，这时客户端与服务器端的连接就建立了。客户端发送数据请求，服务器端接收请求并处理请求，然后把回应数据发送给客户端，客户端读取数据，最后关闭连接，一次交互结束。

#### Socket作用：

+ 所谓进程指的是：运行的程序以及运行时用到的资源这个整体称之为进程

+ 所谓进程间通信指的是：运行的程序之间实现数据共享和传递

socket(简称 套接字) 是最通用的进程间通信的一种方式，它与其他进程间通信的一个主要不同是：

**它能实现不同主机间的进程间通信**，我们网络上各种各样的服务大多都是基于 Socket 来完成通信的

例如我们每天浏览网页、QQ 聊天、收发 email 等等

### d.常用的Http协议：

> Http协议是基于TCP的，主要用于web的一种应用层协议

#### http协议简介：

超文本传输协议（英文：**H**yper**T**ext **T**ransfer **P**rotocol，缩写：HTTP）是一种用于分布式、协作式和超媒体信息系统的应用层协议。HTTP是万维网的数据通信的基础。

HTTP的发展是由蒂姆·伯纳斯-李于1989年在欧洲核子研究组织（CERN）所发起。HTTP的标准制定由万维网协会（World Wide Web Consortium，W3C）和互联网工程任务组（Internet Engineering Task Force，IETF）进行协调，最终发布了一系列的RFC，其中最著名的是1999年6月公布的 RFC 2616，定义了HTTP协议中现今广泛使用的一个版本——HTTP 1.1。

2014年12月，互联网工程任务组（IETF）的Hypertext Transfer Protocol Bis（httpbis）工作小组将HTTP/2标准提议递交至IESG进行讨论，于2015年2月17日被批准。 HTTP/2标准于2015年5月以RFC 7540正式发表，取代HTTP 1.1成为HTTP的实现标准。

HTTP是一个客户端终端（用户）和服务器端（网站）请求和应答的标准（TCP）。通过使用网页浏览器、网络爬虫或者其它的工具，客户端发起一个HTTP请求到服务器上指定端口（默认端口为80）。我们称这个客户端为用户代理程序（user agent）。应答的服务器上存储着一些资源，比如HTML文件和图像。我们称这个应答服务器为源服务器（origin server）。在用户代理和源服务器中间可能存在多个“中间层”，比如代理服务器、网关或者隧道（tunnel）。

尽管TCP/IP协议是互联网上最流行的应用，HTTP协议中，并没有规定必须使用它或它支持的层。事实上，HTTP可以在任何互联网协议上，或其他网络上实现。HTTP假定其下层协议提供可靠的传输。因此，任何能够提供这种保证的协议都可以被其使用。因此也就是其在TCP/IP协议族使用TCP作为其传输层。

通常，由HTTP客户端发起一个请求，创建一个到服务器指定端口（默认是80端口）的TCP连接。HTTP服务器则在那个端口监听客户端的请求。一旦收到请求，服务器会向客户端返回一个状态，比如"HTTP/1.1 200 OK"，以及返回的内容，如请求的文件、错误消息、或者其它信息。

---

在浏览器地址栏键入URL，按下回车之后会经历以下流程：

1. 浏览器向 DNS 服务器请求解析该 URL 中的域名所对应的 IP 地址;
2. 解析出 IP 地址后，根据该 IP 地址和默认端口 80，和服务器建立TCP连接;
3. 浏览器发出读取文件(URL 中域名后面部分对应的文件)的HTTP 请求，该请求报文作为 TCP 三次握手的第三个报文的数据发送给服务器;
4. 服务器对浏览器请求作出响应，并把对应的 html 文本发送给浏览器;
5. 释放 TCP连接;
6. 浏览器将该 html 文本并显示内容; 　

#### HTTP协议格式：

##### 请求格式：

![image-20220303232330788](https://s2.loli.net/2022/03/03/bmayBPNvInKh37U.png)

HTTP 的请求报文由三部分构成：

+ **请求行**：由请求方法（Method）、URL 字段和 HTTP 的协议版本组成，注意其中的空格、回车符和换行符均不可省略，所以我们的请求方法实际上就是位于请求行中的了。

+ **请求头部**：位于请求行之后，个数可以为 0~若干个，每个请求头部都包含一个头部字段名和一个值，它们之间用冒号 ":" 分隔，在最后用回车符和换行符表示结束。

+ **请求数据**：如果请求方法为 **GET**，那么请求数据为空。它主要是在 **POST** 中进行使用，适用于需要填表单（FORM）的场景。我们通过一个实际的例子来看看 **HTTP** 的 **GET** 请求报文是什么样的，我们这里以访问 api.github.com/search/users?q=JakeWharton为例，通过抓包我们得到的请求报文如下所示：

![image-20220303232348577](https://s2.loli.net/2022/03/03/ieEjqB8fT3I7bJU.png)

请求头里面的内容举个例子：这个length表示请求体里面的数据长度，其他的请求头里面的这些键值对，陆续我们会讲的，大概知道一下就可以了，其中有一个user-agent，算是需要你记住的吧，就是告诉你的服务端，我是用什么给你发送的请求。

##### 响应格式：

![image-20220303232516838](https://s2.loli.net/2022/03/03/jbXckhwVd4DYaBO.png)

![image-20220303232540390](https://s2.loli.net/2022/03/03/YNIz9wlXu8f6BMH.png)

![image-20220303233505506](https://s2.loli.net/2022/03/03/y6JOrg7VCklKhNq.png)

**请求方法（所有方法全为大写）有多种，各个方法的解释如下：**
**GET**   请求获取Request-URI所标识的资源
**POST**  在Request-URI所标识的资源后附加新的数据
HEAD  请求获取由Request-URI所标识的资源的响应消息报头
PUT   请求服务器存储一个资源，并用Request-URI作为其标识
DELETE 请求服务器删除Request-URI所标识的资源
TRACE  请求服务器回送收到的请求信息，主要用于测试或诊断
CONNECT 保留将来使用
OPTIONS 请求查询服务器的性能，或者查询与资源相关的选项和需求
应用举例：
GET方法：在浏览器的地址栏中输入网址的方式访问网页时，浏览器采用GET方法向服务器获取资源，eg:GET /form.html HTTP/1.1 (CRLF)

POST方法要求被请求服务器接受附在请求后面的数据，常用于提交表单。
eg：POST /reg.jsp HTTP/ (CRLF)
Accept:image/gif,image/x-xbit,... (CRLF)
...
HOST:www.guet.edu.cn (CRLF)
Content-Length:22 (CRLF)
Connection:Keep-Alive (CRLF)
Cache-Control:no-cache (CRLF)
(CRLF)     //该CRLF表示消息报头已经结束，在此之前为消息报头
user=jeffrey&pwd=1234 //此行以下为提交的数据

HEAD方法与GET方法几乎是一样的，对于HEAD请求的回应部分来说，它的HTTP头部中包含的信息与通过GET请求所得到的信息是相同的。利用这个方法，不必传输整个资源内容，就可以得到Request-URI所标识的资源的信息。该方法常用于测试超链接的有效性，是否可以访问，以及最近是否更新。

> 最常用的就是GET和POST请求



## 5.Html在嵌入式中的应用

### a.为什么使用Html?

> 大家平时在使用单片机进行编程时，经常会遇到**显示**，**控制**和**调试**三个问题，即对单片机结果的展示，如何对单片机实施控制以及程序运行时对参数和程序的调试。以Stm32为例，显示可以采用OLED屏或LCD彩屏，控制可以采用按键或者电阻触摸屏，调试采用串口调试参数或者按键调试参数，对新手来说，采用以上方法可能有一些难度，在传统的前后台编程模式中，以上三个模块加入程序会增加程序的复杂度，可能会带来一系列的问题。

大家在平时做应用时，如果涉及到人机交互，可以考虑使用串口屏，串口屏内部集成了显示屏的驱动程序，MCU可以通过串口来实现显示，控制，和调试三个行为。但这种做法的唯一缺点就是串口屏幕的价格较高。同时，如果程序十分复杂的话，可以考虑在stm32上应用RTOS实时操作系统，简化编程难度，提高程序的执行效率。

针对使用串口屏价格较高，直接驱动LCD屏难以做出美观界面的问题。大家在平时的应用中可以考虑使用网页的形式来做人机交互。

#### 如何使用？

+ ESP32官网教程：https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/get-started/index.html

+ Micropython教程：http://www.micropython.com.cn/en/latet/library/index.html

Esp32内置了lwip这个轻量级的TCP/IP协议栈；前面我们说过Socket是应用层与TCP/IP协议族通信的中间软件抽象层，因此我们可以在esp32上进行socket编程来使用tcp/udp等协议，而http又是基于TCP协议的，因此我们可以在esp32上使用HTTP协议来与手机或者电脑上的浏览器传递信息。

> lwIP是一套在MCU层级上用C实现的IP协议栈，可以运行在裸机/RTOS/嵌入式Linux，乐鑫为ESP32提供了相关移植包
>
> MIPS(Million Instructions Per Second)：单[字长](https://baike.baidu.com/item/字长)定点指令平均执行速度 Million Instructions Per Second的缩写，每秒处理的百万级的[机器语言](https://baike.baidu.com/item/机器语言/2019225)指令数。这是衡量CPU速度的一个指标。
>
> BLE是低功耗蓝牙的英文缩写（Bluetooth Low Energy），是蓝牙4.0版本起开始支持的新的、低功耗版本的蓝牙技术规范。

ESP32是由我国的乐鑫公司设计研发的一款可作为独立系统运行应用程序或是主机 MCU 的从设备，通过 SPI / SDIO 或 I2C / UART 接口提供 Wi-Fi 和蓝牙功能。该芯片专为移动设备、可穿戴电子产品和物联网应用而设计，具有业内高水平的低功耗性能，包括精细分辨时钟门控、省电模式和动态电压调整等。其次ESP32将天线开关、RF balun、功率放大器、接收低噪声放大器、滤波器、电源管理模块等功能集于一体，这使得ESP32 只需极少的外围器件，即可实现强大的处理性能、可靠的安全性能，和 Wi-Fi & 蓝牙功能。同时，ESP32 具备极其稳定的性能，工作温度范围达到 –40°C 到 +125°C。集成的自校准电路实现了动态电压调整，可以消除外部电路的缺陷并适应外部条件的变化。

Esp32

![image-20220304162059054](https://s2.loli.net/2022/03/04/yaOwUYQs6L9vMIq.png)

ESP32 有丰富的资源，Xtensa® 32-bitLX6单/双核处理器，运算能力高达600MIPS（除ESP32-S0WD为200MIPS，ESP32-D2WD 为 400 MIPS），拥有448K ROM，**520KB SRAM**，34个 GPIO端口。

除了常规单片机资源外，吸引我的主要是以下资源：

· WIFI模块，支持 2.4G 频段

· 蓝牙模块，支持 BLE 和经典蓝牙

· CAN 控制器，外接一个 CAN收发器便可以实现汽车以及工业使用的CAN总线

· Touch Sensor，拥有 9个GPIO支持作为电容触摸输入使用，不需要单独配置触摸传感器

原始的FreeRTOS设计为在单个内核上运行。但是ESP32是双核，包含协议CPU（称为CPU 0或PRO_CPU）和应用程序CPU（称为CPU 1或APP_CPU）。这两个内核实际上是相同的，并且共享相同的内存。这允许两个内核在它们之间交替运行任务。

> FreeRTOS,可以分为两部分Free和RTOS, Free就是免费的、自由的、不受约束的意思, RTOS全称是Real Time Operating System,中文名就是实时操作系统。可以看出FreeROTS就是一个免费的RTOS类系统。这里要注意, RTOS不是指某一个确定的系统,而是指一类系统。比如uC/os, FreeRTOS, RTX, RT-Thread等这些都是RTOS类操作系统。操作系统允许多个任务同时运行,这个叫做多任务,实际上,一个处理器核心在某一时刻只能运行一个任务。操作系统中任务调度器的责任就是决定在某一时刻究竟运行哪个任务,任务调度在各个任务之间的切换非常快!这就给人们造成了同一时刻有多个任务同时运行的错觉。操作系统的分类方式可以由任务调度器的工作方式决定,比如有的操作系统给每个任务分配同样的运行时间,时间到了就轮到下一个任务, Unix操作系统就是这样的。RTOS的任务调度器被设计为可预测的,而这正是嵌入式实时操作系统所需要的,实时环境中要求操作系统必须对某一个事件做出实时的响应,因此系统任务调度器的行为必须是可预测的。像FreeRTOS这种传统的RTOS类操作系统是由用户给每个任务分配一个任务优先级,任务调度器就可以根据此优先级来决定下一刻应该运行哪个任务。FreeRTOS是RTOS系统的一种, FreeRTOS十分的小巧,可以在资源有限的微控制器中运行,当然了, FreeRTOS不仅局限于在微控制器中使用。但从文件数量上来看FreeRTOS要比uC/OSII和uC/OSII小的多。
>
> 【翻译自官网】普通的FreeRTOS运行在单核上，不彳亍！我们的ESP32-FreeRTOS能运行在双核，彳亍！
>
> 众所周知，ESP32是物美价廉的双核SoC，CPU0和CPU1同时运行、共享内存。乐鑫修改了普通的FreeRTOS，让它能够支持SMP（symmetric multiprocessing对称多处理），所以ESP32的FreeRTOS变成了基于FreeRTOS v8.2.0的Xtensa架构移植版SMP RTOS
>
> **下面对移植版的FreeRTOS简称为SMP RTOS**，
>
> 【补充】对称多处理（SMP）架构是一种两个或多个CPU共享同一内存公共链路的计算机体系结构
>
> *他改变了FreeRTOS*

**ESP32内嵌 FreeRTOS操作系统**，可以支持多任务编程，因此我们可以使用两个进程，一个进程进行正常的工作，另一个进程专门用来进行http协议的处理。

##### 通讯流程：

![image-20220304185020099](https://s2.loli.net/2022/03/04/6nDfsHuryZdBMpl.png)

+ 浏览器端处理：可以使用js的setInterval设置定时时间来执行相应的函数，或者通过事件的方式执行函数，发送http请求可以使用XMLHttpReq。
+ MCU端处理：通过micropython的 _thread模块新建一个进程来单独负责http请求的处理，调用accept()函数后，线程被阻塞，当浏览器发起http请求时，先与MCU的80端口建立连接，然后发送HTTP请求头，控制信息可以包含在http请求头中，方便esp32端进行处理。

##### ESP32常用编程方式：

+ ESP-IDF： 采用c/c++的语法进行编程，官方推荐，优点是灵活，官方文档上的各种API比较多。
+ Micropython: Esp32需要刷入相应固件，人生苦短，我用python，优点不多说。但我使用的时候发现如果使用micropython的话好像不能发挥esp32的全部性能？在micropython中可以使用的内存变小了好多。
+ Arduino: 使用c/c++语法编程，简单易用，Arduino平台上的各种开源库让你十分方便就能做出各种炫酷的应用。

### b.Esp32 Micropython示例

以灯哥开源四足机器人项目控制程序为例：

项目开源地址 Github:https://github.com/ToanTech/py-apple-quadruped-robot

![image-20220304190750266](https://s2.loli.net/2022/03/04/oHpnJTLhf2lEqD7.png)

## 





## 6.个人网站搭建流程

![image-20220305190927994](https://s2.loli.net/2022/03/05/glF4mhB6dR9zsYP.png)

> Linux服务器环境搭建可以参考我原来写过的一篇文章：http://www.gonghaojing.top:8080/archives/linux-yuan-cheng-fu-wu-qi-huan-jing-da-jian

### a.云服务器选型：

 云服务器是一台部署在云端的一台远程主机，通过ssh协议可以想在本地一样使用云服务器。**ssh协议**属于TCP/IP协议族中的一种用于远程登录的安全的通讯协议，它位于体系结构中的应用层，实际是使用Tcp协议进行通讯。常见的远程登录有telnet和ssh两种，但**ssh**协议是十分安全的，因为它在通讯的过程中，会对需要通讯的消息进行加密，实际传输的都是密文，十分安全，故而经常用于远程控制服务器。

 拥有一台远程服务器是很酷的一件事情，拥有一台服务器可以干许多事情，例如**搭建一台MQTT服务器**，然后可以使用ESP8266或ESP32等芯片轻松实现物联网应用。**搭建一台Frp服务**，轻松实现内网穿透，解决众多小伙伴没有公网ip的烦恼。**搭建一台Mysql服务器**,实现数据的远程存储。**配置Tomcat服务器**,搭建个人网站或博客，或者搭建一台**我的世界**服务器等等...

 现在网上有许多服务器的供应商，例如阿里云，腾讯云等，每个平台新用户或双十一的时候都有巨大折扣。购买服务器时主要看**三个指标**：**1.性能指标：**例如1核2G或2核4G,主要体现云服务器的性能。**2.带宽：**带宽也是一个很重要的指标，带宽除以8就是实际的最大网速，对于网站，游戏服务器等并发量可能会比较大的应用，需要选取合适的带宽。**3，是否是境外服务器**:对于境外服务器，搭建网站的时候不需要备案，如何时境内的，根据相关法律法规的要求，必须要进行备案。ps:网站备案程序十分麻烦，建议早做准备，我前段时间为我的域名备案，一顿操作后还让我苦等了半个月，其中艰辛不足为外人道也。。。如果是境外服务器还可以搭建梯子，frp就可以实现Socket代理和http代理，实现科学上网。但境外服务器的价格普遍比国内服务器的价格贵许多。

腾讯云：https://cloud.tencent.com/

阿里云：https://cn.aliyun.com/

### b.域名购买及解析：

配置好域名解析后可以通过域名直接访问到主机，免得去记忆主机ip。正常情况下，解析成功后80端口的网站是不能访问的，需要网站需要域名备案后才能访问。

腾讯云：https://buy.cloud.tencent.com/domain

### c.网站搭建：

Tomcat服务器教程：https://blog.csdn.net/heyeqingquan/article/details/96437921

#### 个人网站：

> 个人网站。可以采用网上下载建站模板，自己修改的方式。零基础也可以迅速开发出精美的网站。

+ 站长之家：https://sc.chinaz.com/moban/
+ 第一模板网：https://www.11moban.com/grmb/index
+ 网站模板库：http://www.baisheng999.com/
+ 英文的模板库：https://html5up.net/
+ 网页插件库：http://www.htmleaf.com/html5/html

#### 个人博客：

> 个人博客。可以使用WordPress或者基于Java的halo博客工具，快速开发出自己的博客。

+ Halo官网：https://halo.run/
+ Halo美化教程：https://bestzuo.cn/posts/halo-beauty.html#%E5%86%99%E5%9C%A8%E5%89%8D%E9%9D%A2

### d.备案：

一般在域名服务商那里都会有代备案系统

#### ICP备案：

ICP备案的目的就是为了防止在网上从事非法的网站经营活动，打击不良互联网信息的传播，如果网站不备案的话，很有可能被查处以后关停。根据中华人民共和国信息产业部第十二次部务会议审议通过的《非经营性互联网信息服务备案管理办法》条例，在中华人民共和国境内提供非经营性互联网信息服务，应当办理备案。未经备案，不得在中华人民共和国境内从事非经营性互联网信息服务。而对于没有备案的网站将予以罚款或关闭。

#### 公安备案：

网站备案是根据国家法律法规需要网站的所有者向国家有关部门申请的备案，公安局备案是其中一种。公安局备案一般按照各地公安机关指定的地点和方式进行，操作流程会比ICP备案流程简单，主要是已登记为主。

![image-20220304192337538](https://s2.loli.net/2022/03/04/bI7s3zBMyVRJUaq.png)

以百度官网为例，其中`京公安网备11000002000001`就是公安备案，`京ICP证030173号`就是ICP备案

### e.CNZZ站长工具：

**该站长工具可以通过在你的网页中添加链接，从而对访问网页的人数，频率等进行统计。**

CNZZ（ http://www.cnzz.com）是全球最大的中文互联网数据统计分析服务提供商，为中文网站及中小企业提供专业、权威、独立的第三方数据统计与分析服务。目前累计超过400万家网站采用了CNZZ提供的流量统计服务，一周覆盖90%以上的上网用户。

CNZZ站长统计和全景统计是两款专业的实时网站流量统计分析系统，可以帮助网站管理员、运营人员、推广人员等实时获取网站流量，并从流量来源、网站内容、网站访客特性等多方面提供网站分析的数据依据。从而帮助您提高网站流量，提升网站的用户体验，让访客更多的沉淀下来变成会员或客户，通过更少的投入获取最大化的收入。

通过简单的几步操作，安装CNZZ统计代码，您就可以实时获得多达几十种的网站数据报告，且所有的报告按照网站数据分析思路一气呵成。网站分析领域的统计指标在CNZZ统计中都可以快速找到，拥有“浏览次数（PV）”、“独立访客（UV）”、“IP”、“访问次数（Session）”这种基础流量指标，也拥有像“平均访问时长”、“跳出率”这种衡量访客行为的指标。[更多可提供的指标见这里](http://help.cnzz.com/tongji/mingcijieshi/)。

### f.上线：

把你的服务器软件运行起来就上线了

## 7.JAVA WEB概述：

如果你想成为一个专业的后端开发工程师

参照动力节点Java web学习流程：https://space.bilibili.com/76542346/favlist?fid=124751046



