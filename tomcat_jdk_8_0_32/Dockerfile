FROM sk/oraclejdk:1.8.0.211
LABEL maintainer="swapnil.xxxx25@gmail.com"
ENV DEBIAN_FRONTEND "noninteractive"

WORKDIR /opt
ADD apache-tomcat-8.0.32.tar.gz /opt/ 
RUN ln -s /opt/apache-tomcat-8.0.32 /opt/tomcat

ENV CATALINA_HOME /opt/tomcat
ENV CATALINA_BASE /opt/tomcat
ENV PATH "$PATH:/opt/tomcat/bin"

WORKDIR /opt/tomcat/logs
EXPOSE 8080
CMD ["catalina.sh", "run"]
