#linux 
bilibili教程：（MAC配置教程，linux可以使用root用户配置，步骤差不多）
https://www.bilibili.com/video/BV1HM411377j?p=11&vd_source=d8a789090c32450316caa55f99960e3e

用户名：Poriacoco
密码：Poria.0818

```
git add . //添加至工作区
git commit -m "just write down something"//添加到本地仓库.git
git push  //将本地仓库同步到远程仓库

git pull //从远程仓库同步到本地仓库
```

## ssh配置
1. 进入～/.ssh
2. ssh -keygen -t rsa -b 4096，
- 会生成test （私钥）&test.pub（公钥） 两个文件![[Pasted image 20240604202939.png]]
3. 复制.pub文件内容
4. github创建ssh keys，粘贴复制内容![[Pasted image 20240604203119.png]]
5. .ssh/下touch一个config文件，收入#github下面这几行![[Pasted image 20240604203404.png]]
6. 完成配置。
