FROM ubuntu:18.04
MAINTAINER Swapnil Khedekar <swapnil.xxxx25@gmail.com>
WORKDIR /root

# setting up UTF-8 encoding
ENV LC_ALL C.UTF-8
ENV LANG C.UTF-8
ENV DEBIAN_FRONTEND "noninteractive"
ENV TZ "Asia/Calcutta"

RUN apt-get update -qq && \
    apt-get install --fix-missing -y software-properties-common && \
    apt-get install -y apt-utils tzdata 

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN dpkg-reconfigure tzdata

RUN apt-get install --fix-missing -y aptitude sudo vim less telnet net-tools curl inetutils-ping
RUN apt-get update -qq
RUN apt-get install -y dnsutils
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && apt-get autoremove -y

RUN ln -sf /dev/stdout /var/log/dpkg.log
RUN ls -sf /dev/stderr /var/log/bootstrap.log

CMD ["/bin/sh", "-c", "/usr/bin/lsb_release -a; /bin/bash"]
