---
title: Shortcodes Example
status: Published
position: content/docs/example
categories: []
tags: []
keywords: []
createat: "2023-01-02T13:47:00+07:00"
author: nonacosa
istranslated: true
lastmod: "2023-01-02T15:41:00+07:00"
description: ""
draft: null
expirydate: null
show_comments: false
slug: ""
image: null
weight: 2
---


该页面 Notion 原文链接：[Shortcodes Example](https://www.notion.so/f0fd1ed702d54115b851c7ebe572dc45)



<!--more-->

### Youtube

{{< youtube id="ICM6AI1kPAA" >}}



### Code

 ```javascript
 mermaidAPI.initialize({
  securityLevel: 'loose',
  theme: 'base',
});
 ```
 

### Mermaid

{{< mermaid >}}
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    section Section
    A task           :a1, 2014-01-01, 30d
    Another task     :after a1  , 20d
    section Another
    Task in sec      :2014-01-12  , 12d
    another task      : 24d
{{< /mermaid >}}




### twitter

{{< tweet id="1544616550074056710" user="sis_nonacosa" >}}

### Audio

{{< audio src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/086b7818-5b65-445e-8bbc-9821fe478125/Curious.George.S01E01.Curious.George.Flies.a.Kite.-.From.Scratchwww.oiabc.com.mp3?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230112%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230112T040220Z&X-Amz-Expires=3600&X-Amz-Signature=5748c0782bcc90950c1e78d31a64882164855dedbea61729848e6b6c7a756e29&X-Amz-SignedHeaders=host&x-id=GetObject" >}}

### PDF

{{< pdf url="media/s3.us-west-2.amazonaws.com_Dingoes_at_Dinnertime.pdf" >}}


### BookMark
{{< bookmark image="https://mcusercontent.com/ea228d7061e8bbfa8639666ad/images/2a002353-3bec-fbab-b0e3-e8eef1ac0e52.png" icon="https://api.daily.dev/favicon.ico" url="https://api.daily.dev/r/dn4_W4VWu"  des="The top 30 tools of 2022, as determined by the number of unique clicks in this newsletter over the past 12 months."  title="Web Tools #493 - The Top 30 Tools of 2022"  >}}



### JsFiddle

{{< jsfiddle url="dmrt5f4w" >}}

### iframe

{{< iframe "https://ciphrd.com/" >}}

### Gist

{{< gist  pkwenda ecc8cc891754a32a479ab74c6aad4e5c >}}



### 自定义 shortcodes
主题中有很多自己实现的 shortcodes，Notion-Site 无法全部支持，当需要使用时，不妨直接写出主题中示例的原文：

{{< tip >}}

这是一个提示！

{{< /tip >}}

后期 Notion-Site 会规划用户自定义 shortcodes 像配置文件一样，通过 Notion 存储，下载，覆盖。

