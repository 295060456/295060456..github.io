# 利用Hugo生成静态网页教程

资料来源：https://www.gohugo.org/

使用终端：Oh-My-Zsh

## 利用brew自动配置安装Hugo（其他方式不推荐）

brew install hugo

## 生成站点

### 1、前置条件：

​	1.1、桌面建立一个空文件夹（Test_Hugo），用于存放静态网页文件相关资源以及依赖

​	1.2、拖动Test_Hugo到终端，执行：hugo new site 【拖动‘Test_Hugo’文件夹到终端】，此时文件夹Test_Hugo里面生成内容如下图所示👇🏻

![image-20230403235709736](/Users/jobs/Library/Application Support/typora-user-images/image-20230403235709736.png)

### 2、创建一些页面资源

​	2.1、【创建文章页面】 hugo new about.md

​	2.2、【创建第一篇文章，放到 `post` 目录，方便之后生成聚合页面】 hugo new post/first.md

### 3、安装皮肤

​	cd命令进入themes文件夹，执行命令  git **clone** https://github.com/spf13/hyde.git

## 运行Hugo

跳出themes文件目录，并且回到Test_Hugo目录，执行命令 hugo server --theme=hyde --buildDrafts

![image-20230404000715846](/Users/jobs/Library/Application Support/typora-user-images/image-20230404000715846.png)

此时，页面服务（监听默认端口1313）已经开启，可以在浏览器里面进行访问

http://localhost:1313

注意：只要关闭Mac终端或者Ctrl+C，都会结束掉页面服务，导致http://localhost:1313无法打开