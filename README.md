# linux-jdk
linux下jdk的安装

(yum -y list java)

(注1： yum install java-1.8.0-openjdk.x86_64)
（注2：yum -y install java-1.8.0-openjdk*）
（注：cd /usr/lib/jvm）


jre-1.8.0-openjdk-1.8.0.181-3.b13.el7_5.x86_64

[root@localhost bin]# vi /etc/profile
在文件最后加入：
#set java environment
JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk-1.8.0.181-3.b13.el7_5.x86_64
PATH=$PATH:$JAVA_HOME/bin
CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
export JAVA_HOME CLASSPATH PATH
修改/etc/profile之后让其生效
[root@localhost alternatives]# . /etc/profile
