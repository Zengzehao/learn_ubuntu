### 1.显示时间
date

### 2.显示日期
cal

### 3.使用计算器
bc

### 4.man或者info命令
当你不知道某个命令如何使用的时候 可以用
例如： man date
就会出现date的用法

### 5.一个超级简单的编辑器
nano

### 6.正确关机的命令
shutdown 或者 poweroff

### 7.理解档案拥有者 群组 其他人的概念

### 8.档案属性与档案类型
![](/文档属性.png)

![](/档案类型.png)

### 9.如何改变文件属性与权限
- chgrp :改变档案所属群组
- chown :改变档案拥有者
- chmod :改变档案的权限, SUID, SGID, SBIT 等等的特怅

重点看一下如何使用chmod  
数字分别代表的权限：
r:4  w:2  x:1
例如：
chmod 777 filename

还有一个改变权限的方法,(1)user(2)group (3)others 三种身份啦!那举我们就可以藉由 u, g, o 来代表三种身份的权限!此外,
a 则代表 all 亦即全部的身份!那举读写的权限就可以写成 r, w, x 啰!
例如：   
chmod u=rwx,go=rx .bashrc   
chmod a+w .bashrc

### 10.ubuntu下文件压缩解压缩命令
http://www.cnblogs.com/haoyijing/p/5810079.html
- .gz   
解压1：gunzip FileName.gz  
解压2：gzip -d FileName.gz   
压缩：gzip FileName  

- .tar.gz   
解压：tar zxvf FileName.tar.gz   
压缩：tar zcvf FileName.tar.gz DirName   
---------------------------------------------
- .bz2    
解压1：bzip2 -d FileName.bz2   
解压2：bunzip2 FileName.bz2    
压缩： bzip2 -z FileName   

- .tar.bz2    
解压：tar jxvf FileName.tar.bz2    
压缩：tar jcvf FileName.tar.bz2 DirName    
---------------------------------------------
- .bz   
解压1：bzip2 -d FileName.bz    
解压2：bunzip2 FileName.bz   
压缩：未知   

- .tar.bz   
解压：tar jxvf FileName.tar.bz   
压缩：未知
---------------------------------------------
- .Z    
解压：uncompress FileName.Z    
压缩：compress FileName    

- .tar.Z    
解压：tar Zxvf FileName.tar.Z    
压缩：tar Zcvf FileName.tar.Z DirName    
---------------------------------------------
- .tgz    
解压：tar zxvf FileName.tgz    
压缩：未知   

- .tar.tgz    
解压：tar zxvf FileName.tar.tgz    
压缩：tar zcvf FileName.tar.tgz FileName   
---------------------------------------------
- .zip    
解压：unzip FileName.zip   
压缩：zip FileName.zip DirName   
---------------------------------------------
- .rar    
解压：rar a FileName.rar   
压缩：r ar e FileName.rar    

#### 11.学习vim 编辑器

#### 12.命令编修能力 (history)
使用history命令，我们可以知道之前执行的命令
~/.bash_hostiry (所有的历史记录都在这个文件)

#### 13.命令不档案补全功能: ([tab] 挄键的好处)
tab键 这是是我最喜欢的一个键了。

#### 14.系统备份与还原
经过上次把系统给搞崩溃的经历，我现在迫不及待想备份一份系统
http://www.linuxidc.com/Linux/2015-12/126216.htm
tar -vczf /backup.tar.gz --exclude=/proc --exclude=/sys --exclude=/backup.tar.gz /
备份的命令
tar -vxzf /backup.tar.gz -C /
还原系统，会把一切文件覆盖掉，所以要非常地小心。
