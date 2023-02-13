---
title: Github Action
status: Published
position: content/docs/introduce
categories: []
tags: []
keywords: []
createat: "2022-12-29T09:41:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2023-01-02T15:50:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: 5
---
Notion-Site 的架构涉及中的自动化部署环境是依赖 Github Action 的能力展开的，我们可以直接在应用市场中找到 Notion-Site 程序免费使用服务，使用 Github Action 容器还可以规避中国大陆访问 Notion 接口不稳定的问题。



<!--more-->-  ***[Github Action](https://docs.github.com/en/actions)***  **[ 官方文档](https://docs.github.com/en/actions)** 



### 配置文件
如果没有特殊需求，使用 Notion-Site 默认模板默认的配置文件可以满足大部分的需求：



### 计费标准
Github Action 是否收费的规则比较透明，下面是计费规则：

-  **[关于 Github Action 的计费](https://docs.github.com/zh/billing/managing-billing-for-github-actions/about-billing-for-github-actions)** 

如果你的仓库是公开的就免费，如果有隐私方面的顾虑，私有仓库也可以提供下面的免费额度。




| 产品 | 存储 | 分钟数（每月） |
| --- | --- | --- |
| GitHub Free | 500 MB | 2,000 |
| GitHub Pro | 1GB | 3,000 |
| 组织的 GitHub Free | 500 MB | 2,000 |
| GitHub Team | 2 GB | 3,000 |
| GitHub Enterprise Cloud | 50 GB | 50,000 |
<!--more-->即使你不是 Github 的付费用户，每天也有近一个小时的容器使用时间（这里默认指的是  Ubuntu 容器）



### 每次部署的时间
每次部署的时间与文章的数量，文章内媒体资源的大小正相关，可以在 action 页面的历史看到每次部署花费了多少服务器时间：



当然如果是 public 仓库就不用担心时间的问题。



### 个性化配置
模板中默认使用的配置是每天部署一次，这意味着每天 Notion-Site 会基于 Github 提供的服务器拉取在 Notion 中维护的所有文章自动进行部署。

具体调整配置可以参考 Github Action 文档，比如如果想调整为：

每小时一次：

可以直接调整 cron 属性的值，调整自动部署的方式和频率，参考下列文章：



{{< bookmark image="https://mcusercontent.com/ea228d7061e8bbfa8639666ad/images/2a002353-3bec-fbab-b0e3-e8eef1ac0e52.png" icon="https://crontab.guru/favicon.ico" url="https://crontab.guru/"  des="An easy to use editor for crontab schedules."  title="Crontab.guru - The cron schedule expression editor"  >}}

{{< bookmark image="https://github.githubassets.com/images/modules/open_graph/github-logo.png" icon="https://docs.github.com/assets/cb-803/images/site/favicon.svg" url="https://docs.github.com/en/actions/quickstart"  des="Try out the features of GitHub Actions in 5 minutes or less."  title="Quickstart for GitHub Actions - GitHub Docs"  >}}

