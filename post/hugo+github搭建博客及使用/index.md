# 

# Hugo+Github搭建博客及使用



## Github操作：

1. 注册一个github账号并登录，地址： https://github.com/ 
2. 新建一个github repository, 库名为*username*.github.io



## Hugo操作：

1. 安装hugo, 参考官方教程：https://gohugo.io/getting-started/installing

   windows安装：直接下载最新版的exe文件，下载地址： https://github.com/gohugoio/hugo/releases ，将可执行文件设置成环境变量，可百度一下windows设置环境变量方法。

2. 安装完成后，打开cmd, 输入以下命令确认hugo版本。

   `hugo version`

3. 新建一个Hugo网站，进入存放Hugo网站文件夹的目录，比如：F:\hugo，执行以下命令新建一个Hugo网站。

   `hugo new site blog`

4. 选择Hugo主题并克隆至本地目录，地址：https://themes.gohugo.io, 将所选主题克隆至本地目录，方法如下：

   `cd F:\hugo\blog   *#* *进入网站目录*`

   `mkdir themes    *#* *创建“themes”目录*`

   `cd themes   *#* *进入”themes“目录*`

   `git clone  https://github.com/matsuyoshi30/harbor.git  harbor  *# 将Harbor主题克隆至”harbor“目录。*`

5. 编辑配置文件，在Hugo网站文件夹的根目录下，编辑config.toml文件

   windows系统： copy themes\harbor\exampleSite\config.toml .

   `baseURL = "https://username.github.io/"`  # username替换为自己的博客名字
   `languageCode = "en-us"`
   `title = "wangxj35's Blog"`
   `theme = "simple-blog"`

6. 重新生成静态博客

   `hugo`

7. 上传public内的文件到username.github.io项目

   `cd F:\hugo\blog\public`

   `git init`

   `git add .`

   `git commit -m "first init blog"`

   `git remote add origin git@github.com:username/username.github.io.git`

   `git push -u origin master`



## 新建一篇文章：

1. 进入网站文件夹的根目录 

   `cd F:\hugo\blog`

2. 使用以下命令新建一篇文章

   hugo new post/my-first-post.md

3. 编辑新建的文章，添加内容并保存。

   `hugo`

4. 进入F:\hugo\blog\public目录，将文章推送到github, 命令如下：

   `cd public`

   `git add -A`

   `git commit -m "add my-first-post.md"`

   `git push -u origin master`

   `cd ..`



## 本地预览网站效果：

1. 打开cmd, 启动Hugo server

   `hugo server -D`

2. 使用浏览器打开http://localhost:1313预览。



## 打开网页预览效果：

 https://wangxj35.github.io/ 
