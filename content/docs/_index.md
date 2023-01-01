---
title: Notion Site Doc
status: Published
position: content/docs
categories: []
tags: []
keywords: []
createat: "2022-12-29T08:17:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2023-01-01T17:24:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: null
---

Notion-Site 是一个打通 Notion 与 Hugo 的自动建站工具，它比 Notion 默认提供的 Share 功能更适用于构建网站，我们可以使用 Hugo 提供的 200 多种类型的主题创建我们的网站。只需要一次配置之后，无需记忆命令、无需服务器、我们只需要在任何设备的 Notion 中正常写文章就可以随时随地编辑网站。

<!--more-->![](media/s3.us-west-2.amazonaws.com_1dbf46ad-691b-4b0e-9cf7-fb3140b37958.png)

![](media/s3.us-west-2.amazonaws.com_a8bac8cf-c661-48ef-adb2-46e441bee15a.png)

### Notion 做为博客的不足

Notion 因为自带分享链接，所以近几年我们通常直接分享 Notion 的地址作为我们的博客、文档站，或者使用类似 **_[Notion-Blog](/3dab2163acdb415aaf6514b3c00368c5)_** 等开源方案做 1:1 的转换。

也可以在 **[Cloudflare Web Worker](https://developers.cloudflare.com/dns/zone-setups/full-setup/setup)** 提供的能力绑定域名、CDN 提速等等：

{{< bookmark image="https://res.cloudinary.com/practicaldev/image/fetch/s--9mAvnDqk--/c_imagga_scale,f_auto,fl_progressive,h_500,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pnivzp4qvskmpr5ppk4f.png" icon="https://res.cloudinary.com/practicaldev/image/fetch/s--lrmEcD2H--/c_limit,f_png,fl_progressive,q_80,w_128/https://practicaldev-herokuapp-com.freetls.fastly.net/assets/devlogo-pwa-512.png" url="https://dev.to/koddr/using-the-notion-page-as-a-personal-website-with-your-domain-on-cloudflare-1pi7"  des="Introduction   Hi, DEV people! 🙂 Today, I give you a handy step-by-step guide to help you..."  title="🌐 Using the Notion page as a personal website with your domain on Cloudflare"  >}}

### **Notion 缺失的功能：**

- <span style="color: rgba(212, 76, 71, 1);">没有 RSS 订阅</span>

- <span style="color: rgba(212, 76, 71, 1);">加载的 notion 资源太多，打开文章较慢</span>

- <span style="color: rgba(212, 76, 71, 1);">中国大陆访问速度慢</span>

- <span style="color: rgba(212, 76, 71, 1);">文章链接太长，如想缩短需要针对每个文章使用</span><span style="color: rgba(212, 76, 71, 1);"> **[Cloudflare Web Worker](https://developers.cloudflare.com/dns/zone-setups/full-setup/setup)** </span><span style="color: rgba(212, 76, 71, 1);">做映射</span>

- <span style="color: rgba(212, 76, 71, 1);">缺失很多博客的要素：时间轴、分类、标签，更像是笔记</span>

- <span style="color: rgba(212, 76, 71, 1);">只有 Notion 的风格，主题样式太单一，无法定制化</span>

### Hugo 的缺点

- <span style="color: rgba(212, 76, 71, 1);"> **shortcodes** </span><span style="color: rgba(212, 76, 71, 1);">很难维护，在 MD 编辑器中不伦不类</span>

- <span style="color: rgba(212, 76, 71, 1);">备份需要成本</span>

- <span style="color: rgba(212, 76, 71, 1);">需要维护一些部署脚本</span>

- <span style="color: rgba(212, 76, 71, 1);"> **Hugo** </span><span style="color: rgba(212, 76, 71, 1);">很难用任何设备（手机，平板）维护网站文章</span>

在希望实现上面的需求的同时，保留 Notion 的便利性，与 Hugo 平台深度绑定，开发了 Notion-Site。

{{< tip >}}

我们要做的只是在 Notion 中编辑文章即可。 **只需要一次配置实现** ：

- <span style="color: rgba(68, 131, 97, 1);">备份交给</span><span style="color: rgba(68, 131, 97, 1);"> **Notion 、 Github Repository** </span>

- <span style="color: rgba(68, 131, 97, 1);">自动化交给 ：</span><span style="color: rgba(68, 131, 97, 1);"> **Github Action** </span>

- <span style="color: rgba(68, 131, 97, 1);">自动部署交给：</span><span style="color: rgba(68, 131, 97, 1);"> **Vercel** </span>

{{< /tip >}}

### Notion-Site 构建流程

{{< mermaid >}}
graph TD
A[Notion DataBase] -->|Notion-Site| B(Get Pages)
B --> C{Process Pages To Hugo}
C -->|setting| D[Hugo Setting Files]
C -->|Article| E[Hugo Content Files]
E -->|Folder| G[Folder]
E -->|Article| H[Markdown files]
E -->|Media| I[Downlaod Meida files]
{{< /mermaid >}}

{{< mermaid >}}
graph TD

    Hugo -->|CI| J[GitHub ACtion] --> Vercel --> DPD[Complete the deployment]

{{< /mermaid >}}
