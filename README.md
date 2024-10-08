# 曲宝的博客备份

---start---
## 目录 (2024年09月08日更新)
[测试在根目录下能否正常倒序显示文章](https://blogs.qudange.top/p/%e6%b5%8b%e8%af%95%e5%9c%a8%e6%a0%b9%e7%9b%ae%e5%bd%95%e4%b8%8b%e8%83%bd%e5%90%a6%e6%ad%a3%e5%b8%b8%e5%80%92%e5%ba%8f%e6%98%be%e7%a4%ba%e6%96%87%e7%ab%a0/)

[荒原往事](https://blogs.qudange.top/p/readme/)

[Obsidian 实现复制时自动上传图片到图床](https://blogs.qudange.top/p/2024-08-11-obsidian-pic-upload/)

[用 n8n 实现三步翻译](https://blogs.qudange.top/p/2024-08-07-n8n_3steps_translate/)

[语音笔记AudioPen的“平替”](https://blogs.qudange.top/p/2024-07-16-audiopen-substitute/)

[AudioPen：让Ai帮你整理碎碎念，语音转书面化文字的利器](https://blogs.qudange.top/p/2024-07-15-audiopen/)

[obcsapi —— 最好的obsidian工具（需要云部署）](https://blogs.qudange.top/p/2024-07-14-obcsapi/)

[安卓透明代理，上手 box for magisk](https://blogs.qudange.top/p/2024-07-14-box-for-magisk/)

[如何下载网易云音乐的普通歌词与双语歌词](https://blogs.qudange.top/p/2024-07-13-how-to-download-the-lyrics/)

[安卓端用tasker实现ai总结b站](https://blogs.qudange.top/p/2024-07-13-android_tasker_ai_summary/)

[wordpress导入rss以同步全平台](https://blogs.qudange.top/p/2024-04-23-wordpress%e5%af%bc%e5%85%a5rss%e4%bb%a5%e5%90%8c%e6%ad%a5%e5%85%a8%e5%b9%b3%e5%8f%b0/)

[三星浏览器调教记录](https://blogs.qudange.top/p/2024-04-01-samsung/)

[安卓使用 Thanox 实现安装新应用自动加入 Magisk 的 Denylist（Shamiko 实现）](https://blogs.qudange.top/p/2023-07-07-magisk/)

[测试github2wordpress](https://blogs.qudange.top/p/2023-07-06-test/)

[一键把excalidraw的头脑风暴输出为线性文章](https://blogs.qudange.top/p/%e4%b8%80%e9%94%ae%e6%8a%8aexcalidraw%e7%9a%84%e5%a4%b4%e8%84%91%e9%a3%8e%e6%9a%b4%e8%be%93%e5%87%ba%e4%b8%ba%e7%ba%bf%e6%80%a7%e6%96%87%e7%ab%a0/)

[obsidian发布的探索](https://blogs.qudange.top/p/obsidian%e5%8f%91%e5%b8%83%e7%9a%84%e6%8e%a2%e7%b4%a2/)

[Obsidian 实现复制时自动上传图片到图床](https://blogs.qudange.top/p/obsidian%20%e5%ae%9e%e7%8e%b0%e5%a4%8d%e5%88%b6%e6%97%b6%e8%87%aa%e5%8a%a8%e4%b8%8a%e4%bc%a0%e5%9b%be%e7%89%87%e5%88%b0%e5%9b%be%e5%ba%8a/)

[Obsidian tar插件实现obsidian内部集成LLM对话](https://blogs.qudange.top/p/obsidian%20tar%e6%8f%92%e4%bb%b6%e5%ae%9e%e7%8e%b0obsidian%e5%86%85%e9%83%a8%e9%9b%86%e6%88%90llm%e5%af%b9%e8%af%9d/)

[这是一篇用于测试笔记流程是否完善的笔记](https://blogs.qudange.top/p/%e8%bf%99%e6%98%af%e4%b8%80%e7%af%87%e7%94%a8%e4%ba%8e%e6%b5%8b%e8%af%95%e7%ac%94%e8%ae%b0%e6%b5%81%e7%a8%8b%e6%98%af%e5%90%a6%e5%ae%8c%e5%96%84%e7%9a%84%e7%ac%94%e8%ae%b0/)

---end---
## 项目介绍

平时用obsidian写东西，整理好后发布到github上，通过github pages做一个静态博客，然后用github action同步到自建博客上。
obsidian作为一个好用的编辑器，自建博客的功能更完善，而github pages做永久备份。

## 博客地址

我的wordpress：https://blogs.qudange.top

我的github blog： https://dangehub.github.io

## obsidian端设置
1. 安装插件`Github Publisher`
2. 配置插件：其他保持不动，修改以下选项
    - Repository Nmae: <github2wp>
    - GitHub Username: <your github name>
    - Github Token: <your github token>
    - Default Folder: _posts  #此选项位于Upload configuration中
3. 使用方法：在obsidian的文章yaml区中加入字段`share: true`，然后执行obsidian命令`Github Publisher:Upload single current active note`

ps：只要是能发布到github，其实什么插件都行，不用插件直接用git也行。不过这个插件能够检测所有打了share标记的文章，并且能只上传修改过的文章，比git用起来更省心。可以将常用的yaml头做成obsidian模板，这里也附上我的模板：

```
---
share: true 
title: 标题
tags: 
- geek
categories:
- Github
---

```

## 用Github Actions写Markdown文章，自动更新到WordPress


- 写博客最舒服的格式是Markdown；

- 管理博客站最省心的方式是WordPress；

- 最稳定的博客是Github；



这个项目可以让你用Markdown写博客，push更新到Github后，Github Actions自动将文章更新到WordPress，并将WordPres站的文章索引更新到Github仓库的README.md，供搜索引擎收录。



![image-20210119181051609](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123033557RhdS4nmK.png)



### 如何实现WordPress登录授权？

WordPress默认开启了xmlrpc服务，xmlrpc是一套的统用的博客更新标准，允许用户以POST方式自动对文章内容进行增删改查。授权方式为 用户名 和 密码, 在WordPress中是后台登录的账户名和密码

假设WordPress网站为 [https://fangyuanxiaozhan.com](https://fangyuanxiaozhan.com) 

![image-20210119180338929](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123033711jFFFRE3D.png)

它的xmlrpc服务地址为  [https://fangyuanxiaozhan.com/xmlrpc.php](https://fangyuanxiaozhan.com/xmlrpc.php)

![image-20210119180403270](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123033808cFthmwwi.png)



### 使用Github Actions 有什么好处？

Github Actions 可以让我们无需安装开发环境，即可完成代码的运行。

![image-20210119180656968](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123033850KpH03KNE.png)

对于本项目而言，我可以用手机版Git App，或者Github网页完成新建文章, 然后push到仓库，Github Actions会自动帮我完成相关代码运行，代码可以帮我更新文章到WordPress网站，并生成新的文章目录索引，并自动给你更新到README.md, 供搜索引擎收录。



![image-20210119180529083](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123033950bTXn7Skr.png)


### 如何保护自己的WordPress账户密码？


Github 有一个secrets 功能，可以将用户名密码等关键信息保护起来，只有Github Actions可以读取到关键信息。

本项目需要设置三个secret



- WordPress登录用户名, 变量名为 USERNAME
- WordPress登录密码，变量名为 PASSWORD
- WordPress的xmlrpc.php，变量名为 XMLRPC_PHP







![image-20210119173133800](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/16111230341284PaHwCDm.png)



### 如何新建文章？

在`_post` 目录下新建 后缀为 `.md` 的markdown文件即可

![image-20210119181544158](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/16111230342738acPGWSM.png)



### 文章管理：如何为文章分类/加关键词标签？

在 `.md` 文件顶部填写以下初始化信息，即可完成标题（title），标签（tags），分类（categories）的设置，**其中title为必填项目**（这些关键词不是我定义的，我借用了著名静态博客构建工具 [hexo](https://github.com/hexojs/hexo) 的标准）








```
---
title: 我是标题
tags: 
- 我是0号标签关键词
- 我是1号标签关键词
- 我是2号标签关键词
categories:
- 我是1号分类
- 我是2号分类
---

```







## 标签(tags)和分类(categories)有什么区别？

标签(tags)是针对单篇文章的关键词，比如香蕉的标签有 **黄色**，**味甜** （标签是香蕉的属性）
分类(categories)是本篇文章的归属，比如香蕉的分类为 **水果**，**植物** 

![image-20210119182027684](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123034368EXM02d37.png)

###  如何设置固定链接？

对于博客而言，文章拥有一个固定的链接，是很重要的，我经过各种尝试，最终借鉴了 [简书](jianshu.com) 的文章url形式，域名后加 `/p/` , 再加英文文件名，只要不改变英文文件名，文章就有固定的链接，我在`_posts` 目录下新建一个 `2020-01-18-blog.md` 文件，同步后的文章url为 



[https://fangyuanxiaozhan.com/p/2020-01-18-blog/](https://fangyuanxiaozhan.com/p/2020-01-18-blog/)



文件名与网站url严格对应，既方便了修改，又可以在网站数据库出事故后，迅速从github仓库迅速恢复文章内容（容灾），连url都不会变。




![image-20210119171713841](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123034673aad52Amb.png)



## 如何使用？

完成以上配置后

每次在`_posts` 文件夹新增或更新文章后，运行

```
git pull && git add _posts && git commit -m "update" && git push
```

![image-20210119182503520](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123034888HbKthGTh.png)

即可！



![image-20210119182653436](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123036038n18wBCfT.png)



###  Github README.md显示效果,（新增的文章排在首位）



![image-20210119184015781](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/16111230361713668ZtFR.png)



### WordPress网站也同步发布了文章

![image-20210119182849720](https://raw.githubusercontent.com/zhaoolee/WordPressXMLRPCTools/master/README/1611123036272XED7hTE0.png)

[https://fangyuanxiaozhan.com/p/2020-01-19-18-00-wordpressxmlrpctools/](https://fangyuanxiaozhan.com/p/2020-01-19-18-00-wordpressxmlrpctools/)




[https://imgkr.com/#upload](https://imgkr.com/#upload)

Pocket Git 和 MT管理器可以配合完成Git 文件的新增更新和上传。


