#linux #权限 
问题：[[用户sudo命令权限设置.png]]
解决方法：
https://blog.csdn.net/csdnzouqi/article/details/95499348
```
	su - root
	chmod 640 /etc/sudoers
#更改sudoers文件
	vim /etc/sudoers
#所示位置加上`用户名 ALL=(ALL) ALL`后保存并退出
```
