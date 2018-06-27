hive image
====

### 安装的程序
hive.1.2.2

### 创建镜像
docker run -itd -p 22:22  --name hive --hostname hive ninecrow/centos6-hive -d

### 进入镜像
docker exec -it hive /bin/bash -l

### 日志
/tmp/{user}/hive.log

### 启动hiveserver2
$HIVE/bin/hiveserver2 & 

### beeline链接hiveserver2
$HIVE/bin/beeline <br/> 
beeline> !connect jdbc:hive2://localhost:10000 <br/>
Connecting to jdbc:hive2://localhost:10000 <br/>
Enter username for jdbc:hive2://localhost:10000: hadoop <br/>
Enter password for jdbc:hive2://localhost:10000: hadoop  (用户名，密码是配置在 $HADOOP/etc/hadoop/core-site.xml 的hadoop.proxyuser.hadoop.hosts)<br/>


