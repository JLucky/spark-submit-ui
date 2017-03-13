# spark-submit-ui
这是一个基于playframwork开发，web管理spark应用的程序

你需要安装SBT和Java以及PlayFramowrk。这个项目基于2.2.x 版本开发，需要PlayFramowrk 2.2或更高版本。

#### 并下载并安装Play Framework 编译环境
 [Installing Play](https://www.playframework.com")


#### 修改配置文件，将集群地址替换为你的
文件路径在
<pre>conf/web-site.conf</pre>

#### 编译与运行
<pre> activator run </pre>
然后再 http://localhost:9000 查看正在运行的服务器。

如果运行有这个界面提示，点击Apply this script now 初始化数据表
 ![](http://upload-images.jianshu.io/upload_images/522641-65dbf16c874c1289.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#### 项目默认使用H2数据库
这是Play 内嵌的一个数据库 H2
[H2数据库]("http://www.h2database.com/html/main.html")

如果想要换成Mysql或者是其他的存储可以参考指引
<b>MySQL 数据库引擎连接属性
配置文件 conf/application.conf
</b>
<pre>
db.default.driver=com.mysql.jdbc.Driver
db.default.url="jdbc:mysql://localhost/playdb"
db.default.user=playdbuser
db.default.pass="a strong password" </pre>


#其他

通过界面管理，kill或者rerun任务
![](http://upload-images.jianshu.io/upload_images/522641-8bc5a35a895f944e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

如果你的提交参数或配置导致异常，可以在提交时查看
![QQ20170313-171709@2x.png](http://upload-images.jianshu.io/upload_images/522641-f06c579d508dc53d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<b>更详细的日志信息可以在logs下的文件查看</b>


spark-submit-ui: https://github.com/kingekinge/spark-submit-ui 
playframework:https://www.playframework.com


