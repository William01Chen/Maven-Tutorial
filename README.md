# Maven Tutorial
## Install Maven
* 下载地址：http://maven.apache.org/
* Linux安装： `unzip apache-maven-x.x.x-bin.zip
or   tar xzvf apache-maven-x.x.x-bin.tar.gz`
* Windows安装: 解压下载的apache-maven-x.x.x-bin.zip到指定目录

## Environment

* 添加 `apache-maven-x.xx/bin` 目录到path系统变量
* 检查环境变量是否配置成功`mvn -v`结果如下

```
Apache Maven 3.3.9 (bb52d8502b132ec0a5a3f4c09453c07478323dc5; 2015-11-11T00:41:47+08:00)
Maven home: /usr/local/Cellar/maven/3.3.9/libexec
Java version: 1.8.0_92, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_92.jdk/Contents/Home/jre
Default locale: zh_CN, platform encoding: UTF-8
OS name: "mac os x", version: "10.11.4", arch: "x86_64", family: "mac"
```

## Build Project

1.	定位在工作目录
2.	输入mvn archetype:generate 这一步需要等待一段时间，maven从中央仓库下载需要的第三方jar
3.	默认下载路径为用户家目录下的.m2/repository文件夹下
4.	第2步执行完成，会列出maven模型列表
5.	默认会定位在maven-archetype-quickstart 模型
6.	按键return or enter
7.	选择模块的版本号，默认return or enter
8.	输入groupId  例如：org.wwrsh.demo
9.	输入 artifactId 例如：demo
10.	输入版本号 return or enter
11.	输入package 默认是groupId 可以自己输入或者return or enter
12.	确认以上信息是否正确，无误return or enter
以上全部完成，我们的Maven构建的JAVA项目就成功了

## Mavne Command

* mvn compile - 编译项目
* mvn compile - 打包项目
* mvn test - 执行测试
* mvn clean - 清除构建目录
* mvn install - 安装jar包到本地库

## Quick Build Project
```
mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```
## Install Other Jar
```
mvn install:install-file -Dfile=path -DgroupId=org.wwrsh.xxx -DartifactId=xxx -Dversion=0.1.0 -Dpackaging=jar
```

