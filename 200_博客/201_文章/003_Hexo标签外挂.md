---
title: 记录 Hexo  Butterfly主题 标签外挂 
pid: "003"
date: 2022-08-02 18:00:00
top_img: 
---
{% audio https://npm.elemecdn.com/anzhiyu-music@1.0.4/%E9%9D%92%E8%8A%B1%E7%93%B7/%E9%9D%92%E8%8A%B1%E7%93%B7.mp3 %}
## 记录 Hexo  Butterfly主题 标签外挂 
hexo 分栏写法 需要安装什么插件？
{% tabs Tabs, 1 %}
  
<!-- tab 安装插件 -->
`hexo-butterfly-tag-plugins-plus` 可以让您使用更多的标签功能。
## 安装方法如下：
1. 在您的博客根目录下，打开终端，输入以下命令：
```yaml
npm install hexo-butterfly-tag-plugins-plus --save
```
2. 由于 hexo 自带的 markdown 渲染插件 hexo-renderer-marked 与这些标签的语法不太兼容，建议您用 hexo-renderer-kramed 来替换它。输入以下命令：
> a. 卸掉之前的渲染器
```yaml
npm uninstall hexo-renderer-marked --save
```
 b. 安装新的渲染器
```yaml
npm install hexo-renderer-kramed --save
```
3. 现在好了，去进行配置吧


***
<!-- endtab -->
  
<!-- tab 参数配置 -->
添加配置信息，以下为写法示例

在站点配置文件`_config.yml` 或者主题配置文件`_config.butterfly.yml` 中添加

```yaml
# tag-plugins-plus  
# see https://akilar.top/posts/615e2dec/  
tag_plugins:  
  enable: true # 开关  
  priority: 5 #过滤器优先权  
  issues: false #issues标签依赖注入开关  
  CDN:  
    anima: https://cdn.jsdelivr.net/gh/l-lin/font-awesome-animation/dist/font-awesome-animation.min.css #动画标签anima的依赖  
    jquery: https://cdn.jsdelivr.net/npm/jquery@latest/dist/jquery.min.js #issues标签依赖  
    issues: https://cdn.jsdelivr.net/npm/hexo-theme-volantis@latest/source/js/issues.min.js #issues标签依赖  
    iconfont: //at.alicdn.com/t/font_2032782_8d5kxvn09md.js # 阿里图标可以自设
    carousel: https://cdn.jsdelivr.net/npm/hexo-butterfly-tag-plugins-plus@latest/lib/carousel-touch.min.js
```
<!-- endtab -->
  
<!-- tab 注意事项 -->
虽然使用挺好的，但是格式``-->``后面千万不要再加空格【复制粘贴真的看不出】，否则会报错，亲测了好多天（==

![](https://img.tucang.cc/api/image/show/9b95e9175bb58500b364401b8f1533f9)
<!-- endtab -->
  
<!-- tab demo模板 -->
必须注意！！！
``-->``后面千万不要再加空格，否则会报错
``-->``后面千万不要再加空格，否则会报错
``-->``后面千万不要再加空格，否则会报错

```yaml
{% tabs text,1 %}
<!-- tab 预览一 -->
内容111
<!-- endtab -->


<!-- tab 预览二 -->
内容222
<!-- endtab -->


<!-- tab 示例源码 -->
内容333
<!-- endtab -->
{% endtabs%}
```

上面的开头`1` 代表优先显示第几个
<!-- endtab -->
{% endtabs %}


## demo展示【來自上面第4个】
{% tabs text,1 %}
<!-- tab 预览一 -->
内容111
<!-- endtab -->


<!-- tab 预览二 -->
内容222
<!-- endtab -->


<!-- tab 示例源码 -->
内容333
<!-- endtab -->
{% endtabs%}
