# **1**、持续集成Jenkins介绍

## 1.1、软件开发生命周期

软件开发生命周期又叫做**SDLC (** Software Development Life Cycle ),它是集合了计划、开发、测试 和部署过程的集合。如下图所示：

![image-20210626230554259](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626230554259.png)

- 需求分析 

  这是生命周期的第一阶段，根据项目需求,团队执行一个可行性计划的分析。项目需求可能是公司内部 或者客户提出的。这阶段主要是对信息的收集,也有可能是对现有项目的改善和重新做一个新的项目。 还要分析项目的预算多长,可以从哪方面受益及布局,这也是项目创建的目标。

- 设计

  第二阶段就是设计阶段,系统架构和满意状态(就是要做成什么样子,有什么功能),和创建一个项目 计划。计划可以使用图表,布局设计或者文者的方式呈现。

- 实现

  第三阶段就是实现阶段,项目经理创建和分配工作给开者,开发者根据任务和在设计阶段定义的目鼬 行开发代码。依据项目的大小和复杂程度,可以需要数月或更长时间才能完成。

- 测试

  测试人员进行代码测试,包括功能测试、代码测试、压力测试等。

- 进化

  最后进阶段就是对产品不断的进化改进和维护阶段，根据用户的使用情况，可能需要对某功能进行修 改，bug修复，功能增加等。

## 1.2、软件开发瀑布模型

瀑布模型是最著名和最常使用的软件开发模型。瀑布模型就是一系列的软件开发过程。它是由制造业繁 衍出来的。一个高度化的结构流程在一个方向上流动,有点像生产线一样。在瀑布模型创建之初,没有 其它开发的模型,有很多东西全靠开发人员去猜测,去开发。这样的模型仅适用于那些简单的软件开 发，但是已经不适合现在的开发了。

下图对软件开发模型的一个阐述。

![image-20210626230842482](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626230842482.png)


| **优势**                                   | **劣势**                                                     |
| :----------------------------------------- | :----------------------------------------------------------- |
| 简单易用和理解                             | 各个阶段的划分完全固定,阶段之间产生大量的文档,极大地 增加了工作量。 |
| 当前一阶段完成后,您只需要 去关注后续阶段。 | 由于开发模型是线性的,用户只有等到整个过程的末期才能见 到开发成果,从而增加了开发风险。 |
| 为项目提供了按阶段划分的检 查节点          | 瀑布模型的突出缺点是不适应用户需求的变化。                   |

## 1.3、软件的敏捷开发

### **什么是敏捷开发?**

敏捷开发(Agile Development)的核心是迭代开发(Iterative Development)与增量开发(Incremental Development) 。

### 何为迭代开发

对于大型软件项目，传统的开发方式是采用一个大周期(比如一年)进行开发，整个过程就是一次”大 开发，迭代开发的方式则不一样,它将开发过程拆分成多个小周期，即一次”大开发”变成多次“小开 发，每次小开发都是同样的流程*，*所以看上去就好像重复在做同样的步骤。

举例来说，SpaceX公司想造一个大推力火箭,将人类送到火星。但是，它不是一开始就造大火箭，而 是先造一个最简陋的小火箭Falcon 1。结果，第一次发射就爆炸了，直到第四次发射，才成功进入轨道。然后，开发了中型火箭Falcon 9 ,九年中发射了70次。最后，才开发Falcon重型火箭。如果 SpaceX不采用迭代开发,它可能直到现在还无法上天。

### **何为增量开发**

软件的每个版本*，*都会新增一个用户可以感知的完整功能。也就是说*，*按照新增功能来划分迭代。

举例来说,房产公司开发一个10栋楼的小区。如果采用增量开发的模式,该公司第一个迭代就是交付一 号楼，第二个迭代交付二号楼每个迭代都是完成一栋完整的楼。而不是第一个迭代挖好10栋楼的地	 基，第二个迭代建好每栋楼的骨架，第三个迭代架设屋顶	.....

### **敏捷开发如何迭代**

虽然敏捷开发将软件开发分成多个迭代，但是也要求，每次迭代都是一个完整的软件开发周期，必须按 照软件工程的方法论，进行正规的流程管理。

![image-20210626231051397](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626231051397.png)

### 敏捷开发有什么好处

- **早期交付**

  敏捷开发的第一个好处，就是早期交付，从而大大降彳蹴本。还是以上一节的房产公司为例,如果按照 传统的"瀑布开发模式"，先挖10栋楼的地基、再盖骨架、然后架设屋顶，每个阶段都等到前一个阶段完 成后开始,可能需要两年才能一次性交付10栋楼。也就是说,如果不考虑预售,该项目必须等到两年后 才能回款。敏捷开发是六个月后交付一号楼,后面每两个月交付一栋楼。因此,半年就能回款10%,后 面每个月都会有现金流,资金压力就大大减轻了。

- **降低风险**

  敏捷开发的第二个好处是,及时了解市场需求,降彳氐产品不适用的风险。请想一想,哪一种情况损失比 较小:［。栋楼都造好以后,才发现卖不出去,还是造好第一栋楼,就发现卖不出去,从而改进或停建后 面9栋楼?

- **什么是持续集成**

持续集成(Continuous integration ,简称Cl )指的是,频繁地(一天多次)将代码集成到主干。

**持续集成的目的，就是让产品可以快速迭代，同时还能保持高质量。**它的核心措施是，代码集成到主干 之前，必须通过自动化测试。只要有一个测试用例失败，就不能集成。

通过持续集成,团队可以快速的从一个功能到另一个功能,简而言之,敏捷软件开发很大一部分都要归 功于持续集成。

### 持续集成的流程

![image-20210626231509180](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626231509180.png)

根据持续集成的设计,代码从提交到生产,整个过程有以下几步。

- **提交** 

流程的第一步,是开发者向代码仓库提交代码。所有后面的步骤都始于本地代码的一次提交 (commit)。

- **测试**（第一轮）

代码仓库对commit操作配置了钩子（hook）,只要提交代码或者合并进主干,就会跑自动化测试。

- **构建**

鮑第一轮测试,代码就可以合并进主干,瞬可以交付了。

交付后，就先进行构建（build ）,再进入第二轮测试。所谓构建，指的是将源码转换为可以运行的实 际代码,比如安装依赖,配置各种资源（样式表、JS脚本、图片）等等。

- **测试（第二轮）**

构建完成,就要进行第二轮测试。如果第一轮已经涵盖了所有测试内容,第二轮可以省略,当然,这时 构建步骤也要移到第一轮测试前面。

- **部署**

过了第二$仑测试,当前代码就是一个可以頡部署的版本（artifact）。将这个版本的所有文件打包（ tarfilename.tar\* ）	,发到生产服务器。

- **回滚**

一旦当前版本发生问题，就要回滚到上一个版本的构建结果。最简单的做法就是修改一下符号踊，指 向上一个版本的目录。

### 持续集成的组成要素

- 一个自动构熙程，从检出代码、编译构建、运行测试、结果记录、测试统计等都是自动完成 的，无需人工干预。

- 一个代码存储库,即需要版本控制软件来保障代码的可维护性,同时作为构建过程的素材库,一般 使用SVN或Git。

- 一个持续集成服务器，Jenkins就是一个配置简单和使用方便的持续集成服务器。


![image-20210626232106748](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626232106748.png)

### 持续集成的好处

1、	降低风险,由于持续集成不断去构建,编译和测试,可以很早期发现问题,所以修复的代价就少;

2、	对系统健康持续检查，减少发布风险带来的问题；

3、	减少重复性工作；

4、	持续部署,提供可部署单元包；

5、	持续交付可供使用的版本；

6、	增强团队信心；

### Jenkins介绍

![image-20210626232303592](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626232303592.png)


Jenkins是一款流行的开源持续集成(Continuous Integration )工具,广泛用于项目开发,具有自动 化构建、测试和部署等功能。官网：http://jenkins-ci.org/。

**Jenkins的特征:**

- 开源的Java语言开发持续集成工具,支持持续集成,持续部署。

- 易于安装部署配置:可通过yum安装,或下载war包以及通过docker容器等快速实现安装部署,可 方便web界面配置管理。

- 消息通知及测试报告：集成RSS/E-mail通过RSS发布构建结果或当构建完成时通过e-mail通知，生 成Unit/TestNG测试报告。

- 分布式构建:支持Jenkins能够让多新算机一起构建/测试。

- 文件识SU : Jenkins能够跟踪哪次构建生成哪些jar,哪次构建使用哪个版本的jar等。

- 丰富的插件支持:支持扩展插件，你可以开发适合自己团队使用的工具,如git , svn , maven , docker等。

# 2、Jenkins安装和持续集成环境配置

## 2.1、持续集成流程说明

![image-20210626232439387](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626232439387.png)

1. ）首先，开发人员每天进行代码提交,提交到Git仓库
1. ）然后，Jenkins作为持续集成工具，使用Git工具到Git仓库拉取代码到甄服务器,再配合JDK , Maven等软件完成代码编译，代码测试与审查，测试，打包等工作，在这个过程中每一步出错，都重新 再执行一次整个龈
1. ）最后，Jenkins把生成的jar或war包分发到测试服务器或者生产服务器,测试人员或用户就可以访问 应用。

### 2.1.1、服务器列表

本课程虚拟机统一采用CentOS7。

| **名称**        | **IP地址**     | **安装的软件**                                         |
| :-------------- | :------------- | :----------------------------------------------------- |
| 代码托管服务 器 | 192.168.66.100 | Gitlab-12.4.2                                          |
| 持续集成服务 器 | 192.168.66.101 | Jenkins-2.190.3 , JDK1.8 , Maven3.6.2 , Git, SonarQube |
| 应用测试服务 器 | 192.168.66.102 | JDK1.8 , Tomcat8.5                                     |

## 2.2、Gitlab

**Gitlab简介**

![image-20210626232807368](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626232807368.png)

官网：<https://aboutgitlab.com/>

GitLab是一个用于仓库管理系统的开源项目，使用Git作为代码管理工具,并在此基础上搭建起来的 web服务。

GitLab和GitHub一样属于第三方基于Git开发的作品,免费且开源（基于MIT协议*）,*与Github类似, 可以注册用户,任意提交你的代码,添加SSHKey等等。不同的是,**GitLab是可以部署到自己的服务器 上，数据库等一切信息都掌握在自己手上，适合团队内部协作开发**，你总不可能把团队内部的智慧总放在别人的服务器上吧？简单来说可把GitLab看作个人版的GitHub。

### **2.2.1、Gitlab代码托管服务器安装**

1. 安装相关依赖

   > yum -y install policycoreutils openssh-server openssh-clients postfix

2. 启动ssh服务&设置为开机启动

   > systemctl enable sshd && sudo systemctl start sshd

3. 设置postfix开机自启，并启动，postfix支持gitlab发信功能

   > systemctl enable postfix && systemctl start postfix

4. 开放ssh以及http服务，然后重新加载防火墙列表

   > firewall-cmd -add-service=ssh -permanent

   > firewall-cmd -add-service=http -permanent

   > firewall-cmd -reload

   如果关闭防火墙就不需要做以上配置

5. 下载gitlab包，并且安装

   ​	在线下载安装包:

   ​	wget <https://mirrors.tuna.tsin>ghua.edu.en/gitlab-ce/yum/el6/gitlab-ce-12.4.2-ce.0.el6.x86 64.rpm

   ​	安装:

   ​	rpm -i gitlab-ce-12.4.2-ce.0.el6.x86\_64.rpm

6. 修改gitlab配置

   vi /etc/gitlab/gitlab.rb

​		修改gitlab访问地照口端口 ,默认为80 ,我们改为82

​		external\_url 'http:〃192.168.66.100:82’

​		nginx['listen\_port'] = 82

7. 重载配置及启动gitlab

   gitlab-ctl reconfigure

   gitlab-ctl restart

8. 把端口添加到防火墙

   firewall-cmd -zone二public -add-port=82/tcp -permanent

   firewall-cmd -reload

启动成功后,看到以下修改管理员root密码的页面，修改密码后,然后登录即可

![image-20210626233648489](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626233648489.png)

### **2.2.2、Gitlab添加组、创建用户、创建项目**

1 ）创建组

使用管理员root创建组,一个组里面可以有多个项目分支,可以将开发添加到组里面进行设置权限, 不同的组就是公司不同的开发项目或者服务模块,不同的组添加不同的开发即可实现对开发设置权限的 管理

![image-20210626233731851](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626233731851.png)

![image-20210626233741557](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626233741557.png)

2）创建用户

创建用户的时候，可以选择Regular或Admin类型。

![image-20210626233813987](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626233813987.png)

创建完用户后，立即修改密码![image-20210626234038570](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234038570.png)

3）将用户添加到组中

选择某个用户组,进行Members管理组的成员

![image-20210626234148738](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234148738.png)

![image-20210626234202802](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234202802.png)

Gitlab用户在组里面有5种不同权限：

Guest :可以创建issue、发表评论，不能读写版本库Reporter :可以克隆代码,不能提交，QA、PM 可以赋予这个权限Developer :可以克隆代码、开发、提交、push ,普通开发可以赋予这个权限 Maintainer :可以创建项目、添加tag、保护分支、添加项目成员、编辑项目，核心开发可以赋予这个 权限Owner:可以设置项目访问权限-Visibility Level.删除项目、迁移项目、管理组成员，开发组组 长可以赋予这个权限

4）在用户组中创建项目

以刚才创建的新用户身份登录到Gitlab ,然后在用户组中创建新的项目

![image-20210626234354810](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234354810.png)

![image-20210626234411384](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234411384.png)

### 2.2.3、源码上传到Gitlab仓库

下面来到IDEA开发工具,我们已经准备好一个简单的Web应用准备到集成部署。

我们要把源码上传到Gitlab的项目仓库中。

1 ）项目结构说明

![image-20210626234559057](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234559057.png)



我们建立了一个非常简单的web应用,只有一个index.jsp页面,如果部署好,可以访问该页面就成功 啦！

2）开启版本控制

![image-20210626234640352](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234640352.png)

2) 提交代码到本地仓库

先Add到缓存区

![image-20210626234744975](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234744975.png)

再Commit到本地仓库

![image-20210626234818835](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234818835.png)

3 ）推送到Gitlab项目仓库中
![image-20210626234919641](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234919641.png)

这时都Gitlab的项目中拷贝url地址

**web\_demo**

![image-20210626234940169](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626234940169.png)

输入gitlab的用户名和密码,然后就可以把代码推送至U远程仓库啦

![image-20210626235023276](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235023276.png)
刷新gitlab项目

![image-20210626235048003](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235048003.png)

## 2.3、持续集成环境

### 2.3.1、Jenkins安装

1. ）安装JDK

   Jenkins需要依赖JDK,所以先安装JDK1.8

   yum install java-1.8.0-openjdk\* -y

   安装目录为：/usr/lib/jvm

2. ）获取jenkins安装包

   下载页面：https://jenkins.io/zh/download/

   安装文件:jenkins-2.190.3-1.1.noarch.rpm

3. ）把安装包上传到192.168.66.101服务器,进行安装

   rpm -ivh jenkins-2.190.3-1.1 .noarch.rpm

4. ）修改Jen kins配置

   vi /etc/syscofig/jenkins

   修改内容如下：

   JENKINS\_USER=,,rootK

   JENKINS\_PORT=,,8888H

5 ）启动Jenkins

​	systemctl start jenkins

6）打开浏览器访问

​	http://192.168.66.101:8888

​	注意:本服务器把防火墙关闭了，如果开启防火墙,需要在防火墙添加端口

7 ）获取并输入admin账户密码

​	cat /va r/lib/jenkins/secrets/initialAd min Password

8）跳过插件安装

![image-20210626235415429](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235415429.png)

9 ）添加一个管理员账户,并进入Jenkins后台

![image-20210626235455941](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235455941.png)

![image-20210626235533961](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235533961.png)

![image-20210626235545810](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235545810.png)

### 2.3.2、Jenkins插件管理

Jenkins本身不提供很多功能,我们可以通过使用插件来满足我们的使用。例如从Gitlab拉取代码，使用 Maven构建项目等功能需要依靠插件完成。接下来演示如何下载插件。

**修改Jenkins插件下载地址**

Jenkins国夕卜官方插件地址下载速度非常慢,所以可以修改为国内插件地址:

![image-20210626235723230](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210626235723230.png)

这样做是为了JBjenkins官方的插件列表下载到本地，接着修改地址文件，替换为国内插件土也址

> cd /var/lib/jenkins/updates

> sed -i 's/http:\/\/updates.jenkins-ci.org\/download/https:\/\/mirrors.tuna.tsinghua.edu.cn\/jenkins/g' default.json && sed -i's/http:\/\/www.google.com/https:\/\/www.baidu.com/g' default.json

最后,Manage Plugins点击Advanced ,把Update Site改为国内插件下载地址

> https://mirrors.tuna.tsinghua.edu.cn/jenkins/updates/update-center.json

![image-20210627000043974](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000043974.png)

Sumbit 后,在浏览器输入：http://192.168.66.101:8888/restart  ,重启Jenkins。

**下载中文汉化插件**

Jenkins->ManageJenkins->Manage Plugins ,点击Available ,搜索”Chinese”

![image-20210627000144329](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000144329.png)

重启Jenkins后,就看至Men kins汉化了 ！（ PS :但可能部分菜单汉化会失败）

![image-20210627000158718](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000158718.png)

### 2.3.3、Jenkins用户权限管理

​	我们可以利用Role-based Authorization Strategy插件来管理Jenkins用户权限

**安装Role-based Authorization Strategy插件**

![image-20210627000250342](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000250342.png)

**开启权限全局安全配置**

![image-20210627000331197](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000331197.png)

**创建角色**

在系统管理页面进入Manage and Assign Roles

![image-20210627000445099](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000445099.png)

点击"Manage Roles"

![image-20210627000511584](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000511584.png)

Global roles（全局角色）：管理员等高级用户可以创建基于全局的角色 

Project roles（项目角色）：针对某个或者某些项目的角色 

Slave roles（奴隶角色）：节点相关的权限



我们添加以下三个角色：

- baseRole :该角色为全局角色。这个角色需要绑定0verall下面的Read权限，是为了给所有用户绑 定最基本的Jenkins访问权限。注意:如果不给后续用户绑定这个角色，会报错误:用户名is missing the Overall/Read permission

- rolel :该角色为项目角色。使用正则表达式绑定"itcast.\*” ,意思是只能操作itcast开头的项目。

- role2 :该角色也为项目角色。绑定"itheima.\*",意思是只能操作itheima开头的项目。

  ![image-20210627000647411](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000647411.png)

保存。

**创建用户**

在系统管理页面进入Manage Users

![image-20210627000743368](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000743368.png)

分别创建两个用户：jack和eric

![image-20210627000757640](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000757640.png)

**给用户分配角色**

系统管理页面进入Manage and Assign Roles ,点击Assign Roles 绑定规则如下：

- eric用户分别绑定baseRole和rolel角色
- jack用户分别绑定baseRole和role2角色

![image-20210627000831893](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000831893.png)

保存。

**创建项目测试权限**

以itcast管理员账户创建两个项目,分别为itcastOI和itheimaOl

![image-20210627000848880](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000848880.png)

结果为:

- eric用户登录，只能看到itcastOI项目
- jack用户登录，只能看到itheimaOl项目

### 2.3.4、Jenkins凭证管理

凭据可以用来存储需要密文保护的数据库密码、Gitlab密码信息、Docker私有仓库密码等,以便 Jenkins可以和这些第三方的应用进行交互。

**安装Credentials Binding插件**

要在Jenkins使用凭证管理功能,需要安装Credentials Binding插件

![image-20210627000956324](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627000956324.png)


安装插件后*，*左边多了”凭证”菜单,在这里管理所有凭证

![image-20210627001047726](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001047726.png)

可以添加的凭证有5种：

![image-20210627001110238](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001110238.png)

- Username with password :用户名和密码
- SSH Username with private key :使用SSH用户和密钥
- Secret file :需要保密的文本文件，使用时Jenkins会将文件复制到一个临时目录中,再将文件路径 设置到一个变量中,等构建结束后,所复制的Secret file就会被删除。
- Secret text :需要保存的一个加密的文本串,如钉钉机器人或Github的api token
- Certificate :通过上传证书文件的方式

常用的凭证类型有：**Username with password （用户密码）和SSH Username with private key （ SSH 密钥）**

接下来以使用Git工具到Gitlab拉取项目源码为例，演示Jenkins的如何管理Gitlab的凭证。

**安装Git插件和Git工具**

*为了*让Jenkins支持从Gitlab拉取源码,需要安装Git插件以及在CentOS7上安装Git工具。

Git插件安装：

![image-20210627001303490](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001303490.png)

CentOS7上安装Git工具：

> yum install git -y 安装

> git -version安装后查看版本

**用户密码类型**

1 ）创建凭证

![image-20210627001342726](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001342726.png)

![image-20210627001358472](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001358472.png)

选择"Username with password"，输入Gitlab的用户名和密码，点击"确定"。

![image-20210627001425250](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001425250.png)

2）测试凭证是否可用

创建一个Freestyle项目：新建ltem->FreeStyle Project->确定


![image-20210627001458382](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001458382.png)

找至U"源码管理'->"Git",在Repository URL复制Gitlab中的项目URL

![image-20210627001514064](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001514064.png)

这时会报错说无法连接仓库!在Credentials；®择刚刚添加的凭证就不报错啦

![image-20210627001545931](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001545931.png)

保存配置后*，*点击构建"Build Now"开始构建项目

![image-20210627001608574](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001608574.png)

![image-20210627001621527](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001621527.png)

查看**/var/lib/jenkins/workspace/**目录，发现已经从Gitlab成功拉取了代码至Ujenkins中。

![image-20210627001714263](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001714263.png)

**SSH密钥类型**

SSH免密登录示意图

![image-20210627001731874](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001731874.png)

1 ）使用root用户生成公钥和私钥 

> ssh-keygen -t rsa

![image-20210627001822663](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001822663.png)

​	id\_rsa :私钥文件

​	id\_rsa.pub :公钥文件

2 ）把生成的公钥放在Gitlab中

​	以root账户登录->点击头像->Settings->SSH Keys

​	复制刚才id\_rsa.pub文件的内容到这里,点击”Add Key"

![image-20210627001906641](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001906641.png)

3 ）在Jenkins中添加凭证，配置私钥

在Jenkins添加一个新的凭证，类型为"SSH Username with private key",把刚才生成私有文件内容复 制过来

![image-20210627001937238](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627001937238.png)

4*）*测试凭证是否可用

新建"test02''项目->源码管理->Git,这次要使用Gitlab的SSH连接,并且选择SSH凭证

![image-20210627002125265](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002125265.png)

![image-20210627002141667](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002141667.png)

同样尝试构建项目，如果代码可以正常拉取，代表凭证配置成功！

![image-20210627002200846](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002200846.png)

### 2.3.5、Maven安装和配置

​	在Jenkins集成服务器上,我们需要安装Maven来编译和打包项目。

**安装Maven**

先上传 Maven 软件到192.168.66.101

> tar -xzf apache-maven-3.6.2-bin.tar.gz 解压
>
> mkdir -p /opt/maven 仓腱目录
>
> mv apache-maven-3.6.2/\* /opt/maven 移动文件

**配置环境变量**

> vi /etc/profile

![image-20210627002259554](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002259554.png)

> source /etc/profifile 配置生效
>
> mvn -v 查找Maven版本

**全局工具配置关联JDK和Maven**

Jenkins->Global Tool Configuration->JDK->新增JDK ,配置如下：

![image-20210627002351241](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002351241.png)

Jenkins->Global Tool Configuration->Maven->新增Maven ,配置如下:

![image-20210627002411843](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002411843.png)

**添加Jenkins全局变量**

Manage Jenkins->Configure System->Global Properties，添加三个全局变量

JAVAJHOME、M2JH0ME、PATH+EXTRA

![image-20210627002452678](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002452678.png)

**修改Maven的settings.xmI**

> mkdir /root/repo创建本地仓库目录

> vi /opt/maven/conf/settings.xml

本地仓库改为：/root/repo/

添加阿里云私服地址：

> alimaven aliyun maven http://maven.aliyun.com/nexus/content/groups/public/ central

**测试Maven是否配置成功**

使用之前的gitlab密码测试项目,修改配置


![image-20210627002626933](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002626933.png)

构建->增加构建步骤->Execute Shell

![image-20210627002644356](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002644356.png)

输入

> mvn clean package

![image-20210627002708685](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002708685.png)

再次构建，如果可以把项目打成war包,代表maven环境配置成功啦！

![image-20210627002732446](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002732446.png)

**持续集成环境(6)-Tomcat安装和配置**

**安装Tomcat8.5**

> yum install java-1.8.0-openjdk* -y 安装JDK（已完成）
>
> tar -xzf apache-tomcat-8.5.47.tar.gz 解压
>
> mkdir -p /opt/tomcat 创建目录mv /root/apache-tomcat-8.5.47/* /opt/tomcat 移动文件
>
> /opt/tomcat/bin/startup.sh 启动tomcat

注意：服务器已经关闭了防火墙,所以可以直接访问Tomcat啦

地址为：http://192.168.66.102/8080

![image-20210627002847358](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002847358.png)

**配置Tomcat用户角色权限**

默认情况FTomcat是没有配置用户角色权限的

![image-20210627002921934](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002921934.png)

![image-20210627002937476](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002937476.png)

但是，后续Jenkins部署项目到Tomcat服务器,需要用到Tomcat的用户,所以修改tomcat以下配置, 添加用户及权限

> vi /opt/tomcat/conf/tomcat-users.xml

内容如下：

![image-20210627002957844](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627002957844.png)

用户和密码都是：tomcat

注意:为了能够刚才配置的用户登录到Tomcat ,还需要修改以下配置

> vi /opt/tomcat/webapps/manager/META-INF/context.xml

![image-20210627003015101](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003015101.png)

把上面这行注释掉即可!

**重启Tomcat,访问测试**

> /opt/tomcat/bin/shutdown.sh 停止
>
> /opt/tomcat/bin/startup,sh 启动

访问： http://192.168.66.102:8080/manager/html ，输入tomcat和tomcat，看到以下页面代表成功啦

![image-20210627003056537](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003056537.png)



# 3、Jenkins构建Maven项目

## 3.1、Jenkins构建的项目类型介绍

Jenkins中自动构建项目的类型有很多,常用的有以下三种:

- 自由风格软件项目(Freestyle Project)

- Maven项目(Maven Project)

- 流水线项目(Pipeline Project)

每种类型的构建其实都可以完成一样的构建过程与结果,只是在扌榮作方式、灵活度等方面有所区别，在 实际开发中可以根据自己的需求和习惯来跡。(PS :个人推荐使用流水线类型,因为灵活度非常高)

## 3.2、自由风格项目构建

下面演示创建一个自由风格项目来完成项目的集成过程:

> 拉取代码-> 编译-> 打包-> 部署

### 3.2.1、拉取代码

1 )创建项目

![image-20210627003503082](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003503082.png)

2 ）配置源码管理,从gitlab拉取代码

### 3.2.2、源码管理

![image-20210627003517701](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003517701.png)

### 3.2.3、编译打包

构建->添加构建步骤->Executor Shell

> echo ”开始编译和打包”
>
> mvn clean package
>
> echo ”编译和打包结束”

### 3.2.4、部署

把项目部署到远程的Tomca t里面

1 ）安装 Deploy to container插件

Jenkins本身无法实现远程部署到Tomcat的功能,需要安装Deploy to container插件实现

![image-20210627003615754](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003615754.png)

2 ）添加Tomcat用户凭证

![image-20210627003634962](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003634962.png)

3）添加构建后操作

构建后操作

![image-20210627003709734](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003709734.png)

![image-20210627003733352](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003733352.png)

点击"Build Now"，开始构建过程

![image-20210627003754857](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003754857.png)

4 ) 部署成功后,访问项目

http://192.168.66.102:8080/web_demo-1.0-SNAPSHOT/

![image-20210627003840190](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627003840190.png)

### 3.2.5、演示改动代码后的持续集成

1. ) IDEA中源码修改并提交到gitlab
1. )在Jenkin沖项目重新构建
1. )访问Tomcat

## 3.3、Maven项目构建

1. )安装Maven Integration插件

   ![image-20210627004108872](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004108872.png)

2. )创建Maven项目

   ![image-20210627004126681](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004126681.png)

3. )配置项目

拉取代码和远程部署的过程和自由风格项目一样，只是"构建''部分不同

## 3.4、Pipeline流水线项目构建(\*)

### 3.4.1、Pipeline 简介

1）概念

Pipeline ,简单来说，就是一套运行在Jenkins上的工作流框架，将原来独立运行于单个或者多个节点 的任务连接起来,实现单个任务难以完成的复杂流程编排和可视化的工作。

2 ）使用Pipeline有以下好处（来自翻译自官方文档）：

代码:Pipeline以代码的形式实现,通常被检入源代码控制，使团队能够编辑,审查和迭代其传送流 程。持久：无论是计划内的还是计划夕卜的服务器重启,Pipeline都是可恢复的。可停止：Pipeline可接 收交互式输入,以确定是否继续执行Pipeline。多功能：Pipeline支持现实世界中复杂的持续交付要 求。它支持fork/join、循环执行,并行执行任务的功能。可扩展:Pipeline插件支持其DSL的自定义扩 展,以及与其他插件集成的多个选项。

3 ）如何创建 Jenkins Pipeline呢?

- Pipeline脚本是由**Groovy**语言实现的，但是我们没必要单独去学习Groovy
- Pipeline支持两种语法：**Declarative**（声明式）和**Scripted Pipeline**（脚本式）语法
- Pipeline也有两种创建方法:可以直接在Jenkins的Web UI界面中输入脚本；也可以通过创建一 个Jenkinsfile脚本文件放入项目源码库中（一般我们都跡在Jen kins中直接从源代码控制（SCM） 中直接载入Jenkinsfile Pipeline这种方法）。

### 3.4.2、安装Pipeline插件

Manage Jenkins->Manage Plugins-〉可选插件

![image-20210627004248102](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004248102.png)

安装插件后，创建项目的时候多了“流水线”类型

![image-20210627004314480](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004314480.png)

### 3.4.3、Pipeline语法快速入门

#### 1 ) Declarative声明式-Pipeline

创建项目

![image-20210627004346270](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004346270.png)

流水线->选择HelloWorld模板

![image-20210627004447166](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004447166.png)



stages :代表整个流水线的所有执行阶段。通常stages只有1个，里面包含多个stage

stage :代表流水线中的某个阶段,可能岀现n个。一般分为拉取代码,编译构建,部署等阶段。

 steps :代表一个阶段内需要执行的逻辑。steps里面是shell脚本，git拉取代码,ssh远程发布等任意内容。

编写一个简单声明式Pipeline :

![image-20210627004606680](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004606680.png)

点击构建,可以看到整个构建过程


![image-20210627004627388](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004627388.png)

#### 2 ) Scripted Pipeline脚本式-Pipeline

创建项目

![image-20210627004652529](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004652529.png)


这次选择"Scripted Pipeline”

![image-20210627004716182](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004716182.png)

- Node :节点,—个Node就是一个Jenkins节点,Master或者Agent,是执行Step的具体运行 环境,后续讲至Jenkins的Master-Slave架构的时候用到。
- Stage :阶段,一个Pipeline可以划分为若干个Stage ,每个Stage代表一组操作,比如： Build、Test、Deploy , Stage是一个逻辑分组的概念。

- Step :步骤,Step是最基本的操作单元,可以是打印一句话，也可以是构建一个Docker镜像, 由各类Jenkins插件提供，比如命令：sh 'make',就相当于我们平时shell终端中执行make命令—样。

编写一个简单的脚本式Pipeline

![image-20210627004746818](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004746818.png)

构建结果和声明式一样！

**拉取代码**

![image-20210627004803727](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004803727.png)

**编译打包**

![image-20210627004819507](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004819507.png)**部署**

![image-20210627004847089](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004847089.png)

**Pipeline Script from SCM**

刚才我们都是頡在Jenkins的Ul界面编写Pipeline代码，这样不方便脚本维护，建议把Pipeline脚本放 在项目中（一起进行版本控制）

1 ）在项目根目录建立Jenkinsfile文件，把内容复制到该文件中

![image-20210627004909613](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004909613.png)

​	把Jenkinsfile上传到 Gitlab

2)在项目中引用该文件

流水线

![image-20210627004947394](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627004947394.png)

## 3.5、常用的构建触发器

Jenkins内置4种构建触发器:

- 触发远程构建


- 其他工程构建后触发(Build after other projects are build )


- 定时构建(Build periodically )


- 轮询SCM ( Poll SCM )


### 3.5.1、触发远程构建

![image-20210627005208562](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005208562.png)

触发构建url : http://192.168.66.101:8888/job/web_demo_pipeline/build?token=6666

### 3.5.2、其他工程构建后触发

1 ）创建pre\_job流水线工程

![image-20210627005446212](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005446212.png)

2 )配置需要触发的工程

![image-20210627005506568](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005506568.png)

### 3.5.3、定时构建

![image-20210627005550098](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005550098.png)

**定时字符串从左往右分别为：分时日月周**

一些定时表达式的例子：

> 每30分钟构建一次：H代表形参 H/30 * * * * 10:02 10:32
>
> 每2个小时构建一次: H H/2 * * *
>
> 每天的8点，12点，22点，一天构建3次： (多个时间点中间用逗号隔开) 0 8,12,22 * * *
>
> 每天中午12点定时构建一次 H 12 * * *
>
> 每天下午18点定时构建一次 H 18 * * *
>
> 在每个小时的前半个小时内的每10分钟 H(0-29)/10 * * * *
>
> 每两小时一次，每个工作日上午9点到下午5点(也许是上午10:38，下午12:38，下午2:38，下午4:38) H H(9-16)/2 * * 1-5

### 3.5.4、轮询SCM

轮询SCM ,是指定时扫描本地代码仓库的代码是否有变更,如果代码有变更就触发项目构建。

![image-20210627005753100](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005753100.png)

注意:这次构建触发器,Jenkins会定时扫描本土也整个项目的代码,增大系统的开销，不建议使用。

### 3.5.5、Git hook自动触发构建(\*)

刚才我们看到在Jenkins的内置构建触发器中,轮询SCM可以实现Gitlab代码更新,项目自动构建,但是 该方案的性能不佳。那有没有更好的方案呢？有的。就是利用Gitlab的webhook实现代码push到仓 库,立即触发项目自动构建。

轮询SCM原理示意图

![image-20210627005929165](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005929165.png)

#### 3.5.5.1、安装Gitlab Hook插件

需要安装两个插件:

**Gitlab Hook和GitLab**

![image-20210627005949685](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627005949685.png)

#### 3.5.5.2、Jenkins设置自动构建

![image-20210627010006593](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010006593.png)

等会需要把生成的webhook URL配置到Gitlab中。

#### 3.5.5.3、Gitlab 配置 webhook

1 )开启webhook功能

使用root账户登录到后台,点击Admin Area -> Settings -> Network

勾选"Allow requests to the local network from web hooks and services"

![image-20210627010214124](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010214124.png)

2 )在项目添加webhook

点击项目->Settings->lntegrations

![image-20210627010236836](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010236836.png)

注意：以下设置必须完成,否则会报错!

Manage Jenkins->Configure System

![image-20210627010257077](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010257077.png)

### 3.5.6、Jenkins的参数化构建

有时在项目构建的过程中，我们需要根据用户的输入动态传入一些参数，从而影响整个构建结果，这时 我们可以使用参数化构建。

Jenkins支持非常丰富的参数类型

![image-20210627010657409](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010657409.png)


接下来演示通过输入gitlab项目的分支名称来部署不同分支项目。

#### 3.5.6.1、项目创建分支,并推送到Gitlab上

![image-20210627010732985](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010732985.png)


新建分支:V1 ,代码稍微改动下,然后提交到gitlab上。

这时看到gitlab上有一个两个分支:master和v1

![image-20210627010745027](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010745027.png)

#### 3.5.6.2、在Jenkins添加字符串类型参数

![image-20210627010803372](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010803372.png)

![image-20210627010811546](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010811546.png)

#### 3.5.6.3、改动pipeline流水线代码

![image-20210627010823735](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010823735.png)



#### 3.5.6.4、点击Build with Parameters

![image-20210627010852932](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010852932.png)

输入分支名称，构建即可！构建完成后访问Tomcat查看结果

### 3.5.7、配置邮箱服务器发送构建结果

#### 3.5.7.1、安装Email Extension插件

![image-20210627010956122](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627010956122.png)

#### 3.5.7.2、Jenkins设置邮箱相关参数

![image-20210627011036576](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011036576.png)

- 设置邮件参数


![image-20210627011047984](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011047984.png)

- 设置Jenkins默认邮箱信息


![image-20210627011106679](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011106679.png)

#### 3.5.7.3、准备邮件内容

​	在项目根目录编写email.html ,并把文件推送到Gitlab ,内容如下：

![image-20210627011145468](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011145468.png)

![image-20210627011420206](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011420206.png)

![image-20210627011437399](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011437399.png)

#### 3.5.7.4、编写Jenkinsfile添加构建后发送邮件

![image-20210627011541320](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011541320.png)

![image-20210627011553903](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011553903.png)

#### 3.5.7.5、测试

![image-20210627011626521](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011626521.png)

PS :邮件相关全局参数参考列表：

系统设置->Extended E-mail Notification->ContentToken Reference ,点击旁边的?号

![image-20210627011647632](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011647632.png)

## 3.6、Jenkins+SonarQube代码审查

### 3.6.1、安装SonarQube

#### 3.6.1.1、SonaQube 简介

**sonarqube**

SonarQube是一个用于管理代码质量的开放平台,可以快速的定位代码中潜在的或者明显的错误。目前 支持java,C#,C/C++,Python,PL/SQL,Cobol,JavaScrip,Groovy等二十几种编程语言的代码质量管理与检 测。

官网：<https://vwwv.sonarqube.org/>

**环境要求**

| **软件**  | **服务器**     | **版本** |
| :-------- | :------------- | :------- |
| JDK       | 192.168.66.101 | 1.8      |
| MySQL     | 192.168.66.101 | 5.7      |
| SonarQube | 192.168.66.101 | 6.7.4    |

**安装 SonarQube**

1. ）安装MySQL （已完成）
1. ）安装SonarQube

在MySQL创建sonar数据库

![image-20210627011920987](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627011920987.png)

下载sonar压缩包：

https://www.sonarqube.org/downloads/

解压sonar,并设置权限

> yum install unzip
>
> unzip sonarqube-6.7.4.zip 解压
>
> mkdir /opt/sonar 创建目录
>
> mv sonarqube-6.7.4/* /opt/sonar 移动文件
>
> useradd sonar 创建sonar用户，必须sonar用于启动，否则报错
>
> chown -R sonar. /opt/sonar 更改sonar目录及文件权限

修改sonar配置文件

>vi /opt/sonarqube-6.7.4/conf/sonar.properties
>
>内容如下：
>
>sonar.jdbc.username=root sonar.jdbc.password=Root@123
>
>sonar.jdbc.url=jdbc:mysql://localhost:3306/sonar?
>
>useUnicode=true&characterEncoding=utf8&rewriteBatchedStatements=true&useConfifigs=
>
>maxPerformance&useSSL=false

注意：sonar■默认监听9000端口 ,如果9000端口被占用，需要更改。

启动sonar

> cd /opt/sonarqube-6.7.4
>
> su sonar ./bin/linux-x86-64/sonar.sh start 启动
>
> su sonar ./bin/linux-x86-64/sonar.sh status 查看状态
>
> su sonar ./bin/linux-x86-64/sonar.sh stop 停止
>
> tail -f logs/sonar.logs 查看日志

访问sonar

http://192.168.66.101:9000

![image-20210627012114461](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012114461.png)

默认账户:admin/admin

创建token

![image-20210627012134006](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012134006.png)

> bb8b6c53d9d921 e101343cef0395243e6c1dc8a3

token要记下来后面要使用

**0151ae8c548a143eda9253e4334ad030b56047ee**

### 3.6.2、实现代码审査

![image-20210627012311659](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012311659.png)

#### 3.6.2.1、安装SonarQube Scanner插件

![image-20210627012326304](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012326304.png)

#### 3.6.2.2、添加SonarQube凭证

![image-20210627012400973](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012400973.png)**Jenkins进行SonarQube 配置**

![image-20210627012538354](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012538354.png)

#### 3.6.2.3、SonaQube关闭审查结果上传到SCM功能

- ![image-20210627012621514](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012621514.png)

#### 3.6.2.4、在项目添加SonaQube代码审查（非流水线项目）

添加构建步骤：

![image-20210627012709960](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012709960.png)

#### 3.6.2.5、在项目添加SonaQube代码审查（流水线项目）

1 ）项目根目录下，创建sonar-project.properties文件

![image-20210627012736458](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012736458.png)

2）修改Jenkinsfifile，加入SonarQube代码审查阶段

![image-20210627012833579](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012833579.png)

3 ）到SonarQube的Ul界面查看审查结果

![image-20210627012851011](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627012851011.png)

# 4、Jenkins+Docker+SpringCloud微服务持续集成（上）

## 4.1、Jenkins+Docker+SpringCloud 持续集成流程说明

![image-20210627013025459](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627013025459.png)

大致流程说明：

1. ）开发人员每天把代码提交到Gitlab代码仓库
1. ） Jenkins从Gitlab中拉取项目源码,编译并打成jar包,然后构建成Docker镜像,将镜像上传到 Harbor私有仓库。
1. ） Jenkins发送SSH远程命令,让生产部署服务器到Harbor私有仓库拉取镜像到本地，然后创建容器。
1. ）最后，用户可以访问到容器

**服务列表**（红色的软件为需要安装的软件，黑色代表已经安装）

| **服务器名称**   | **IP地址**     | **安装的软件**                      |
| :--------------- | :------------- | :---------------------------------- |
| 代码托管服务器   | 192.168.66.100 | Gitlab                              |
| 持续集成服务器   | 192.168.66.101 | Jenkins , Maven z Dockerl 8.06.1-ce |
| Docker仓库服务器 | 192.168.66.102 | Dockerl8.06.1-ce , Harborl .9.2     |
| 服务器名称       | 192.168.66.103 | Docker18.06.1-ce                    |

## 4.2、SpringCloud微服务源码概述

项目架构:前后端分离

后端技术栈：SpringBoot+SpringCloud+SpringDataJpa（ Spring全家桶）

微服务项目结构：

![image-20210627013305175](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627013305175.png)

- tensquare\_parent :父工程,存放基础配置
- tensquare\_common :通用工程,存放工具类
- tensquare\_eureka\_server : SpringCloud的Eureka注册中心
- tensquare\_zuul : SpringCloud的网关服务
- tensqua re\_admin\_service :基础权限认证中心,负责用户认证*（*使用JWT认证）
- tensquare\_gathering : 一个简单的业务模块,活动微服务相关逻辑

数据库结构：

![image-20210627013332992](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627013332992.png)

- tensquare\_user :用户认证数据库，存放用户账户数据。对应tensquare\_admin\_service微服务
- tensquare\_gathering :活动微服务数据库。对应tensquarjgathering微服务

微服务配置分析：

- tensquare\_eureka
- tensquare\_zuul
- tensqua re\_a dmin\_service
- tensqua re\_gatheri ng

## 4.3、本地部署

### 4.3.1、SpringCloud微服务部署

**本地运行微服务**

1. ）逐一启动微服务
1. ）使用postman测试功能是否可用

**本地部署微服务**

1 ） SpringBoot微服务项目打包

必须导入该插件

![image-20210627013454036](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627013454036.png)

打包后在ta rget下产生jar包

2 ）本地运行瀕务的jar包

> java -jar xxx.jar

3）查看效果

### 4.3.2、前端静态web网站部署

前端技术栈：NodeJS+VueJS+ElementUI

使用Visual Studio Code打开源码

1. ）本地运行

   > npm run de

2. ）打包静态web网站

   > npm run build

   打包后，产生dist目录的静态文件

3. ）部署到nginx服务器

   把dist目录的静态文件拷贝到nginx的html目录，启动nginx

4. ）启动nginx ,并访问

<http://localhost:82>

## 4.4、环境准备

### 4.4.1、Docker快速入门

#### 4.4.1.1、Docker简介

![image-20210627013912051](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627013912051.png)

Docker是一个开源的应用容器引擎,基于Go语言并遵从Apache2.0协议开源。

Docker可以让开发者打包他们的应用以及依赖包到一个轻量级、可移植的容器中,然后发布到任何流 行的Linux机器上,也可以实现虚拟化。

容器是完全使用沙箱机制，相互之间不会有任何接口 （类似iPhone的app ）,更重要的是容器性能开销极低。

Docker容器技术 vs 传统虚拟机技术

![image-20210627013956003](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627013956003.png)

|                  | **虚拟机**                    | **容器**               |
| :--------------- | :---------------------------- | :--------------------- |
| **占用磁盘空间** | 非常大,GB级                   | 小,MB甚至KB级          |
| **启动速度**     | 慢,分钟级                     | 快，秒级               |
| **运行形态**     | 运行于Hypervisor上            | 直接运行在宿主机内核上 |
| **并发性**       | 一台宿主机上十几个,最多几十个 | 上百个,甚至数百上千个  |
| **性能**         | 逊于宿主机                    | 接近宿主机本地进程     |
| **资源利用率**   | 低                            | 高                     |

简单一句话总结：**Docker技术就是让我们更加高效轻松地将任何应用在Linux服务器部署和使用。**

#### 4.4.1.2、Docker安装

1）卸载旧版本

> yum list installed | grep docker 歹U出当前所有docker的
>
> yum -y remove docker的包名称卸载docker包
>
> rm -rf/var/lib/docker删除docker的所有镜像和容器

2）安装必要的软件包

> sudo yum install -y yum-utils \ device-mapper-persistent-data \ Ivm2

3）设置下载的镜像仓库

> sudo yum-config-manager \ -add-repo \ https://download.docker.com/linux/centos/docker-ce.repo

4）列出需要安装的版本列表

> yum list docker-ce -showduplicates | sort -r

![image-20210627014304576](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627014304576.png)5）安装指定版本（这里使用18.0.1版本)

> sudo yum install docker-ce-18.06.1 .ce

6）查看版本

> docker -v

7 ）启动Docker

> sudo systemctI start docker 启动
>
> sudo systemctI enable docker 设置开机启动

8）添加阿里云镜像下载地址

> vi /etc/docker/daemon.json

内容如下：

![image-20210627014352701](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627014352701.png)

9 ）重启Docker

> sudo systemctl restart docker

#### 4.4.1.3、Docker基本命令快速入门

1 ）镜像命令

镜像:相当于应用的安装包,在Docker部署的任何应用都需要先构建成为镜像

> docker search镜像名称搜索镜像
>
> docker pull镜像名称拉取镜像
>
> docker images查看本地所有镜像
>
> docker rmi -f镜像名称删除镜像
>
> docker pull openjdk:8-jdk-alpine

2）容器命令

容器:容器是由镜像创建而来。容器是Docker运行应用的载体,每个应用都分别运行在Docker的每个 容器中。

> docker run-i镜像名称:标签运行容器（默认是前台运行）
>
> docker ps查看运行的容器
>
> docker ps -a查询所有容器

常用的参数：

> -i :运行容器
>
> -d :后台守方式运行（守护式）
>
> --name :给容器添加名称
>
> -P :公开容器端口给当前宿主机
>
> -V :挂载目录



> docker exec -it容器ID/容器名称/bin/bash进入容器内部
>
> docker start/stop/restart容器名称/ID启动/停止/重启容器
>
> docker rm -f容器名称/ID删除容器

### 4.4.2、Dockerfile镜像脚本快速入门

#### 4.4.2.1、Dockerfile 简介

Dockerfile其实就是我们用来构建Docker镜像的源码,当然这不是所谓的编程源码,而是一些命令的组 合,只要理解它的逻辑和语法格式,就可以编写Dockerfile了。

简单点说，Dockerfile的作用：它可以让用户个性化定制Docker镜像。因为工作环境中的需求各式各 样，网络上的镜像很难满足实际的需求。

#### 4.4.2.2、Dockerfile常见命令

| **命令**                             | **作用**                                                     |
| :----------------------------------- | :----------------------------------------------------------- |
| FROM image\_name:tag                 |                                                              |
| MAINTAINER user\_name                | 声明镜像的作者                                               |
| ENV key value                        | 设置环境变量（可以写多条）                                   |
| RUN command                          | 编译镜像时运行的脚本（可以写多条）                           |
| CMD                                  | 设置容器的启动命令                                           |
| ENTRYPOINT                           | 设置容器的入口程序                                           |
| ADD source\_dir/file dest\_dir/file  | 将宿主机的文件复制到容器内,如果是一个压缩文件，将会在复 制后自动解压 |
| COPY source\_dir/file dest\_dir/file | 和ADD相似,但是如果有压缩文件并不能解压                       |
| WORKDIR path\_dir                    | 设置工作目录                                                 |
| ARG                                  | 设置编译镜像时加入的参数                                     |
| VOLUMN                               | 设置容器的挂载卷                                             |

镜像构建示意图：

![image-20210627014837086](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627014837086.png)

可以看到,新镜像是从基础镜像一层一层叠加生成的。每安装一个软件，就在现有镜像的基础上增加 	 层

-  RUN、CMD、ENTRYPOINT的区另!] ?

  RUN :用于指定docker build过程中要运行的命令,即是创建Docker镜像（image ）的步骤

  CMD :设置容器的启动命令,Dockerfile中只能有一条CMD命令,如果写了多条则最后一条生效, CMD不支持接收docker run的参数。

  ENTRYPOINT :入口程序是容器启动时执行的程序,docker run中最后的命令将作为参数传递给入口 程序,ENTRYPOINY类似于CMD指令，但可以接收docker run的参数。

以下是mysql官方镜像的Dockerfile示例：

![image-20210627014929835](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627014929835.png)

#### 4.4.2.3、使用Dockerfile制作微服务镜像

我们利用Dockerfile制作一个Eureka注册中心的镜像

1. ）上传Eureka的糊艮务jar包至Ulinux

1. ）编写Dockerfile

   ![image-20210627015022793](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627015022793.png)

1. ）构建镜像

   > docker build --build-arg JAR_FILE=tensquare_eureka_server-1.0-SNAPSHOT.jar -t eureka:v1 .

1. ）查看镜像是否创建成功

   > docker images

1. ）创建容器

   > docker run -i -name=eureka -p 10086:10086 eureka:v1

1. ）访问容器

   http://192.168.66.101:10086

### 4.4.3、Harbor镜像仓库安装及使用

4.7.1、Harbor简介
![image-20210627015659781](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627015659781.png)

Harbor （港口 ,港湾）是一个用于存储和分发Docker镜像的企业级Registry服务器。

除了Harbor这个私有镜像仓库之外,还有Docker官方提供的Registry。相对Registry , Harbor具有很 多优势：

1. 提供分层传输机制，优化网络传输Docker镜像是是分层的，而如果每次传输都使用全量文件（所以 用FTP的方式并不适合），显然不经济。必须提供识别分层传输的机制，以层的UUID为标识，确定 传输的对象。
1. 提供WEB界面，优化用户体验只用镜像的名字来进行上传下载显然很不方便,需要有一个用户界 面可以支持登陆、搜索功能，包括区分公有、私有镜像。
1. 支持水平扩展集群当有用户对镜像的上传下载操作集中在某服务器，需要对相应的访问压力作分 解。
1. 良好的安全机制企业中的开发团队有很多不同的职位，对于不同的职位人员，分配不同的权限， 具有更好的安全性。

#### 4.4.3.1、Harbor安装

Harbor需要安装在192.168.66.102上面

1. ）先安装Docker并启动Docker（已完成）

   参考之前的安装过程

2. ）先安装docker-compose

   >sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker- 
   >
   >compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose 
   >
   >sudo chmod +x /usr/local/bin/docker-compose

3. ）给docker-compose添加执行权限

   > sudo chmod +x /usr/local/bin/docker-compose

4. ）查看docker-compose是否安装成功

   > docker-compose -version

5. ）下载Harbor的压缩包（本课程版本为:v1.9.2 ）

   https://github.com/goharbor/harbor/releases

6. )上传压缩包到linux ,并解压

   > tar -xzf harbor-offlfflffline-installer-v1.9.2.tgz
   >
   > mkdir /opt/harbor
   >
   > mv harbor/* /opt/harbor
   >
   > cd /opt/harbor

7. 修改Harbor的配置

   > vi harbor.yml

8. ）安装Harbor

   > ./prepa re
   >
   > ./install.sh

9. ）启动Harbor

   >docker-compose up -d 启动
   >
   >docker-compose stop 停止 
   >
   >docker-compose restart 重新启动

10. ）访问Harbor

http://192.168.66.102:85

默认账户密码：admin/Harbor12345

![image-20210627020518380](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020518380.png)

#### 4.4.3.2、在Harbor创建用户和项目

1 )  创建项目

Harbor的项目分为公开和私有的：

公开项目:所有用户都可以访问,通常存放公共的镜像,默认有一个library公开项目。

私有项目：只有授权用户才可以访问,通常存放项目本身的镜像。

我们可以为微服务项目创建一个新的项目：

![image-20210627020651865](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020651865.png)

2）创建用户

![image-20210627020713076](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020713076.png)

![image-20210627020731893](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020731893.png)

创建的用户为：itcast/ltcast123

3）给私有项目分配用户

进Atensqua re项目-> 成员

![image-20210627020810261](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020810261.png)

![image-20210627020848146](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020848146.png)

| **角色**   | **权限说明**                                      |
| :--------- | :------------------------------------------------ |
| 访客       | 对于指定项目拥有只读权限                          |
| 开发人员   | 对于指定项目拥有读写权限                          |
| 维护人员   | 对于指定项目拥有读写权限，创建Webhooks            |
| 项目管理员 | 除了读与权限，同时拥有用户管理/镜像扫描等管理权限 |

4 ）以新用户登录Harbor

![image-20210627020907213](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020907213.png)

#### 4.4.3.3、把镜像上传到Harbor

1 ）给镜像打上标签

> docker tag eureka:v1 192.168.66.102:85/tensquare/eureka:v1

2）推送镜像

> docker push 192.168.66.102:85/tensquare/eureka:v1

![image-20210627020949381](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627020949381.png)

这时会岀现以上报错,是因为Docker没有把Harbor加入信任列表中

3 ）把Harbor地址加入到Docker信任列表

> vi /etc/docker/daemon.json

![image-20210627021045344](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021045344.png)

​	需要重启Docker

4）再次执行推送命令,会提示权限不足

> denied: requested access to the resource is denied 

​	需要先登录Harbor,再推送镜像

5 ）登录Harbor

> docker login -u 用户名-p 密码 192.168.66.102:85

![image-20210627021137709](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021137709.png)

![image-20210627021153460](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021153460.png)

#### 4.4.3.4、从Harbor下载镜像

需求：在192.168.66.103服务器完成从Harbor下载镜像

1. ）安装Docker,并启动Docker （已经完成）

1. ）修改Docker配置

   > vi /etc/docker/daemon.json

   ![image-20210627021351538](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021351538.png)

1. ）先登录，再从Harbor下载镜像

> docker login -u 用户名-p 密码 192.168.66.102:85

> docker pull 192.168.66.102:85/tensquare/eureka:v1

## 4.5、微服务持续集成

### 4.5.1、项目代码上传到Gitlab

![image-20210627021545898](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021545898.png)

### 4.5.2、从Gitlab拉取项目源码

1 )创建Jenkinsfile文件

![image-20210627021806139](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021806139.png)

2 ）拉取Jenkinsfile文件

![image-20210627021832552](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627021832552.png)

### 4.5.3、提交到SonarQube代码审查

1 ）创建项目,并设置参数

![image-20210627022011030](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022011030.png)

2 ）每个项目的根目录下添加sonar-project.properties

![image-20210627022031011](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022031011.png)

注意：修改sonar.projectKey和sonar.projectName

3 )修改Jenkinsfile构建脚本

![image-20210627022057320](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022057320.png)

### 4.5.4、使用Dockerfile编译、生成镜像

利用 dockerfile-maven-plugin 插件构建 Docker!竟像

1. ) 在每个微S艮务项目的pom.xml加入dockerfile-maven-plugin插件

![image-20210627022149572](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022149572.png)

2. )在每个微0艮务项目根目录下建立Dockerfile文件

   ![image-20210627022241360](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022241360.png)

   注意：每个项目公开的端口不一样

3. )修改Jenkinsfile构建脚本

![image-20210627022313745](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022313745.png)

注意:如果出现找不到父工程依赖,需要手动把父工程的依赖上传到仓库中

### 4.5.5、上传到Harbor镜像仓库

1 )修改Jenkinsfile构建脚本

/![image-20210627022437786](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022437786.png)

![image-20210627022449382](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022449382.png)

2 )使用凭证管理Harbor私鼬户和密码

先在凭证建立Harbor的凭证，在生成凭证脚本代码

![image-20210627022510724](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022510724.png)

### 4.5.6、拉取镜像和发布应用

![image-20210627022542739](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022542739.png)

注意：192.168.66.103服务已经安装Docker并启动

**安装 Publish Over SSH 插件** 

![image-20210627022601690](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022601690.png)

**配置远程部署服务器**

1）拷贝公钥到远程服务器

> ssh-copy-id 192.168.66.103

2 ）系统配置-＞添加远程服务器

![image-20210627022633112](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022633112.png)


**修改Jenkinsfile构建脚本**

生成远程调用模板代码

![image-20210627022725448](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022725448.png)

添加一个port参数

![image-20210627022751033](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627022751033.png)

![image-20210627023002535](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023002535.png)

![image-20210627023028610](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023028610.png)

![image-20210627023109503](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023109503.png)

**编写deploy.sh部署脚本**

![image-20210627023445620](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023445620.png)

![image-20210627023504056](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023504056.png)

上传deploy.sh文件到/opt/jenkins\_shell目录下,且文件至少有执行权限！

> chmod +x deploy.sh添加执行权限

**导入数据，测试微服务**

![image-20210627023530923](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023530923.png)

### 4.5.7、部署前端静态web网站

![image-20210627023617029](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023617029.png)

#### 4.5.7.1、安装Nginx服务器

> yum install epel-release
>
> yum -y install nginx 安装

修改nginx的端口 ,默认80 ,改为9090 :

> vi /etc/nginx/nginx.conf

![image-20210627023649856](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023649856.png)

还需要关闭selinux ,将SELINUX=disabled

> setenforce 0先临时关闭

> vi /etc/selinux/config 编辑文件,永久关闭 SELINUX二disabled

启动Nginx

> systemctl enable nginx 设置开机启动
>
> systemctl start nginx 启动
>
> systemctl stop nginx 停止
>
> systemctl restart nginx 重启

访问：http://192.168.66.103:9090/

![image-20210627023803049](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023803049.png)

#### 4.5.7.2、安装NodeJS插件

![image-20210627023906132](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023906132.png)



#### 4.5.7.3、Jenkins配置Nginx服务器

Manage Jenkins->Globa I Tool Configuration

![image-20210627023932133](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627023932133.png)



#### 4.5.7.4、创建前端流水线项目

![image-20210627024134980](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024134980.png)

![image-20210627024144655](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024144655.png)

#### 4.5.7.5、建立Jenkinsfile构建脚本

/![image-20210627024206968](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024206968.png)

完成后，访问：http://192.168.66.103:9090 进行测试。

# 5、Jenkins+Docker+SpringCloud微服务持续集成(下)

## 5.1、Jenkins+Docker+SpringCloud部署方案优化

上面部署方案存在的问题:

1）一次只能选择一个微服务部署

2）只有一台生产者部署服务器

3）每个微服务只有一个实例,容错率低

优化方案:

1. ）在一个Jenkins工程中可以选择多个微服务同时发布
1. ）在一个Jenkins工程中可以选择多台生产服务器同时部署
1. ）每个微服务都是以**集群高可用**形式部署

## 5.2、Jenkins+Docker+SpringCloud集群部署流程说明


![image-20210627024502740](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024502740.png)

## 5.3、修改所有微服务配置

### 5.3.1、注册中心配置（\*）

![image-20210627024616029](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024616029.png)

在启动微服务的时候，加入参数: **spring.profifiles.active** 来读取对应的配置

### 5.3.2、其他微服务配置

除了Eureka注册中心以外,其他微服务配置都需要加入所有Eureka服务

![image-20210627024732230](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024732230.png)

把代码提交到Gitlab中

## 5.4、设计Jenkins集群项目的构建参数

### 5.4.1、安装Extended Choice Parameter插件

支持多选框

![image-20210627024838962](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024838962.png)

### 5.4.2、创建流水线项目

![image-20210627024852526](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024852526.png)

### 5.4.3、添加参数

字符串参数:分支名称

![image-20210627024913339](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024913339.png)

多选框：项目名称

![image-20210627024924945](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024924945.png)

![image-20210627024936535](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627024936535.png)

### 5.4.4、最后效果

![image-20210627025042509](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025042509.png)

## 5.5、完成微服务构建镜像，上传私服

![image-20210627025130962](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025130962.png)

![image-20210627025144397](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025144397.png)

![image-20210627025209031](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025209031.png)

![image-20210627025231539](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025231539.png)

## 5.6、完成微服务多服务器远程发布

### 5.6.1、配置远程部署服务器

- 拷贝公钥到远倒艮务器


> ssh-copy-id 192.168.66.104

- 系统配置-> 添加远倒艮务器


![image-20210627025327573](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025327573.png)

### 5.6.2、修改Docker配置信任Harbor私服地址

![image-20210627025400705](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025400705.png)

重启Docker

### 5.6.3、添加参数

多选框：部署服务器


![image-20210627025437983](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025437983.png)

![image-20210627025450976](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025450976.png)

最终效果

![image-20210627025530772](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025530772.png)

### 5.6.4、修改Jenkinsfile构建脚本

![image-20210627025658494](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025658494.png)

![image-20210627025715096](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025715096.png)

![image-20210627025735563](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025735563.png)

![image-20210627025754708](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025754708.png)

### 5.6.5、编写deployCluster.sh部署脚本

![image-20210627025845033](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025845033.png)

![image-20210627025855546](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025855546.png)

### 5.6.6、集群效果

**Nginx+Zuul集群实现高可用网关**

![image-20210627025953239](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627025953239.png)

1. ）安装Nginx （已完成）

2. ）修改Nginx配置
   
   > vi /etc/nginx/nginx.conf
   
   ​	内容如下：

![image-20210627030029436](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030029436.png)

![image-20210627030037445](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030037445.png)

3. ）重启Nginx : systemctI restart nginx

4. ）修改前端Nginx的访问地址

   ![image-20210627030258502](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030258502.png)



# 6、基于Kubernetes/K8S构建Jenkins持续集成平台(上)

## 6.1、Jenkins 的 Master-Slave 分布式构建

### 6.1.1、什么是Master-Slave分布式构建


![image-20210627030514105](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030514105.png)

Jenkins的Master-Slave分布式构建,就是通过将构建过程分配至11从属Slave节点上,从而减轻Master节 点的压力,而且可以同时构建多个,有点类似负载均衡的概念。

### 6.1.2、如何实现Master-SIave分布式构建 

#### 6.1.2.1 、 开启代理程序的TCP端口

![image-20210627030625125](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030625125.png)

#### 6.1.2.2 、 新建节点

![image-20210627030647793](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030647793.png)

![image-20210627030658967](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030658967.png)

有两种在Slave节点连接Master节点的方法

![image-20210627030720450](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030720450.png)

我们选择第二种:

#### 6.1.2.3 、 安装和配置节点

下载agent.jar,并上传到Slave节点,然后执行页面提示的命令：

![image-20210627030910842](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030910842.png)

刷新页面

![image-20210627030943932](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627030943932.png)

#### 6.1.2.4 、测试节点是否可用

自由风格和Maven风格的项目：

![image-20210627031035753](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627031035753.png)

流水线风格的项目：

![image-20210627031053032](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627031053032.png)

## 6.2、Kubernetes实现Master-SIave分布式构建方案

### 6.2.1、传统Jenkins的Master-Slave方案的缺陷

- Master节点发生单点故障时,整个流程都不可用了


- 每个Slave节点的配置环境不一样，来完成不同语言的编译打包等操作,但是这些差异化的配置导 致管理起来非常不方便，维护起来也是比较费劲


- 资源分酉环均衡，有的Slave节点要运行的job出现排队等待，而有的Slave节点处于空闲状态


- 资源浪费,每台Slave节点可能是实体机或者VM ,当Slave节点处于空闲状态时,也不会完全释放 掉资源


以上种种问题,我们可以弓I入Kubernates来解决！

### 6.2.2、Kubernates 简介

​		Kubernetes (简称,K8S )是Google开源的容器集群管理系统，在Docker技术的基础上,为容器化的 应用提供部署运行、资源调度、服务发现和动态伸缩等一系列完整功能,提高了大规模容器集群管理的 便捷性。其主要功能如下：

- 使用Docker对应用程序包装(package)、实例化(instantiate)、运行(run)。


- 以集群的方式运行、管理跨机器的容器。以集群的方式运行、管理跨机器的容器。


- 解决Docker跨机器容器之间的通讯问题。解决Docker跨机器容器之间的通讯问题。


- Kubernetes的自我修复机制使得容器集群总是运行在用户期望的状态。


### 6.2.3、Kubernates+Docker+Jenkins 持续集成架构图

![image-20210627031524073](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627031524073.png)

![image-20210627031531942](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627031531942.png)

​		大致工作流程：手动/自动构建-> Jenkins调度K8S API - >动态生成Jenkins Slave pod - > Slave pod 拉取Git代码/编译/打包镜像->推送到镜像仓库Harbor-> Slave工作完成,Pod自动销毁->部署 到测试或生产Kubernetes平台。(完全自动化,无需人工干预)

### 6.2.4、Kubernates+Docker+Jenkins 持续集成方案好处

- 服务高可用：当Jenkins Master出现故障时，Kubernetes会自动创建一个新的Jenkins Master 容器,并且将Volume分配给新创建的容器,保证数据不丢失,从而达到集群服务高可用。


- 动态伸缩，合理使用资源：每次运行Job时,会自动创建一个Jenkins Slave , Job完成后,Slave 自动注销并删除容器,资源自动释放,而且Kubernetes会根据每个资源的使用情况,动态分配 Slave到空闲的节点上创建,降彳氐出现因某节点资源利用率高,还排队等待在该节点的情况。


- 扩展性好:当Kubernetes集群的资源严重不足而导致Job排队等待时，可以很容易的添加一个 Kubernetes Node到集群中，从而实现扩展。


## 6.3、Kubeadm 安装 Kubernetes

### 6.3.1、Kubernetes 的架构

![image-20210627031746504](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627031746504.png)

- API Server :用于暴露Kubernetes API ,任何资源的请求的调用操作都是通过kube-apiserver提供的接 口进行的。


- Etcd :是Kubernetes提供默认的存储系统，保存所有集群数据，使用时需要为etcd数据提供备份计 划。


- Controller-Manager :作为集群内部的管理控制中心，负责集群内的Node、Pod副本、服务端点(Endpoint)、命名空间(Namespace )、服务账号(ServiceAccount)、资源定额(ResourceQuota )的管理，当某个Node意外宕机时，Controller Manager会及时发现并执行自动化 修复流程,确保集群始终处于预期的工作状态。


- Scheduler :监视新创建没有分配至！iNode的Pod ,为Pod选择一个Node。


- Kubelet :负责维护容器的生命周期，同时负责Volume和网络的管理


- Kube proxy :是Kubernetes的核心组件，咅B署在每个Node节点上,它是实现Kubernetes Service的通 信与负载均衡机制的重要组件。


### 6.3.2、安装环境说明

| **主机名称**      | **IP地址**     | **安装的软件**                                               |
| :---------------- | :------------- | :----------------------------------------------------------- |
| 代码托管服 务器   | 192.168.66.100 | Gitlab-12.4.2                                                |
| Docker仓库 服务器 | 192.168.66.102 | Harbor1.9.2                                                  |
| k8s-master        | 192.168.66.101 | kube-apiservers kube-controller-managers kube- scheduler. docker、etcd、calico , NFS |
| k8s-node1         | 192.168.66.103 | kubelet. ku be proxy s Dockerl 8.06.1 -ce                    |
| k8s-node2         | 192.168.66.104 | kubelet、ku be proxy s Dockerl 8.06.1-ce                     |

### 6.3.3、三台机器都需要完成

- 修改三台机器的hostname及hosts文件

  > hhostnamectl set-hostname k8s-master 
  >
  > hostnamectl set-hostname k8s-node1 hostnamectl set-hostname k8s-node2

  >cat >>/etc/hosts<<EOF 192.168.66.101 k8s-master 192.168.66.103 k8s-node1
  >
  >192.168.66.104 k8s-node2 EOF

- 关闭防火墙和关闭SELinux

  > systemctI stop firewalld
  >
  > systemctl disable firewalld
  >
  > setenforce 0临时关闭
  >
  > vi /etc/sysco nfig/sel i nux 永久关闭

  改为 SELINUX二disabled

- 设置系统参数

  设置允许路由转发，不对bridge的数据进行处理

  - 创建文件

  > vi /etc/sysctl.d/k8s.conf
  >
  > 内容如下：
  >
  > net.bridge.bridge-nf-call-ip6tables = 1 net.bridge.bridge-nf-call-iptables = 1
  >
  > net.ipv4.ip_forward = 1 vm.swappiness = 0

  - 执行文件

  > sysctl -p /etc/sysctl.d/k8s.conf

- kube-proxy开启ipvs的前置条件


![image-20210627032359799](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627032359799.png)

- 所有节点关闭swap

  > swapoff -a临时关闭
  >
  > vi /etc/fstab永久关闭
  >
  > 注释掉以下字段
  >
  > /dev/mapper/cl-swap swap swap defaults 0 0

- 安装kubelet、kubeadm、kubectl

  - kubeadm:用来初始化集群的指令。

  - kubelet:在集群中的每个节点上用来启动pod和container等。

  - kubectl:用来与集群通信的命令行工具。

清空yum缓存

> yum clean all

设置yum安装源

![image-20210627032627094](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627032627094.png)

安装：

> yum i nstal1 -y kubelet kubeadm kubectl

kubelet设置开机启动（注意：先不启动，现在启动的话会报错）

> systemctl enable kubelet

查看版本

> kubelet --version

安装的是最新版本:Kubernetes v1.16.3 （可能会变化）

### 6.3.4、Master节点需要完成

#### 1 ）运行初始化命令

![image-20210627032951462](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627032951462.png)

注意:apiserver-advertise-address这个地址必须是master机器的IP

常用错误：

错误一 :[WARNING IsDockerSystemdCheck]: detected "cgroupfs" as the Docker cgroup driver

作为Docker cgroup驱动程序。Kubernetes推荐的Docker驱动程序是“systemd”

解决方案：修改Docker的酉己置:vi /etc/docker/daemon.json ,加入

![image-20210627033040341](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033040341.png)

然后重启Docker

错误二：[ERROR NumCPU]: the number of available CPUs 1 is less than the required 2

解决方案：修改虚拟机的CPU的个数，至少为2个

![image-20210627033132772](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033132772.png)

安装过程日志：

![image-20210627033200491](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033200491.png)


最后，会提示节点安装的命令，必须记下来

![image-20210627033215219](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033215219.png)

#### 2 )  启动kubelet

> systemctl restart kubelet

![image-20210627033311453](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033311453.png)

#### 3）配置kubectl工具

![image-20210627033335908](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033335908.png)

#### 4)   安装Calico

![image-20210627033352984](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033352984.png)

#### 5 ）查看所有Pod的状态

等待几分钟，查看所有Pod的状态，确保所有Pod都是Running状态

> kubectl get pod --all-namespaces -o wide

![image-20210627033525055](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033525055.png)

### 6.3.5、Slave节点需要完成

#### 1 ）让所有节点让集群环境

使用之前Master节点产生的命令加入集群

![image-20210627033616634](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033616634.png)

#### 2 )  启动kubelet

> systemctl start kubelet

![image-20210627033645544](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033645544.png)

#### 3 ）Master节点査看

回到Master节点査看，如果Status全部为Ready，代表集群环境搭建成功! ! !

> kubectl get nodes

![image-20210627033740834](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033740834.png)

### 6.3.6、kubectl常用命令

> kubectl get nodes 查看所有主从节点的状态 
>
> kubectl get ns 获取所有namespace资源 
>
> kubectl get pods -n {$nameSpace} 获取指定namespace的pod 
>
> kubectl describe pod的名称 -n {$nameSpace} 查看某个pod的执行过程 
>
> kubectl logs --tail=1000 pod的名称 | less 查看日志 
>
> kubectl create -f xxx.yml 通过配置文件创建一个集群资源对象 
>
> kubectl delete -f xxx.yml 通过配置文件删除一个集群资源对象 
>
> kubectl delete pod名称 -n {$nameSpace} 通过pod删除集群资源 
>
> kubectl get service -n {$nameSpace} 查看pod的service情况

# 7、基于Kubernetes/K8S构建Jenkins持续集成平台(下)

Jenkins-Master-Slave架构图回顾：

![image-20210627033950864](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627033950864.png)

## 7.1、安装和配置NFS

### 7.1.1、NFS简介

NFS ( Network File System ),它最大的功能就是可以通过网络,让不同的机器、不同的操作系统可以 共享彼此的文件。我们可以利用NFS共享Jenkins运行的配置文件、Maven的仓库依赖文件等

### 7.1.2、NFS安装

我们把NFS服务器安装在192.168.66.101机器上

1）安装NFS服务（在所有K8S的节点都需要安装）

> yum install -y nfs-utils

2）创建共享目录

> mkdir -p /opt/nfs/jenkins 
>
> vi /etc/exports 编写NFS的共享配置 
>
> 内容如下: 
>
> /opt/nfs/jenkins *(rw,no_root_squash) *代表对所有IP都开放此目录，rw是读写

3 )  启动服务

> systemctl enabl e nfs 开机启动 systemctl start nfs 启动

4）查看NFS共享目录

> showmount -e 192.168.66.101

## 7.2、在 Kubernetes 安装Jenkins-Master

### 7.2.1、创建NFS client provisioner

​		nfs-client-provisioner 是一个Kubernetes的简易NFS的外部provisioner,本身不提供NFS ,需要现有 的NFS服务器提供存储。

1 )上传nfs-client-provisioner构建文件

![image-20210627034306222](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034306222.png)

其中注意修改deployment.yaml，使用之前配置NFS服务器和目录

![image-20210627034329181](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034329181.png)

2 ）构建nfs-client-provisioner的pod资源

> cd nfs-cli ent 
>
> kubectl create -f .

3 ）查看pod是否创建成功

![image-20210627034451731](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034451731.png)

### 7.2.2、安装Jenkins-Master

#### 1 ）上传Jenkins-Master构建文件

![image-20210627034556721](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034556721.png)

其中有两点注意:

第一、在StatefulSet.yaml文件，声明了利用nfs-client-provisioner进行Jenkins-Master文件存储

![image-20210627034621319](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034621319.png)

第二、Service发布方法采用NodePort,会随机产生节点访问端口

![image-20210627034643446](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034643446.png)

#### 2 ) 创建kube-ops的namespace

因为我们把Jenkins-Master 的 pod 放到 kube-opsT

> kubectl create namespace kube-ops

3 )构建Jenkins-Master的pod资源

> cd jenkins-master kubectl create -f .

4 ）查看pod是否创建成功

> kubectl get pods -n kube-ops

5 ）查看信息，并访问

​	查看Pod运行在那个Node±

> kubectl describe pods -n kube-ops

![image-20210627034759719](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034759719.png)

​	查看分配的端口

> kubectl get service -n kube-ops

![image-20210627034920367](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034920367.png)

​	最终访问地址为：http://192.168.66.103:30136 （192.168.66.103为k8s-node1的IP）

![image-20210627034950772](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627034950772.png)

​	安装过程跟之前是一样的！

6）先安装基本的插件

- Localization:Chinese
- Git
- Pipeline
- Extended Choice Parameter

## 7.3、Jenkins 与 Kubernetes 整合

### 7.3.1、安装Kubernetes插件

系统管理->插件管理->可选插件

![image-20210627035243269](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035243269.png)

### 7.3.2、实现Jenkins与Kubernetes整合

系统管理-> 系统配置-> 云-> 新建云-> Kubernetes

![image-20210627035359690](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035359690.png)


- kubernetes地用了kube白勺月艮务器发现:<https://kubemetes.default.svc.cluster.local>
- namespace填kube-ops ,然后点击Test Connection ,如果出现 Connection test successful 的提 示信息证明Jenkins已经可以和Kubernetes系统正常通信
- Jenkins URL 地址：http://jenkins.kube-ops.svc.cluster.local:8080

## 7.4、构建Jenkins-Slave自定义镜像

Jenkins-Master在构建Job的时候,Kubernetes会创建Jenkins-Slave的Pod来完成Job的构建。我们选择 运行Jenkins・Slave的镜像为官方推荐镜像:jenkins/jnlp-slave:latest,但是这个镜像里面并没有Maven 环境，为了方便使用,我们需要自定义一个新的镜像：

准备材料：

![image-20210627035559896](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035559896.png)

Dockerfile文件内容如下：

![image-20210627035613708](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035613708.png)

构建出一个新镜像:jenkins-slave-maven:latest

然把镜像上传到Harbor的公共库library中

![image-20210627035644827](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035644827.png)

## 7.5、测试Jenkins-Slave是否可以创建

### 7.5.1、创建一个Jenkins流水线项目

![image-20210627035725804](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035725804.png)

### 7.5.2、编写Pipeline ,从Gltlab拉取代码

![image-20210627035748471](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035748471.png)

### 7.5.3、查看构建日志

![image-20210627035833957](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035833957.png)

## 7.6、Jenkins+Kubernetes+Docker完成微服务持续集成

### 7.6.1、拉取代码,构建镜像

#### 1 ）创建NFS共享目录

![image-20210627035943125](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627035943125.png)

#### 2 ）创建项目,编写构建Pipeline

![image-20210627040056405](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040056405.png)

![image-20210627040115782](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040115782.png)

![image-20210627040142673](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040142673.png)

注意:在构建过程会发现无法创建仓库目录，是因为NFS共享目录权限不足,需更改权限

> chown -R jenkins:jenkins /opt/nfs/maven
>
> chmod -R 777 /opt/nfs/maven

还有Docker命令执行权限问题

> chmod 777 /var/run/docker.sock

需要手动上传父工程依赖到NFS的Maven共享仓库目录中

![image-20210627040248135](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040248135.png)

### 7.6.2、微服务部署到K8S

修改每个微0艮务的application.yml

Eureka

![image-20210627040406015](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040406015.png)

其他微服务需要注册到所有Eureka中

![image-20210627040421066](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040421066.png)

#### 1 ）安装Kubernetes Continuous Deploy插件

![image-20210627040447323](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040447323.png)

#### 2）修改后的流水线脚本

![image-20210627040503396](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040503396.png)

#### 3 ）建立k8s认证凭证

![image-20210627040519818](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040519818.png)

​	kubeconfifig到k8s的Master节点复制

> cat /root/.kube/config 

#### 4 )  生成Docker凭证

Docker凭证，用于Kubernetes至"Docker私服拉取镜像

![image-20210627040614169](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040614169.png)

#### 6 )  在每个项目下建立deploy.xml

Eureka 的 deply.yml

![image-20210627040656368](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040656368.png)

其他项目的deploy.yml主要把名字和端口修改：

![image-20210627040737016](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040737016.png)

#### 7 ）项目构建后，查看服务创建情况

> kubectl get pods -owide 
>
> kubectl get service

效果如下:

![image-20210627040826342](https://github.com/HymesZhao/StudyNotes/blob/master/Jekins/JenkinsPic/image-20210627040826342.png)







































