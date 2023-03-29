---
title: "用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布"
alias: 
  - "用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布"
created-date: 2023-03-24T00:38:26+0800
type: Simpread
banner: "https://cdn.sspai.com/article/72ff0d31-69f7-470c-e4e8-7a6b41569772.jpg "
banner_icon: 🔖
tag: 
idx: 8
---

# 用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布

> [!example]- [🌐外部链接](<https://sspai.com/post/58013>)    
> URI:: [🌐](<https://sspai.com/post/58013>) 
> intURI:: [🧷内部链接](<https://sspai.com/post/58013>)

%%
> [!example]+ **Comments**  
> ```dataview
> TABLE 
>     WITHOUT ID
>     link(Source, dateformat(date(Source), "yyyy-MM-dd")) as Date___, 
>     regexreplace(rows.Comments,"^@@\[\[.+?\]\]\s","") as "Comments"
> FROM "journals"
> WHERE  contains(cmnt, this.file.name)
> FLATTEN cmnt as Comments
> WHERE contains(Comments, this.file.name)
> GROUP BY file.link as Source
> SORT rows.file.day desc
> ```
>  **Description**:: 在个人博客式微的今天，希望大家都能再去试试这个纯粹、自由的媒介，在互联网上拥有属于自己的一亩三分地其实是种很不错的体验。
%%

> [!md] Metadata  
> **标题**:: [用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布](https://sspai.com/post/58013)  
> **日期**:: [[2023-03-24]]  

## Annotations


> [!srhl2] [[SR8@用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 除文本内容外，对图片等附件的管理也是相当棘手的问题。由于 Markdown 能力有限，人们倾向于把图片上传至第三方图床，然后在文章中通过链接引用。然而这算不得可靠的方案。今年年初就由于新浪突然对自己的图片服务增加访问限制，一众使用新浪图床的博主都只能叫苦连天。最好的方法是保证 Markdown 文本文件与图片文件位于同处，文章内通过相对位置（例如 `./images/1.png` 这样的链接）引用图片，自给自足，以最大程度保证持久性与可访问性。
> ^sran-1679589738924

> [!srhl2] [[SR8@用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 第一类，仓库名形如 `<用户名>.github.io`。开启 Pages 服务后可以直接通过 `http://<用户名>.github.io` 访问。
> 
> 第二类，其它名称的仓库。对这些仓库，开启 Pages 服务后可以通过 `http://<用户名>.github.io/<仓库名>` 访问。
> ^sran-1679590052299

> [!srhl2] [[SR8@用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 两类仓库都可以指定部署的内容来源，包括
> ^sran-1679590048259

> [!srhl2] [[SR8@用 GitHub 搭建静态博客太繁琐？用这个小工具实现「傻瓜式」发布|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> Create new file
> ^sran-1679590364586

