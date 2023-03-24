---
title: Properties
status: Published
position: content/docs/introduce
categories: []
tags: []
keywords: []
createat: "2022-12-29T09:33:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2022-12-30T14:58:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: 2
---
Notion 的属性是可以完全自己定制的，但是在 Notion-Site 中，我们绑定了一些生成网站所必要的属性，这些属性是 Notion-Site 的核心功能，每个属性都用于管理生成的网站，所以，为了以后随时随地管理网站，需要先理解这些属性的意义和规则。

{{< tip "warning" >}}

<!--more-->Notion-Site 的属性非常重要，本页内容请一定仔细阅读。当然如果你非常了解 Hugo，浅浅的浏览一遍就好。

{{< /tip >}}

### Name
Database 中的默认字段，用作维护网站的子页面，名称作为描述字段，让网站管理人员理解这个页面的作用



### Cover
Database 中的隐藏字段，用作维护网站文章的封面，缩略图



### Title
{{< tip >}}

标题属性，大多数所有主题都默认支持该属性，用来维护文章或文档的标题

{{< /tip >}}

### Status
用于管理博客的发布状态，目前有以下几种状态：

- <span style="color: rgba(203, 145, 47, 1);"> **finished** </span>

- <span style="color: rgba(68, 131, 97, 1);"> **published** </span>

- <span style="color: rgba(212, 76, 71, 1);"> **draft** </span>

如果设置该状态是 draft，表示该文章还处于“草稿” 阶段，那么 Notion-Site 不会拉取该页面，也不会参与生成网站。

如果设置该状态是 finished 或 published ，那么 Notion-Site 会从 Notion 服务器拉取该页面，生成目标网页

当网站发布完毕，Notion-Site 会将 finished 状态自动修改为 published 状态，用户可以很方便的看到变化。

### Categories
{{< tip >}}

分类属性，大多数博客类主题都默认支持该属性，方便查看分类的文章或浏览该分类的所有文章。

{{</ tip >}}

![](media/s3.us-west-2.amazonaws.com_b8bd389a-2c96-4217-adbe-b59926928086.png)

![](media/s3.us-west-2.amazonaws.com_e8b53394-b2c1-431e-8f0d-fe962265cc52.png)

### Tags
{{< tip >}}

标签属性，大多数博客类主题都默认支持该属性，方便查看标签的文章或浏览该标签的所有文章。

{{< /tip >}}

![](media/s3.us-west-2.amazonaws.com_cf1778bd-2c50-4235-9d70-7594f28f95d1.png)

### Position
{{< tip "warning" >}}
非必填，如果未填写，Notion-Site 初始化默认值为`"content/post"`

{{< /tip >}}

{{< tip >}}

因为各种主题的用途不同，所以每种主题可能有自己的存放 markdown 原文的路径，用户可以根据自己的需求选择 Notion-Site 生成文件的位置,该路径是以 HomePath 为基础的相对路径

{{< /tip >}}



![](media/s3.us-west-2.amazonaws.com_0e6b1342-ef2d-4f16-8273-16ab94825e64.png)

![](media/s3.us-west-2.amazonaws.com_c516369d-ea9f-4bc5-a48c-6b73b4be4576.png)



### Keywords
一些模板有支持

### FileName
为生成的文件自定义文件名，默认生成的规则:`{homePath} / {Position} / {Name} / index.md`

{{< tip "warning" >}}

但是如果填写了 FileName 属性，将会按照`{homePath} / {position} / {FileName}.md`规则创建文件

{{< /tip  >}}

### Desctiption
文章的描述信息

### CreateAt
创建时间属性，大多数博客类主题都默认支持该属性，方便按照年度查看归档的文章，文章的发布时间，以及排序。

![](media/s3.us-west-2.amazonaws.com_e535b945-d4dd-492e-8ee9-4f8206cf2694.png)

{{< tip "warning" >}}

该字段会影响生成网站中文章的发布时间，在 Notion-Site 提供的 Database 默认模板中，时间是默认不可编辑的，如果用户想自定义创建时间，例如迁移一些旧文章等，可以修改 CreateAt 的属性改为自定义，由自己调整时间。



{{< /tip  >}}

### Author
保留字段，暂时没用

### LastMod
上次修改时间属性，<span style="color: rgba(159, 107, 83, 1);">部分</span>博客类主题默认支持该属性。

### ExpiryDate
过期时间属性，大多数博客类主题都默认支持该属性，如果 当前时间 > 过期时间，该文章不可见。

### PublishDate
该文章最近一次的部署时间，为 Notion-Site 成功发布该文章的时间，由 Notion-Site 程序自动修改。

### Show_comments
是否显示评论，暂未接入评论组件，TODO

### Slug
自定义文章 URL 属性，大多数博客类主题都默认支持该属性，如果文章含有中文导致链接不美观或名称太长，可以设置该属性，将自动替换 Name 属性作为访问地址。

### Type
-  **setting** 

-  **gallery** 

-  **folder** 

-  **compose** 

setting 表示该 Page 里面的内容为配置信息，比如 config.yaml，只会原样输出，并且不会生成任何额外的 FrontMatter 描述信息。



folder 表示该 Page 只是一个目录，里面包含子 Database , 一般用于文档站的维护，方便在 Notion 中体现层次，方便管理，而不是都堆在一个层级，不便于管理。



gallery 表示该文章开启 “画廊模式”，针对三张以上连续的图片会在文章内部合并为一个 Gallery，比较适合图片类的博客。

### Weight
权重属性，大多数文档类主题都默认支持该属性，方便按照为一个目录下的文档定制排序。

这里截个图

