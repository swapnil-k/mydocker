FROM sk/ubuntu:18.04
MAINTAINER Swapnil Khedekar <swapnil.xxxx25@gmail.com>

ADD  https://download.java.net/java/GA/jdk12/33/GPL/openjdk-12_linux-x64_bin.tar.gz /opt/
RUN tar -zxvf /opt/openjdk-12_linux-x64_bin.tar.gz -C /opt/
RUN ln -s /opt/jdk-12 /opt/jdk

ENV JAVA_HOME "/opt/jdk"
ENV PATH "$PATH:/opt/jdk/bin"
WORKDIR /opt/jdk
CMD ["java", "-version"]
