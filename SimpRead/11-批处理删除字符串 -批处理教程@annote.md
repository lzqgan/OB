---
title: "批处理删除字符串 -
		批处理教程"
alias: 
  - "批处理删除字符串 -
		批处理教程"
created-date: 2023-03-24T04:51:55+0800
type: Simpread
tag: 
idx: 11
---

# 批处理删除字符串 -
		批处理教程

> [!example]- [🌐外部链接](<https://www.yiibai.com/batch_script/batch_script_remove.html>)    
> URI:: [🌐](<https://www.yiibai.com/batch_script/batch_script_remove.html>) 
> intURI:: [🧷内部链接](<https://www.yiibai.com/batch_script/batch_script_remove.html>)

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
>  **Description**:: 字符串替换功能也可以用来从一个字符串中删除一个子字符串。
%%

> [!md] Metadata  
> **标题**:: [批处理删除字符串 -
		批处理教程](https://www.yiibai.com/batch_script/batch_script_remove.html)  
> **日期**:: [[2023-03-24]]  

## Annotations


> [!srhl2] [[SR11@批处理删除字符串 -
		批处理教程|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 字符串替换功能也可以用来从一个字符串中删除一个子字符串。
> 
> **示例**
> 
> ```
> @echo off   
> set str=Batch scripts is easy. It is really easy.   
> echo %str%   
>   
> set str=%str:is=%   
> echo %str%  
>   
> 
> ```
> 
> 关于上述程序是要注意的是，`'is'`这个词是使用`'stringtoberemoved'=`命令从字符串中删除。
> 
> 以上命令产生以下输出。
> 
> ```
> Batch scripts is easy. It is really easy.   
> Batch scripts easy. It really easy.
> ```
> ^sran-1679604715828

