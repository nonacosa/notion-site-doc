---
title: Publish by Vercel
status: Published
position: content/docs/start
categories: []
tags: []
keywords: []
createat: "2023-01-02T16:53:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2023-01-02T17:06:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: 10
---
 **首先，需要创建一个 Vercel 账号，然后添加新项目** 



<!--more-->![](media/s3.us-west-2.amazonaws.com_b7647e66-8277-4a86-bd9d-9888afa4e74c.png)



 **授权 Github ， 选择之前基于 Notion-Site-Doc 创建的新仓库，点击 Import** 



![](media/s3.us-west-2.amazonaws.com_6d644129-daa1-447b-9781-aca747f3295a.png)



 **创建后修改分支 main 为 gh-pages  :** 



![](media/s3.us-west-2.amazonaws.com_814dabf3-1f89-4cc9-9a72-7fb4dfd0816f.png)



 **如果有自己的域名，绑定到中国区的 Host 并设置子域名即可** 



![](media/s3.us-west-2.amazonaws.com_f6671ee5-9642-4d8a-9c32-775d05ee504b.png)

![](media/s3.us-west-2.amazonaws.com_d9115b18-4c81-4f7f-97f0-51737d34fe4e.png)

在 Github Action  手动重新运行一下（第一次构建默认是 main 分支，修改为 gh-pages 分支后需要再触发一下 Vercel 的 Hook）

### 完成
如果不更换主题，以后都不需要再配置了。



![](media/s3.us-west-2.amazonaws.com_bbd0549a-15b4-4817-bd2c-5ebded2e038f.png)



