# MAINTAINER        qingbo.liu<260831882@qq.com>
# DOCKER-VERSION    17.06.2-ce

FROM          jdk:latest
MAINTAINER   qingbo.liu<260831882@qq.com>

ADD ./apache-tomcat-7.0.55.tar.gz /home/tomcat/
COPY ./server.xml /home/tomcat/apache-tomcat-7.0.55/conf/server.xml

ENV TOMCAT_VERSION 7.0.55

ENV JAVA_HOME /home/jdk/jdk1.7.0_80
ENV CATALINA_HOME /home/tomcat/apache-tomcat-7.0.55
ENV CATALINA_BASE /home/tomcat/apache-tomcat-7.0.55

ENV CLASSPATH $JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/lib:$CATALINA_HOME/bin
ENV APP_DIR ${CATALINA_HOME}/webapps/

EXPOSE 8080

ENTRYPOINT /home/tomcat/apache-tomcat-7.0.55/bin/catalina.sh run