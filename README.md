## redis admin
Redis Admin是一个Redis管理平台，主要用于方便查看Key信息。

目前支持`单机Redis`和`Redis Cluster`模式

如果您有好的建议或需求欢迎私信

## 相关文档
**[blong](https://www.centoscn.vip/5321.html)**


## 截图

![](https://github.com/cncentoscn/redis/blob/master/static/img/1.png)
![](https://github.com/cncentoscn/redis/blob/master/static/img/2.png)
![](https://github.com/cncentoscn/redis/blob/master/static/img/3.png)


## 配置文件说明
项目配置文件说明
DEBUG
值:True/False
开启debug模式，使用请将其改为False

LOG_LEVEL
值:ERROR/WARNING/INFO/DEBUG 日志级别

socket_timeout
值: 2,数字 连接redis超时时间

scan_batch
值: 10000,数字 如果redis key过多避免导致性能问题，key列表最多获取值

mail_host
邮箱smtp服务器地址

mail_user
邮箱用户

mail_pass
邮箱密码

mail_receivers
邮件接收者

admin_mail
管理员邮箱

数据库信息
database = {
    "name": "redis_admin", //数据库名称
    "host": "127.0.0.1",   //连接地址
    "username": "root",    //用户名
    "password": "root",    //密码
    "port": "3306",        //端口
}

## redis管理
添加redis
名称: 单机redis请注意唯一性, cluster请一致性
主机: redis主机地址
端口: redis端口
DB数: 请保持和redis配置文件中db数量一致
密码: 如redis有密码请填写
如redis为cluster模式，请添加多个redis，名称保持一致并勾选类型为cluster

添加配置后请为用户配置redis权限，被授权用户需要退出登陆方可看的左侧菜单栏显示

编辑redis
这里只需要点击单元格信息即可进行修改，编辑按钮是为了提示信息

##左侧菜单栏

收到很多反馈左侧菜单栏没有信息，在此说声抱歉，忘记说明了。

左侧菜单栏和权限相关联并进行了本地缓存，配置了redis后需要在用户管理中给相应用户授权，被授权用户需要退出重新登陆即可看到左侧菜单栏

## 用户管理

这里可对用户进行管理，如添加，编辑，删除用户

重点: 添加redis配置后需要在此编辑用户，为用户授权redis并退出登陆后才可看到右侧菜单栏信息


