# edermag/jetty-9-dev

FROM edermag/ubuntu-java-8-dev
MAINTAINER Eder Magalhaes "eder@yaw.com.br"

ENV JETTY_HOME /opt/jetty

ENV JETTY_VERSION 9.3.0.v20150612
ENV JETTY_TGZ_URL http://mirror.cc.vt.edu/pub/eclipse/jetty/$JETTY_VERSION/dist/jetty-distribution-$JETTY_VERSION.tar.gz

RUN echo $JETTY_TGZ_URL

ADD $JETTY_TGZ_URL /opt/jetty.tar.gz

RUN tar -xvf /opt/jetty.tar.gz -C /opt                   && \
    rm /opt/jetty.tar.gz                                 && \
    mv /opt/jetty-distribution-$JETTY_VERSION /opt/jetty && \
    rm -rf /opt/jetty/webapps.demo /opt/jetty/start.d/*-demo.ini

EXPOSE 8088

