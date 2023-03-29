1 认证、
```
git config --global user.name "lzqgan"
git config --global user.email "lzqgan@126.com"
git config --global credential.helper store
```
2 仓库初始化
```git init```
3 克隆
```
git clone 复制的SSH或者HTTPS key
```
4 上传 
```
git pull
git add .
git commit -m "Update site"
git push
```
5 token加入远程仓库
token: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
```
git remote add origin https://(token)@(复制的SSH或者HTTPS)
```
例子：git remote add origin https://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@github.com/lzqgan/Blog-With-GitHub-Boilerplate.git

> [!md]  一直无法同步，网上的方法
> **使用此方法成功上传**
> [github访问令牌token的创建方法 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/501872439)
> 第七步、使用token
> 那我创建完了，我怎么用呢？我们需要进行一下几步完成token的使用；
> 1、删除远程仓库地址
> 如果刚初始化的本地仓库，忽略这一步！
> git remote remove origin
> 可以通过一下命令查看是否删除成功，无内容输出意味着已经删除成功了！
> git remote -v
> 2、链接远程仓库
> 把token放在远程仓库地址里，如下所示：
> git remote add origin https://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@github.com/xxx/xxxx.git
> 3、成功
> 完成以上步骤之后，就可以正常拉取、上传你的仓库代码了！

