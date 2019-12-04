1.编辑 /etc/profile
vim /etc/profile
在文本最下面添加
#set java environment
export JAVA_HOME=/usr/singbon/jdk/jdk1.7.0_80
export JRE_HOME=/usr/singbon/jdk/jdk1.7.0_80/jre
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib:$CLASSPATH
export PATH=$JAVA_HOME/bin:$PATH
##########first tomcat###########
CATALINA_BASE=/usr/singbon/tomcat/apache-tomcat-7.0.78-80
CATALINA_HOME=/usr/singbon/tomcat/apache-tomcat-7.0.78-80
TOMCAT_HOME=/usr/singbon/tomcat/apache-tomcat-7.0.78-80
export CATALINA_BASE CATALINA_HOME TOMCAT_HOME
##########second tomcat##########
CATALINA_2_BASE=/usr/singbon/tomcat/apache-tomcat-7.0.78-81
CATALINA_2_HOME=/usr/singbon/tomcat/apache-tomcat-7.0.78-81
TOMCAT_2_HOME=/usr/singbon/tomcat/apache-tomcat-7.0.78-81
export CATALINA_2_BASE CATALINA_2_HOME TOMCAT_2_HOME
##########second tomcat##########
2.编辑tomcat catalina.sh
第一个tomcat：
JAVA_OPTS="-Djava.security.egd=file:/dev/./urandom -server -Xms4096m -Xmx4096m -Xss2048K -XX:PermSize=2048m -XX:MaxPermSize=3072m -Dfile.encoding=UTF-8"
export JAVA_HOME=/usr/singbon/soft/java/jdk1.7.0_80
export JRE_HOME=/usr/singbon/soft/java/jdk1.7.0_80/jre
第二个tomcat：
JAVA_OPTS="-Djava.security.egd=file:/dev/./urandom -server -Xms4096m -Xmx4096m -Xss2048K -XX:PermSize=2048m -XX:MaxPermSize=3072m -Dfile.encoding=UTF-8"
export JAVA_HOME=/usr/singbon/soft/java/jdk1.7.0_80
export JRE_HOME=/usr/singbon/soft/java/jdk1.7.0_80/jre
export CATALINA_BASE=$CATALINA_2_BASE
export CATALINA_HOME=$CATALINA_2_HOME
3.编辑两个server.xml
已在项目中 t80 t81