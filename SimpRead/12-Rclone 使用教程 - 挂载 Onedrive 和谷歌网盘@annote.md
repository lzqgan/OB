---
title: "Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘"
alias: 
  - "Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘"
created-date: 2023-03-24T20:29:11+0800
type: Simpread
banner: "https://bkqsimg.ikafan.com/upload/chatgpt-s.png?! "
banner_icon: 🔖
tag: 
idx: 12
---

# Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘

> [!example]- [🌐外部链接](<https://www.shuzhiduo.com/A/ZOJPNy1ydv/>)    
> URI:: [🌐](<https://www.shuzhiduo.com/A/ZOJPNy1ydv/>) 
> intURI:: [🧷内部链接](<https://www.shuzhiduo.com/A/ZOJPNy1ydv/>)

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
>  **Description**:: 
%%

> [!md] Metadata  
> **标题**:: [Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘](https://www.shuzhiduo.com/A/ZOJPNy1ydv/)  
> **日期**:: [[2023-03-24]]  

## Annotations


> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> ### 2.1 下载安装 rclone
> 
> 1.  windows 版本：下载 [rclone](https://rclone.org/downloads/) 并解压
>
> ^sran-1679660951451

> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> ### 2.2 配置 OneDrive
> 
> 1.  在目录下打开 cmd 运行命令 `rclone authorize "onedrive"`
>     
>       
>     
>     世纪互联运行的命令 `rclone authorize onedrive "应用程序(客户端)ID" "客户端密码值" --onedrive-is-21vianet-version=true`
>
> ^sran-1679660958084

> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 配置
> 
>   
> 
> ```
> rclone config
> ```
> ^sran-1679660962226

> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> ### 2.4 获取配置文件
> 
> 搜索 ，windows 下正常都在 `C:\Users\你的用户名\\.config\rclone`目录下，Linux 正常都在 `./.config/rclone/`目录下
> ^sran-1679660973866

> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 3. 使用教程
> -------
> 
> 常用命令：
> 
> ```
> rclone config - 以控制会话的形式添加rclone的配置，配置保存在.rclone.conf文件中。  
> rclone copy - 将文件从源复制到目的地址，跳过已复制完成的。  
> rclone sync - 将源数据同步到目的地址，只更新目的地址的数据。  
> rclone move - 将源数据移动到目的地址。  
> rclone delete - 删除指定路径下的文件内容。  
> rclone purge - 清空指定路径下所有文件数据。  
> rclone mkdir - 创建一个新目录。  
> rclone rmdir - 删除空目录。  
> rclone check - 检查源和目的地址数据是否匹配。  
> rclone ls - 列出指定路径下所有的文件以及文件大小和路径。  
> rclone lsd - 列出指定路径下所有的目录/容器/桶。  
> rclone lsl - 列出指定路径下所有文件以及修改时间、文件大小和路径。  
> rclone md5sum - 为指定路径下的所有文件产生一个md5sum文件。  
> rclone sha1sum - 为指定路径下的所有文件产生一个sha1sum文件。  
> rclone size - 获取指定路径下，文件内容的总大小。.  
> rclone version - 查看当前版本。  
> rclone cleanup - 清空remote。  
> rclone dedupe - 交互式查找重复文件，进行删除/重命名操作。  
> 
> ```
> 
> 1.  显示网盘上的目录
>     
>       
>     
>     ```
>     rclone lsd onedrive:   #onedrive是上面设置的名称  
>     rclone lsd gdrive:    #gdrive是上面设置的名称  
>     
>     ```
>     
>   
> 3.  拷贝谷歌网盘上的文件到 Onedrive
>     
>       
>     
>     ```
>     !rclone copy gdrive:music onedrive:音乐 --ignore-existing --config ./music/rclone.conf  
>     # --config xxxx.conf 表示指定配置文件  
>     # --ignore-existing表示跳过已存在的文件  
>     # 此命令表示将谷歌网盘下的music目录复制到Onedrive网盘下的音乐目录  
>     
>     ```
>     
>   
> 5.  挂在 Onedrive
>     
>       
>     
>     ```
>     rclone mount onedrive:音乐 music --copy-links --no-gzip-encoding --no-check-certificate --allow-other --allow-non-empty --umask 000 --config /co
>     ```
>
> ^sran-1679661243845

> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> 4. Linux 上挂载网盘
> --------------
> 
> 1.  新建 Linux 下的文件夹
>     
>       
>     
>     ```
>     rm -rf /root/music  #删除已有的目录  
>     mkdir /root/music  #新建目录  
>     
>     ```
>     
>   
> 3.  挂载磁盘
>     
>       
>     
>     下载脚本
>     
>       
>     
>     ```
>     wget -N --no-check-certificate https://raw.githubusercontent.com/x91270/Centos/master/rcloned  
>     
>     ```
>     
>       
>     
>     使用 `vim rcloned`修改脚本项
>     
>       
>     
>     ```
>     NAME="myone" #创建的rclone名，本文此处填ojbk  
>     REMOTE="音乐" #远程挂载地址对应的文件夹，是你OneDrive对应的具体目录  
>     LOCAL="/root/music" #在本机上的挂载地址  
>     
>     ```
>     
>       
>     
>     启动脚本 `rcloned start`
>     
>   
> 5.  挂载成功后，输入`df -h`命令查看
>     
>       
>     
>   
> 7.  设置开机启动
>     
>       
>     
>     ```
>     mv rcloned /etc/init.d/rcloned    #移动rcloned到init(开机启动目录)下  
>     chmod +x /etc/init.d/rcloned      #给rcloned可执行权限  
>     chkconfig rcloned on                   #设置自启动  
>     bash /etc/init.d/rcloned start       #启动rclone
>     ```
>
> ^sran-1679661249995

> [!srhl2] [[SR12@Rclone 使用教程 - 挂载 Onedrive 和谷歌网盘|📄]] <mark style="background-color: #ffeb3b">Highlights</mark>   
> ![](https://i.loli.net/2020/08/15/y2B5TYqenzbkDcX.png)
> ^sran-1679661250036

