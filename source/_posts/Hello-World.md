---
title: Hello World
date: 2021-02-06 18:18:49
tags: 技术
---

# 嗨！

你们好！我是北丸らみと！这是我的第一个~~简短而又小~~的文章！从今天开始请多关照咯！

---

## 我是如何有这个想法的？

今天看了其他人的博客（虽然那个是基于Wordpress做的动态网站），突发奇想，于是我就想“诶？我能不能也建一个博客网站......”，于是便有了你现在所看的这个页面。

---

## 如何简单的建立类似于我这样的个人博客？

如果你已经安装了[Git](https://www.jianshu.com/p/bebba0d8038e)和[Node.js](https://www.jianshu.com/p/482d92aba48f)并注册了[Github](https://github.com/)【也可以是[Gitee](https://gitee.com/)】，那么太好了，你只需要创建一个以**你的Github/Gitee用户名**为首的二级域名，就完全可以简易建站啦！

软件安装和建库部分可以去参照其他文章 下面是Hexo建站的详细操作步骤

### 第一步：在CMD下安装Hexo

使用Win+X键，以管理员方式运行命令提示符，然后在确保已安装上述软件的前提下，输入

```
npm install -g hexo
```

当然，如果你的下载速度过慢且你拥有支持HTTP的代理的话，也可以尝试通过代理通道加速，代码如下

```
git config --global http.proxy http://127.0.0.1:10809
```

```
npm config set proxy=http://127.0.0.1:10809
```

（Tip：如果你的代理链接并不是上方的链接，可以替换，包括端口）

### 第二步：建立Hexo库

首先创建一个文件夹 因为以管理员身份运行的命令提示符默认dir在`C:\Windows\system32>`下，所以我们先换到我们想要的父目录，这里以用户文件夹为例。输入以下代码：

```
cd \ 
cd Users\[你的用户名]\创建的文件夹
hexo init
```

![示例](https://cdn.jsdelivr.net/gh/kitamaruramito/kitamaruramito.github.io/img/posta1-1.png)

如果出现上述文字，那么你的博客就已经创建好啦！
输入`hexo s`启动，然后在浏览器中键入`localhost:4000`测试一下吧！

### 第三步：Git到你的仓库

（这里默认你已经建好了Github仓库，并已添加`Master`分支
在你的博客根目录下找到`_config.yml`，打开后找到`Deployment`一项，并修改成：

```
# Deployment
deploy:
  type: git
  repo: git@github.com:【你的Github用户名】/【你的Github用户名】.github.io.git
  branch: master
```

后，在博客根目录下打开cmd，输入：

```
hexo clean
hexo g
hexo d
```

就可上传保存到库啦~