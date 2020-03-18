FROM sk/ubuntu:18.04
LABEL maintainer="swapnil.xxxx25@gmail.com"

WORKDIR /opt
ADD jdk-8u211-linux-x64.tar.gz /opt/
RUN ln -s /opt/jdk1.8.0_211 /opt/jdk
ENV JAVA_HOME "/opt/jdk"

ENV PATH "$PATH:/opt/jdk/bin"
WORKDIR /opt/jdk
CMD ["java", "-version"]
