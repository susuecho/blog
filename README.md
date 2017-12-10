# Jenkins 服务器构建

## 在所有经过的自动化构建项目中，使用过 GoCD , TeamCity , Jenkins, 三者对比，至少现在选用了 Jenkins 理由有下面几条
* Jenkins 开源，
* Jenkins 可以创建无数个 Slave 为你工作，而不像 TC 一样，想要增加 Slave 就必须要升级为商业版
* Jenkins Slave 启动工作不像 GoCD 一样需要花费不知名的若干分钟的 不知道在做什么的准备时间
* Jenkins 可以使用 pipeline 写脚本，且并行 Job， 这任何可以并行的自动化，都节省了非常多的时间

### 说了无数 Jenkins 的好处 ， 那就说一下它的缺点
* Jenkins 的 Slave 存在已知的内存泄漏问题
* Jenkins 有时 JOb 会卡死无法运行

### 上面利弊已经澄清，下面就介绍一下如何在服务器端安装 Jenkins 及 如何升级

### Jenkins 服务器搭建

#### 根据官方文档， Jenkins 的搭建可以使用很多种方式，
* 可以使用命令行安装
`Run java -jar jenkins.war --httpPort=8080`
#### 在浏览其中打开下面网址，就可以进行 Jenkins 网页浏览
`http://localhost:8080`
#### 其中网址可以根据需求自行配置

* 可以下载 rpm 包后使用 rpm 安装命令安装，RMP 是 LINUX 下的一种软件的可执行程序，你只要安装它就可以了。这种软件安装包通常是一个RPM包（Redhat Linux Packet Manager，就是Redhat的包管理器），后缀是.rpm。
#### 安装软件执行
`rpm -ivh rpm包名`

#### 安装jenkins并查看jenkins安装产生的文件，如下：
`rpm -ivh jenkins-2.19.4-1.1.noarch.rpm`
`rpm -ql jenkins-2.19.4-1.1.noarch`

#### 升级软件执行
`rpm -Uvh rpm包名`

#### 升级 Jenkins 时，最好选用长期稳定版本， 节省踩坑的时间，可根据自己需求惊醒升级
#### [下载地址：]() [https://pkg.jenkins.io/redhat-stable/】
