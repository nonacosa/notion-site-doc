---
title: Use Github Action
status: Published
position: content/docs/start
categories: []
tags: []
keywords: []
createat: "2022-12-30T15:49:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2023-01-01T09:54:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: 8
---
我们在 Github Action 中找到 **[Notion-Site](https://github.com/marketplace/actions/notion-site)**  **，** 就可以在 **Github** 中随意使用了，代码如下：


 ```yaml
 - name: notion-site
  uses: pkwenda/notion-site@v1.0.3
 ```
 <!--more-->为了节省大家的时间，已经创建好了一套默认流程，可以直接使用：

[https://github.com/pkwenda/notion-hugo-website-builder](https://github.com/pkwenda/notion-hugo-website-builder)

直接点击：use the template 创建自己的仓库即可，默认实现流程如下：

{{< bookmark image="https://github.githubassets.com/images/modules/open_graph/github-logo.png" icon="https://github.githubassets.com/favicons/favicon.svg" url="https://github.com/pkwenda/notion-hugo-website-builder/blob/main/.github/workflows/builder.yml"  des="GitHub is where people build software. More than 94 million people use GitHub to discover, fork, and contribute to over 330 million projects."  title="Build software better, together"  >}}
- 创建 ubuntu 容器

- 设置每天执行一次

- 拉取本仓库代码（并递归下载 sub model 主题）

- 清空上次拉取的 Page

- 从 Notion 拉取最新的 Page

- 提交保存最新的 Page >> markdown 到本仓库做备份

- 拉取 hugo docker，并编译为网站要素，提交到 XXX 分支

以上所有的配置用户可以根据自己的需求自行调整，参考文档：

{{< bookmark image="https://github.githubassets.com/images/modules/open_graph/github-logo.png" icon="https://docs.github.com/assets/cb-803/images/site/favicon.svg" url="https://docs.github.com/en/actions"  des="Automate, customize, and execute your software development workflows right in your repository with GitHub Actions. You can discover, create, and share actions to perform any job you'd like, including CI/CD, and combine actions in a completely customized workflow."  title="GitHub Actions Documentation - GitHub Docs"  >}}
{{< tip >}}

至此，我们已经拥有了一个每天不断从 Notion 更新的静态网站仓库，我们可以在手机、平板、电脑等任何设备和平台对网站进行编辑和管理。

{{< /tip >}}

下一步只需要考虑部署到服务器即可，Notion-Site 默认提供 Vercel 部署方案，至于其他发布平台或部署到自己服务器的 Nginx ，需要根据自己的情况定制化调整配置文件，Github Action 已经有很多成熟的组件：

- Nettxxx

- SFTP

- FTP

- AWS

等等通用的 Upload 方式，只需要根据自己的实际情况调整即可。

