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
