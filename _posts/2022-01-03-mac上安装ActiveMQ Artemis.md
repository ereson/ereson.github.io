# mac上安装ActiveMQ Artemis


## 缘由
我在看《spring实战》这本书的第8章异步发送消息的JMS部分时，添加好pom文件的依赖后，书上说了自己安装artemis，他就不赘述了。我想这应该不难，然后我就在网上搜了下“如何在mac上安装artemis“，然后就出现了一堆”在windows上安装artemis““mac如何在docker上安装artemis”“mac上安装ActiveMQ”。。。就是没有出现我想要的东西。然后我就尝试这用windows的方式在mac上安装artemis,最后就慢慢摸索出来了。

## 什么是ActiveMQ Artemis
其实，ActiveMQ Artemis就是ActiveMQ的更新版本，两者在使用上并没有太大的区别，唯一需要注意的是两者配置代理的位置和凭证信息的属性是不太一样的。

配置Artemis代理的位置和凭证信息的属性
 |属性 | 描述 |
 | -----   | ----    |
 | spring.artemis.host | 代理的主机|
 | spring.artemis.port | 代理的端口，默认为61616 |
 | spring.artemis.user | 用来访问代理的用户     |
 | spring.artemis.password  | 用来访问代理的密码|

配置ActiveMQ代理的位置和凭证信息的属性
 |属性 | 描述 |
 | -----   | ----    |
 | spring.activemq.broker.url | 代理的URL|
 | spring.activemq.user | 用来访问代理的用户 |
 | spring.activemq.in-memory |   是否启用在内存中运行的代理（默认为true   |
 | spring.activemq.password  | 用来访问代理的密码|


 ## 在mac上安装ActiveMQ Artemis

1. 首先在[点击进入官网下载](https://activemq.apache.org/components/artemis/download/)
2. 点击下载，[![TbflTJ.png](https://s4.ax1x.com/2022/01/03/TbflTJ.png)](https://imgtu.com/i/TbflTJ)
3. 解压到指定目录后，
    `cd Users/**/**/apache-artemis-2.20.0/bin`
,其中`**/**/`是需要你填写自己本地的路径,然后输入`./artemis create /Users/xiongwei/artemisbroker --user mq --password 123`,
[![TbfxAJ.png](https://s4.ax1x.com/2022/01/03/TbfxAJ.png)](https://imgtu.com/i/TbfxAJ)

4. 然后输入`Y`即可，这样就创建了一个broker.
5. 输入`"/Users/xiongwei/artemisbroker/bin/artemis" run`就可以启动ActiveMQ Artemis


## pom文件配置

    <dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-artemis</artifactId>
	</dependency>


## 结尾
这样就可以安装并使用ActiveMQ Artemis了，有疑问欢迎大家来一起探讨。


---
#### 版权声明
本文原创作者：ereson<br/>
博客地址 ：[https://ereson.github.io/](https://ereson.github.io/)

