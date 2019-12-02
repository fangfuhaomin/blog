



#查看linux版本

```shell
cat /etc/redhat-release 

CentOS Linux release 7.6.1810 (Core) 
```

#下载jDK8

https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html



#在linux上操作，默认把java文件上传到/tmp下面

```shell
tar -zxvf /tmp/jdk-8u*-linux-x64.tar.gz
mv /tmp/jdk1.8* /usr/local/jdk1.8
```

#加入环境变量

```shell
cp -a /etc/profile /etc/profile.bak
cat << EOF >> /etc/profile
export JAVA_HOME=/usr/local/jdk1.8
export CLASSPATH=.:$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar
export PATH=$JAVA_HOME/bin:$PATH
EOF
```

#环境变量激活

```
. /etc/profile
```

#验证环境变量

```shell
java -version
```

