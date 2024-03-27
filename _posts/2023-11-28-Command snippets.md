---
title: Command Snippets
author: ge2k
date: 2023-11-28 15:46:20 +0800 
categories: [Blogging, syntax]
tags: [command]

---
___
## 2023-11-28
### 片段一
jupyuter 幻灯片转html

`jupyter nbconvert 你的文件名称.ipynb --to slides --post serve`

___

## 2023-11-25
### 片段一
windows电脑添加其他用户组

`win+run netplwiz`

### 片段二
只编译不链接  生成main.o

`g++ main.cpp -c ` 

将编译的结果链接生成可执行文件a.out

`g++ main.o`

### 片段三
用当前路径的Dockfile创建镜像

`docker build -t 镜像名 .  `  

查看镜像

`docker image ls`

删除镜像

`docker rmi` 

用镜像创建容器，本地没有会自动下载

`docker run 镜像名`	

查看容器

`docker ps -a`

删除容器

`docker rm`

___