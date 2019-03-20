# RabbitMQ的安装启动

## 1. 使用RabbitMQ之前要先下载并安装erlang
* 下载  从[Erlang的官方网址](https://www.erlang.org/)的[下载页面](https://www.erlang.org/downloads)找到想要的版本下载  
* 安装  使用默认选项一直next下去,当然你可以适当地调整安装地址  
        安装成功后会自动在环境变量中配置ERLANG_HOME=D:\Program Files\erl10.3,建议先重启电脑  
		如果安装完erlang后没重启直接安装RabbitMQ的话,则启动RabbitMQ可能报错: 
		   ```cmd 
		   信息: 用提供的模式无法找到文件。
		   系统找不到指定的路径。

           ******************************
           ERLANG_HOME not set correctly.
           ******************************

           Please either set ERLANG_HOME to point to your Erlang installation or place the
           RabbitMQ server distribution in the Erlang lib folder.
		   ```

## 2. 下载安装RabbitMQ 
* 下载  从[RabbitMQ官网](http://www.rabbitmq.com/)的[下载页面](http://www.rabbitmq.com/download.html)下载想要的版本  
* 安装  1. 下载完成后双击软件安装,设置想要的安装路径,其他使用默认配置一直next下去.
        2. 进入cmd命令行, 切换到RabbitMQ安装目录下的sbin文件夹下输入`rabbitmq-plugins.bat enable rabbitmq_management`  
		   如果显示如下,则代表启动成功.  
		   ```cmd 
		   Enabling plugins on node rabbit@DESKTOP-O2OE0LP:
           rabbitmq_management
           The following plugins have been configured:
             rabbitmq_management
             rabbitmq_management_agent
             rabbitmq_web_dispatch
           Applying plugin configuration to rabbit@DESKTOP-O2OE0LP...
           The following plugins have been enabled:
             rabbitmq_management
             rabbitmq_management_agent
             rabbitmq_web_dispatch

           started 3 plugins.
		   ```  
		3. 重启RabbitMQ服务  
		```cmd 
		停止RabbitMQ服务
		net stop rabbitmq 
		启动RabbitMQ服务
		net start rabbitmq
		```  
		4. 打开网页验证 
		进入网址http://localhost:15672 ,输入用户名guest 密码guest 
		