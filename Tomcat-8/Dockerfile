FROM edermag/ubuntu-java-8-dev
MAINTAINER Eder Magalhaes "eder@yaw.com.br"

ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH

ENV TOMCAT_MAJOR 8
ENV TOMCAT_VERSION 8.0.23
ENV TOMCAT_TGZ_URL https://www.apache.org/dist/tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz

ADD $TOMCAT_TGZ_URL /opt/apache-tomcat.tar.gz

RUN tar -xvf /opt/apache-tomcat.tar.gz -C /opt   && \
  mv /opt/apache-tomcat-$TOMCAT_VERSION "$CATALINA_HOME" && \
  rm /opt/apache-tomcat.tar.gz

EXPOSE 8080

