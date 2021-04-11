# 1 显示文件列表命令 ls
![linux1](https://github.com/killmichael/Scala.github.io/blob/main/linux1.png)

# 2 目录操作指令
## 2.1 pwd
查看当前所在路径

## 2.2 cd
![linux2](https://github.com/killmichael/Scala.github.io/blob/main/linux2.png)

## 2.3 mkdir
mkdir dir  #创建单级目录
mkdir /etc/dir  #在已有的etc文件夹下创建dir
mkdir -p aaa/bbb/ccc  #创建多级目录

## 2.4 rm
![linux3](https://github.com/killmichael/Scala.github.io/blob/main/linux3.png)

# 3 文件操作命令
## 3.1 touch
touch a.txt  #创建a.txt文件
touch a.txt b.txt c.txt  #创建多个文件

## 3.2 mv
移动： mv a.txt dir  #将a.txt移动到dir目录下
       mv dir dir2   #将dir2目录移动到dir目录
重命名： mv a.txt b.txt
         mv dir2 dir22
![linux4](https://github.com/killmichael/Scala.github.io/blob/main/linux4.png)

## 3.3 cat
显示文件内容
cat /root/initial.cfg

## 3.4 more
按页或者按行显示文件内容
![linux5](https://github.com/killmichael/Scala.github.io/blob/main/linux5.png)

## 3.5 cp
文件或目录的复制
![linux6](https://github.com/killmichael/Scala.github.io/blob/main/linux6.png)

# 4 系统管理命令
## 4.1 ps
列出系统中当前运行的进程
ps -ef  #查看所有进程

## 4.2 kill
终止执行中的程序
kill -l  #列出linux所有信号
kill -9 16004  #结束PID为16004的进程（第9个信号）

# 5 网络管理命令
## 5.1 hostname
查看主机名

## 5.2 ifconfig
查看ip地址（windows里面是ipconfig）

## 5.3 netstat
显示与网络协议相关的统计数据
netstat -nltup #列出占用网络端口信息

# 6 其他命令
## 6.1 clear
clear 或者 ctrl+l  #清屏

## 6.2 重启关机命令
reboot 重启
shutdown -h now  #立即关机（断电关机）
halt  #立即关机（不断电关机）

# 7 vi编辑器 --- vim
## 7.1 基本使用
vim a.txt +10  #直接打开文件，并将光标定位到第10行
![linux7](https://github.com/killmichael/Scala.github.io/blob/main/linux7.png)

## 7.2 命令行模式
![linux8](https://github.com/killmichael/Scala.github.io/blob/main/linux8.png)

## 7.3 底行模式
![linux9](https://github.com/killmichael/Scala.github.io/blob/main/linux9.png)





