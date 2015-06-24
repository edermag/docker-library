FROM ubuntu:14.04
MAINTAINER Eder Magalhaes "eder@yaw.com.br"

# Install java-8 from Oracle
RUN apt-get update -y                           && \
  apt-get install software-properties-common -y && \
  add-apt-repository ppa:webupd8team/java -y    && \
  apt-get update -y                             && \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  apt-get install oracle-java8-installer -y     && \
  rm -rf /var/lib/apt/lists/*                   && \
  rm -rf /var/cache/oracle-jdk8-installer

# Define JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

ADD http://archive.apache.org/dist/maven/maven-3/3.3.3/binaries/apache-maven-3.3.3-bin.tar.gz /opt/maven.tar.gz

# Install Maven 3.3.3
RUN tar -xvf /opt/maven.tar.gz -C /opt   && \
  mv /opt/apache-maven-3.3.3 /opt/maven && \
  ln -s /opt/maven/bin/mvn /usr/bin/mvn       && \
  rm /opt/maven.tar.gz

# Define MAVEN_HOME variable
ENV MAVEN_HOME /opt/maven

