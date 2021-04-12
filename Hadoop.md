# 1 启动Hadoop相关服务
cd /export/onekey/

./start-all.sh         # 一键开启

./stop-all.sh          # 一键关闭

jps                    # 查看启动进程

https://192.168.88.100:50070/  # 查看HDFS页面

![hadoop1](https://github.com/killmichael/Scala.github.io/blob/main/hadoop1.png)

# 2 HDFS架构
![hadoop2](https://github.com/killmichael/Scala.github.io/blob/main/hadoop2.png)

![hadoop3](https://github.com/killmichael/Scala.github.io/blob/main/hadoop3.png)

![hadoop4](https://github.com/killmichael/Scala.github.io/blob/main/hadoop4.png)

![hadoop5](https://github.com/killmichael/Scala.github.io/blob/main/hadoop5.png)

![hadoop6](https://github.com/killmichael/Scala.github.io/blob/main/hadoop6.png)

# 3 HDFS的Shell命令
hadoop fs <args>       # 既可操作HDFS，又可以操作本地系统
 
hdfs dfs <args>        # 只能操作HDFS系统
  
## ls
hadoop fs -ls /        # 显示文件列表

hadoop fs -ls -R /     # 递归显示文件列表（把子目录、子子目录等都显示）
## mkdir
hadoop fs -mkdir /dir1        # 在/上创建dir1目录

hadoop fs -mkdir -p /aaa/bbb/ccc # 创建多级文件夹
## put
hadoop fs -put /root/1.txt /dir1 # 将文件1.txt上传到HDFS的dir1目录下

hadoop fs -put /root/dir2 /dir1 # 将目录dir2上传到HDFS的dir1目录下（包含目录下的所有文件）
## get
hadoop fs -get /initial-setup-ks.cfg /opt  #将HDFS中的文件下载到本地opt目录
## mv
hadoop fs -mv /dir1/1.txt /dir2    # 文件复制（只能在HDFS目录之间复制，不能跨文件系统）
## rm
hadoop fs -rm /dir1/1.txt          # 删除文件，文件暂时存放在回收站里；若要恢复，用mv命令复制

hadoop fs -rm -r /dir2             # 删除目录，暂存于回收站

hadoop fs -rm -skipTrash /dir1/1.txt # 删除文件，跳过回收站直接删除
## cp
hadoop fs -mv /dir1/1.txt /dir2    # 文件复制（只能在HDFS目录之间复制，不能跨文件系统）

## Linux下mv和cp命令的区别：

1、功能上的区别

mv: 用户可以使用该命令为文件或目录重命名或将文件由一个目录移入另一个目录中；

cp: 该命令的功能是将给出的文件或目录拷贝到另一文件或目录中。 

2、从inode角度来区分

mv: 会将存储于indoe索引节点上的文件元信息也移动到新文件中；

cp: 只会复制文件数据，不会复制inode索引节点上的文件元信息。
## cat
hadoop fs -cat /dir1/1.txt     # 查看HDFS中文件的内容

# 4 HDFS的基准测试
![hadoop7](https://github.com/killmichael/Scala.github.io/blob/main/hadoop7.png)











