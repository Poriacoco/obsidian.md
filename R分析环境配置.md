#R #bioinfo #linux 
# R-server 安装
## 正常安装过程
1. 安装R以及rstudio
2. 修改R路径 
     基因学苑文档-10.biostation 
```
vi /etc/rstudio/rserver.conf
```
3. 重启 -stop -start -status
4. 修改防火墙配置
 ```
systemctl start firewalld #开启防火墙
systemctl status firewalld #查看状态
firewall-cmd --permanent --add-port=8787/tcp
firewall-cmd --permanent --add-port=8787/udp
firewall-cmd --reload
 ```
 5. 云服务器修改防火墙
 ![[云服务器防火墙配置8787端口.png]]
 6.  浏览器输入101.43.61.245:8787，完成登录（root不可登录）
## 浏览器无法登录server
- 浏览器无法链接：unable to connect to service(1)
```
#linux下检查是否安装成功
rstudio-server verify-installation
```
- 这一步骤会报错，貌似是gcc相关的包版本过低，两篇文章供参考
- https://blog.csdn.net/u012322399/article/details/120065301
- https://blog.csdn.net/L1481333167/article/details/137919464


## 解决操作实例 

1. **step1 -找到目录中高版本的libstdc++.so.6.0.32**
	 *根据step2,这个包可能是conda安装的*
![[locate libstdc++.so.6.png]]
2. **step2-创建软链接**
![[Pasted image 20240531161222.png]]
**3.step3-检查安装状态并启动服务，未显示报错**
![[Pasted image 20240531161628.png]]
4. **step -浏览器登录成功，收工![[Pasted image 20240531161710.png]]**