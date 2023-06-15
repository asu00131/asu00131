---

title: 阿苏00131的Hexo 安装日记
pid: "002"
date: 2022-08-02 12:00:00
top_img: 
---

欢迎使用[Hexo](https://hexo.io/)！这是[第一篇](/blog/001/)的中文翻译。查看[文档](https://hexo.io/zh-cn/docs/)以获取更多信息。如果在使用Hexo时遇到任何问题，你可以在[故障排除](https://hexo.io/zh-cn/docs/troubleshooting.html)中找到答案，或者在[GitHub](https://github.com/hexojs/hexo/issues)上向我提问。

  

## 快速入门

  

### 创建新文章

  

``` bash

hexo new "我的新文章"

```

  

更多信息：[写作](https://hexo.io/zh-cn/docs/writing.html)

  

### 运行服务器

  

``` bash

hexo server

```

  

更多信息：[服务器](https://hexo.io/zh-cn/docs/server.html)

  

### 生成静态文件

  

``` bash

hexo generate

```

  

更多信息：[生成](https://hexo.io/zh-cn/docs/generating.html)

  

### 部署到远程站点

  

``` bash

hexo deploy

```

  

更多信息：[部署](https://hexo.io/zh-cn/docs/one-command-deployment.html)

  

## 我的笔记

  

### Hexo一键三联预览
```yaml
hexo c; hexo g; hexo s
```
  

#### VSCODE终端

```yaml
hexo clean; hexo generate; hexo server
```

#### Git BASH终端

```  bash
hexo clean && hexo generate && hexo server
```

  

### em代表16px

1 em在字体中代表16像素点长度单位。1em是CSS中的一个长度单位，它是相对于父元素的字体大小而言的。如果父元素的字体大小为16px，那么1em就等于16px。

  

### 安装Node Git环境 文本编辑器
1. [Node](https://nodejs.org/en/download)
1. [Git](https://git-scm.com/downloads)
1. [文本编辑器(推荐VSCODE)](https://code.visualstudio.com/download)

### 初始化 Hexo 项目
> hexo init [你的项目名] 
//项目名

### 进入Hexo 项目
> cd [你的项目名]  
//例如你要进入C:/blog-demo文件夹 就写
```yaml
cd C:/blog-demo
```

### 全局安装 Hexo
```yaml
npm install -g hexo-cli
```

### 修改npm源
```yaml
npm config set registry https://registry.npm.taobao.org
```

### 安装Hexo 项目依赖
```yaml
npm i
```

### 下载主题
```yaml
git clone https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
```
这个命令的意思是从 GitHub 上克隆名为 "hexo-theme-butterfly" 的主题仓库，并将其下载到 themes/butterfly 目录中

>	用的是npm方式安装的 hexo-theme-butterfly，后续魔改时更改的文件都是【C:/[项目名]/node_modules/hexo-theme-butterfly】文件夹中的文件。

>	如果你是git clone克隆方式安装的主题，请在【C:/[项目名]/themes/butterfly】文件夹下修改对应的文件。

这里建议使用[everything](https://getquicker.net/Sharedaction?code=7c105817-9d6b-4177-aff3-08d8f6743496)进行查找
大致有许多，这`_posts`里面可以开始写markdown文章了
```bash
source/   # 主题的源代码文件
  ├── _data/     # 存放数据文件（可选）
  ├── _posts/    # 存放文章（可选）
  ├── css/       # 存放CSS文件（可选）
  ├── js/        # 存放JavaScript文件（可选）
  └── ...
```
修改站点配置文件`_config.yml` 或者主题配置文件`_config.butterfly.yml` 中，把主题改为butterfly

### 应用主题
```yaml
theme: butterfly
```
### `pug`以及`stylus`的渲染器依赖下载（非必须）
```yaml
npm install hexo-renderer-pug hexo-renderer-stylus --save
```
### Hexo一键三联预览

```yaml
hexo clean; hexo generate; hexo server
```

### 将静态博客挂载到 GitHub Pages
#### 查看所有配置
```yaml
git config -l
```
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"

#### 安装 hexo-deployer-git 插件
```yaml
npm install hexo-deployer-git --save
```
修改 _config.yml 文件，就是整个Hexo框架的配置文件了。可以在里面修改大部分的配置。详细可参考官方的[配置描述](https://hexo.io/zh-cn/docs/configuration)。  
    修改最后一行的配置，将repository修改为你自己的github项目地址即可，还有分支要改为`main`代表主分支（注意缩进）。

```yaml
deploy:
  type: git
  repository: git@github.com:Fomalhaut-Blog/Fomalhaut-Blog.github.io.git
  branch: main
```

### Hexo一键三联发布

```yaml
hexo clean; hexo generate; hexo deploy
```