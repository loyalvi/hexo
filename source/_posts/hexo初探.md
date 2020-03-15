---
title: hexo的简单使用
date: 2020-03-11 20:27:23
tags: 
- hexo
- blog
---

## 安装部署
　　
　　安装部署比较简单,看官方文档很快就解决了,不过现在还有个遗留问题:`GitHub上的代码是编译后的文件,源码没有上传到git上`之后有时间在研究。

### 安装hexo
```JavaScript {.line-numbers}
    npm install hexo-cli -g
    hexo init blog
    cd blog
    npm install
    hexo server
```
### hexo-deployer-git 部署到github
```JavaScript {.line-numbers}
    //部署服务到git
    npm install hexo-deployer-git --save
```
修改配置文件` _config.yaml`
```JavaScript {.line-numbers}
# _config.yaml
deploy:
  - type: git
    repo: git@github.com:<username>/<username>.github.io.git
    branch: master
    name: loyalvi
    email: 2869775223@qq.com
```
## 常用指令

```JavaScript {.line-numbers}
    #npm
    //Layout post page draft false
    hexo new [layout] <title>
    //推送草稿
    hexo publish [layout] <title>
    //显示草稿文件夹
    hexo --draft 
    //生成静态文件
    hexo generate 
    //清除缓存文件 (db.json) 和已生成的静态文件 (public)。
    hexo clean 
    //部署网站
    hexo deploy
```

## Front-matter

Front-matter 是文件最上方以 `---`分隔的区域，用于指定个别文件的变量，举例来说：
```
---
title: Hello World
date: 2013/7/13 20:46:25
---
```



|参数	|描述		|默认值|
|--	|--	|--	|
|layout	|布局		||
|title	|标题		|文章的文件名|
|date	|建立日期	|文件建立日期											|
|updated	|更新日期	|文件更新日期											|
|comments	|开启文章的评论功能|true													|
|tags	|标签（不适用于分页）|														|
|categories	|分类（不适用于分页）|														|
|permalink	|覆盖文章网址|														|
|keywords	|仅用于 meta 标签和 Open Graph 的关键词（不推荐使用）	|

分类具有顺序性和层次性，也就是说 Foo, Bar 不等于 Bar, Foo；而标签没有顺序和层次。
```
categories:
- Diary
tags:
- PS3
- Games
```
## TODO
[ ] 源码上git
[ ] 安装主题
[ ] 研究一下常用的hexo指令
[ ] 研究一下常用的文件目录结构
[ ] 研究更新日志如何添加
[ ] 研究更新日志如何添加
[ ] 123