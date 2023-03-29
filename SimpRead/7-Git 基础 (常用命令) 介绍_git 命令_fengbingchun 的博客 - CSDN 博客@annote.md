---
title: "Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客"
alias: 
  - "Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客"
created-date: 2023-03-23T22:29:50+0800
type: Simpread
tag: 
idx: 7
---

# Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客

> [!example]- [🌐外部链接](<https://blog.csdn.net/fengbingchun/article/details/45847439/>)    
> URI:: [🌐](<https://blog.csdn.net/fengbingchun/article/details/45847439/>) 
> intURI:: [🧷内部链接](<https://blog.csdn.net/fengbingchun/article/details/45847439/>)

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
>  **Description**:: 版本控制是一种记录若干文件内容变化,以便将来查阅特定版本修订情况的系统.关于版本控制分为三种：本地版本控制系统，如rcs；集中化的版本控制系统，如CVS、SVN；分布式版本控制系统，如Git。Git基础要点Git和其它版本控制系统的主要差别在于：Git只关心文件数据的整体是否发生变化，而大多数其它系统则只关心文件内容的具体差异。对于任何一个文件，在Git内都只有三种状态：已提交(c......
%%

> [!md] Metadata  
> **标题**:: [Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客](https://blog.csdn.net/fengbingchun/article/details/45847439/)  
> **日期**:: [[2023-03-23]]  

## Annotations


> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 基本的 Git 工作流程：(1)、在工作目录中修改某些文件；(2)、对这些修改了的文件作快照，并保存到暂存区域；(3)、提交更新，将保存在暂存区域的文件快照转储到 git 目录中。
> ^sran-1679581790803

> [!srhl6] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffb7da">Highlights</mark> #git   
> 对于已安装的 Git，第一个要配置的是你个人的用户名称和电子邮件地址。这两条配置很重要，每次 Git 提交时都会引用这两条信息，说明是谁提交了更新，所以会随更新内容一起被永久纳入历史记录：
> 
> ```
> $ git config --global user.name "Spring"  
> $ git config --global user.email Spring@163.com  
>   
> 
> ```
> 
> 如果用了 --global 选项，那么更改的配置文件就是位于你用户主目录的那个，以后你所有的项目都会默认使用这里配置的用户信息。如果要在某个特定的项目中使用其他名字或者电邮，只要去掉 --global 选项重新配置即可，新的设定保存在当前项目的./git/config 文件里。
> ^sran-1679582012188

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> Git 常用命令
> ^sran-1679582094115

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 有两种取得 Git 项目仓库的方法。
> ^sran-1679582102538

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 第一种是在现存的目录下，通过导入所有文件来创建新的 Git 仓库：(1)、从当前目录初始化：$ git init , 初始化后，在当前目录下会出现一个名为. git 的目录，所有 Git 需要的数据和资源都存放在这个目录中；(2)、如果当前目录下有几个文件想要纳入版本控制，需要先用 git add 命令告诉 Git 开始对这些文件进行跟踪，然后提交：
> 
> ```
> $ git add README    
> $ git commit -m 'initial project version'   
> 
> ```
> 
> 其中 README 文件是已经存在在当前目录中的。git add 后可以接要跟踪的文件或目录的路径。如果是目录的话，就说明要递归跟踪所有该目录下的文件。
> ^sran-1679582129013

> [!srhl6] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffb7da">Highlights</mark> #git   
> 第二种是从已有的 Git 仓库克隆出一个新的镜像仓库来，如：
> 
> ```
> $ git clone git://github.com/schacon/grit.git  
> 
> ```
> 
> 如果希望在克隆的时候，自己定义要新建的项目目录名称，可以在上面的命令最后指定：
> 
> ```
> $ git clone git://github.com/schacon/grit.git mygrit  
> 
> ```
> 
> 唯一的差别就是，现在新建的目录成了 mygrit，其它的都和上边的一样。
> ^sran-1679582142483

> [!srhl6] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffb7da">Highlights</mark> #git   
> 检查当前文件状态：
> 
> ```
> $ git status
> ```
> ^sran-1679582268555

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 每次准备提交前，先用 git status 看下，是不是都已经暂存起来了，然后在运行提交命令：
> 
> ```
> $ git commit
> ```
> ^sran-1679582317339

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 这种方式会启动文本编辑器以便输入本次提交的说明，也可以使用 - m 参数后跟提交说明的方式：
> 
> ```
> $ git commit -m "commit message"
> ```
> ^sran-1679582330939

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 提交更新：现在的暂存区域已经准备妥当可以提交了。在此之前，请一定要确认还有什么修改过的或新建的文件还没有 git  add 过，否则提交的时候不会记录这些还没暂存起来的变化。所以，每次准备提交前，先用 git  status 看下，是不是都已暂存起来了，然后再运行提交命令 git  [commit](https://so.csdn.net/so/search?q=commit&spm=1001.2101.3001.7020)。  
> 跳过使用暂存区域：只要在提交的时候，给 git  commit 加上 - a 选项，Git 就会自动把所有已经跟踪过的文件暂存起来一并提交，从而跳过 git  add 步骤。
> ^sran-1679582546750

> [!srhl2] [[SR7@Git 基础 (常用命令) 介绍_git 命令_fengbingchun 的博客 - CSDN 博客|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 移除文件：要从 Git 中移除某个文件，就必须要从已跟踪文件清单中移除（确切地说，是从暂存区域移除），然后提交。可以用 git  rm 命令完成此项工作，并连带从工作目录中删除指定的文件，这样以后就不会出现在未跟踪文件清单中了：
> 
> ```
> $ git rm README
> ```
> ^sran-1679582586250

