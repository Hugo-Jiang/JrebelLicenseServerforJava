# JrebelLicenseServerforJava

搭建jrebel激活服务; 欢迎star。



# 使用教程

1. 准备工作，你需要一个后台一直运行的服务，可以在阿里云购买一台轻量级应用服务器，并且安装好java环境；

2. 克隆本项目，打成jar包，会生成jar包，或者到这里[直接下载](https://github.com/wyx176/JrebelLicenseServerforJava/releases)也行（已经打好包了）

   ```
   mvn clean package
   ```

3. 把jar包传送到云服务器上，然后进入到jar包所在目录，执行以下命令：

   ```bash
   # nohup  命令   &     ：表示后台运行，这样保证ssh连接断开服务也是一直开着的
   nohup java -jar JrebelBrainsLicenseServerforJava.jar -p 8081 &
   ```

4. 最后，可以检查下是否OK了，可以通过浏览器访问ip:8081或者使用命令查看：  `ps -ef | grep java`



# Jrebel & Jet Brains License Server for Java

A license server for Jrebel & JetBrains products, it also support JRebel for Android and XRebel.

***
Thank ilanyu

NOTE: This is provided for educational purposes only. Please support genuine.
***
## Setup
Run:
```
cd /path/to/project
mvn compile 
mvn exec:java -Dexec.mainClass="com.vvvtimes.server.MainServer" -Dexec.args="-p 8081"
```
Packing a runnable jar:
```
mvn package
```
then
```
java -jar JrebelBrainsLicenseServerforJava.jar -p 8081
```
default port is 8081.

## Docker
Build image
```
mvn package 
docker build -t jrebel-ls .
```

start container
```
docker run -d --name jrebel-ls --restart always -e PORT=9001 -p 9001:9001 jrebel-ls
```
default port is 8081,you can modify it
## Support

Jrebel

JRebel for Android

XRebel

JetBrains Products

## Feedback




