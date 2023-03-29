---
title: "Git Bash 的简单使用教程"
alias: 
  - "Git Bash 的简单使用教程"
created-date: 2023-03-24T03:41:19+0800
type: Simpread
banner: "https://pic1.zhimg.com/v2-364b3b84c530fa02ee988088b3c0e0b5_720w.jpg?source=172ae18b "
banner_icon: 🔖
tag: 
idx: 9
---

# Git Bash 的简单使用教程

> [!example]- [🌐外部链接](<https://zhuanlan.zhihu.com/p/124687836?from_voters_page=true>)    
> URI:: [🌐](<https://zhuanlan.zhihu.com/p/124687836?from_voters_page=true>) 
> intURI:: [🧷内部链接](<https://zhuanlan.zhihu.com/p/124687836?from_voters_page=true>)

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
>  **Description**:: Git的下载安装及配置详见这篇笔记： HUST小菜鸡：Git的下载安装及配置一、本地文件的基本操作进入某一个文件夹，和Linux系统一样有两种方式： 直接进入该文件夹位置，然后右键Git Bash Here，在当前文件夹打开Git …
%%

> [!md] Metadata  
> **标题**:: [Git Bash 的简单使用教程](https://zhuanlan.zhihu.com/p/124687836?from_voters_page=true)  
> **日期**:: [[2023-03-24]]  

## Annotations


> [!srhl2] [[SR9@Git Bash 的简单使用教程|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> ### 4、内容同步
> 
> 在第一次同步的时候，必须使用如下指令
> 
> ```
> git push -u 仓库代称 master  
> 
> ```
> 
> 第一次推送 master 分支时，必须加上 - u 参数，git 不但会推送分支，还会把本地 master 分支与远程 master 分支相关联，以后的推送直接使用 git push 仓库代称 master 即可
> 
> ```
> git push 仓库代称 master  
> 
> ```
> 
> 同步后可以进 GitHub 的 web 端看已经被修改
> ^sran-1679600522834

> [!srhl2] [[SR9@Git Bash 的简单使用教程|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> ![](https://pic3.zhimg.com/v2-f613d6cc072e3cb0b1ceabf99db8b896_r.jpg)
> ^sran-1679600522869

