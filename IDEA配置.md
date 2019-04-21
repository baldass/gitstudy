# IDEA配置  
官网：https://www.jetbrains.com/idea/  

## IDEA破解(2018可用) 
1. 将[JetbrainsIdesCrack-4.2-release-sha1.jar](https://raw.githubusercontent.com/baldass/gitstudy/master/idea/JetbrainsIdesCrack-4.2-release-sha1.jar)放到安装IDEA路径的bin目录下  
2. 找到同一目录下的idea.exe.vmoptions和idea64.exe.vmoptions,在两个文件最后分别加上
```
-javaagent:{安装IDEA的绝对路径}\bin\JetbrainsIdesCrack-4.2-release-sha1.jar
```  
3. 启动IDEA,选择Activation Code输入:  
```
ThisCrackLicenseId-{
"licenseId":"ThisCrackLicenseId",
"licenseeName":"someone",
"assigneeName":"",
"assigneeEmail":"idea@qq.com",
"licenseRestriction":"For This Crack, Only Test! Please support genuine!!!",
"checkConcurrentUse":false,
"products":[
{"code":"II","paidUpTo":"2099-12-31"},
{"code":"DM","paidUpTo":"2099-12-31"},
{"code":"AC","paidUpTo":"2099-12-31"},
{"code":"RS0","paidUpTo":"2099-12-31"},
{"code":"WS","paidUpTo":"2099-12-31"},
{"code":"DPN","paidUpTo":"2099-12-31"},
{"code":"RC","paidUpTo":"2099-12-31"},
{"code":"PS","paidUpTo":"2099-12-31"},
{"code":"DC","paidUpTo":"2099-12-31"},
{"code":"RM","paidUpTo":"2099-12-31"},
{"code":"CL","paidUpTo":"2099-12-31"},
{"code":"PC","paidUpTo":"2099-12-31"}
],
"hash":"2911276/0",
"gracePeriodDays":7,
"autoProlongated":false}
```  
4. 在此启动就可以使用了 

## 配置 
* 修改IDEA配置  
    1. 打开IDEA安装目录\bin\idea.properties文件
    2. 找到# idea.config.path=${user.home}/.IntelliJIdea/config  
   修改成idea.config.path=D:/Program Files/JetBrains/.IntelliJIdea/config
    3. 找到# idea.system.path=${user.home}/.IntelliJIdea/system  
   修改成idea.system.path=D:/Program Files/JetBrains/.IntelliJIdea/system  
* 修改IDEA默认启动  
  File=>settings=>Appearance  & Behavior =>System Settings =>把Starup/Shutdown下面的Reopen last project on startup单选框设成未选择状态

* 修改IDEA的maven配置
    * 打开IDEA=>settings=>Build,Execution,Deployment=>Build Tools=>Maven
=>在Maven home directory选择自己本地的maven(D:\Program Files\apache\apache-maven-3.6.0)
=>User settings file: 输入对应的本地配置文件(D:\Program Files\apache\apache-maven-3.6.0\conf\settings.xml)
=>Local repository: 输入自己的本地Maven仓库  

## 设置IDEA自动提示不区分大小写  
* IDEA=>settings=>Editor=>General=>Code Completion的Mathch case取消掉  

## 修改默认文件编码(例如properties文件)  
> File=>settings=>Editor=>File Encodings=>如下图设置  
> ![具体设置](https://raw.githubusercontent.com/baldass/gitstudy/master/idea/idea-filencoding-set.png)
