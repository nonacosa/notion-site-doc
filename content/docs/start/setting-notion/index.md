---
title: Setting Notion
status: Published
position: content/docs/start
categories: []
tags: []
keywords: []
createat: "2022-12-30T15:49:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2023-01-02T12:11:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: 7
---


### 创建 Integration
先为当前 Notion 账号设置 Secret

{{< bookmark image="https://www.notion.so/images/meta/default.png" icon="https://www.notion.so/images/favicon.ico" url="https://www.notion.so/my-integrations"  des="A new tool that blends your everyday work apps into one. It's the all-in-one workspace for you and your team"  title="Notion – The all-in-one workspace for your notes, tasks, wikis, and databases."  >}}

<!--more-->![](media/s3.us-west-2.amazonaws.com_ec57dff2-9d52-4ac8-aaf0-45e6df24b5ba.png)

![](media/s3.us-west-2.amazonaws.com_1d60a269-df97-4500-a589-d96a80c5b228.png)

然后勾选 Internal integration, 并勾选三个权限：

- read

- update

- insert （可选）

{{< tip >}}

read 权限是为了读取 Page 信息，update 权限是为了自动更新 Page 属性，insert 权限可以为了以后 Notion-Site 的新功能做准备。

{{< /tip >}}



### 添加 Integration
![](media/s3.us-west-2.amazonaws.com_49f20c24-125d-4bda-b1e7-6072c471a584.png)

### 保存 Token
![](media/s3.us-west-2.amazonaws.com_14eb72d0-043d-4ad6-acca-5b89bb4f7904.png)

进入刚刚创建的 Notion Integration，拿到 token，该 token 的生效范围是该账号的 workspace，不同的 workspace 需要不同的  Integration



### 复制模板


博客类 Notion 模板：[BLOG](https://www.notion.so/df7fb0e4e0114268b973f9d3e9a39982)

文档类 Notion 模板：[Notiton Site Doc](https://www.notion.so/2bd00e5dfff3449ba81e0142f8af9bbb)



选择类型后，点击复制，选择复制到自己的 workspace 即可。

![](media/s3.us-west-2.amazonaws.com_c19ce73e-f88c-4f0a-a64f-a958eaaa336a.png)



