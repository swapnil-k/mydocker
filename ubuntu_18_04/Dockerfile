FROM ubuntu:18.04
MAINTAINER Swapnil Khedekar <swapnil.xxxx25@gmail.com>
WORKDIR /root

# setting up UTF-8 encoding
ENV LC_ALL C.UTF-8
ENV LANG C.UTF-8
ENV DEBIAN_FRONTEND "noninteractive"


RUN apt-get update -qq && \
    apt-get install --fix-missing -y software-properties-common && \
    apt-get install -y apt-utils tzdata && \
    echo 'Asia/Calcutta' > /etc/timezone && \
    dpkg-reconfigure tzdata


RUN apt-get install --fix-missing -y aptitude sudo vim less telnet net-tools curl inetutils-ping
RUN apt-get update -qq
RUN apt-get install -y dnsutils

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && apt-get autoremove -y

CMD ["/bin/sh", "-c", "/usr/bin/lsb_release -a; /bin/bash"]
