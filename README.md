ctrl+t
### 为什么选择 Jenkins 及 如何使用
---
### 一、选择 Jenkins 的原因
##### 通过 GoCD , TeamCity , Jenkins对比 ，选用了 Jenkins 理由有下面几条
* Jenkins 开源
* Jenkins 可以创建无数个 Slave 为你工作，而不像 TC 一样，想要增加 Slave 就必须要
升级为商业版
* Jenkins Slave 启动工作不像 GoCD 一样需要花费不知名的若干分钟的 不知道在做什么>的准备时间
* Jenkins 可以使用 pipeline 写脚本，且并行 Job， 这任何可以并行的自动化，都节省了非常多的时间

##### 说了无数 Jenkins 的好处 ， 那就说一下它的缺点
* Jenkins 的 Slave 存在已知的内存泄漏问题
* Jenkins 有时 JOb 会卡死无法运行

### 二、Jenkins 安装及升级

* 准备环境
* CentOS 6.2
* jenkins-2.19.4-1.1 稳定版
* 备注： 上述为博主自己使用过的版本， 大家可以选用自己合适的版本安装

##### Jenkins 常用安装方式有两种
* 可以下载 .war 包使用命令行安装

`Run java -jar jenkins.war --httpPort=8080`
##### 在浏览其中打开下面网址，就可以进行 Jenkins 网页浏览
`http://localhost:8080`
##### 其中网址可以根据需求自行配置

* 可以下载 rpm 包后使用 rpm 安装命令安装

##### 安装软件执行
`rpm -ivh rpm包名`

##### 安装jenkins并查看jenkins安装产生的文件，如下：
`rpm -ivh jenkins-2.19.4-1.1.noarch.rpm`

`rpm -ql jenkins-2.19.4-1.1.noarch`

#### 升级软件执行
`rpm -Uvh rpm包名`

##### 升级 Jenkins 时，最好选用长期稳定版本
##### 下载地址：[https://pkg.jenkins.io/redhat-stable/]
