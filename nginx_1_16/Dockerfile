FROM sk/ubuntu:18.04
MAINTAINER Swapnil Khedekar <swapnil.xxxx25@gmail.com>

RUN add-apt-repository -y ppa:nginx/stable
RUN apt-get update -qq
RUN apt-get install -y nginx
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && apt-get autoremove -y

RUN ln -s /etc/nginx /opt/nginx
RUN ln -sf /dev/stdout /var/log/nginx/access.log 
RUN ls -sf /dev/stderr /var/log/nginx/error.log

WORKDIR /opt/nginx

RUN mv sites-available/default conf.d/default.conf
RUN rm -rf sites-enabled sites-available
RUN sed -i 's/^user/\#user/g' nginx.conf
RUN sed -i 's/include\ \/etc\/nginx\/sites-enabled\/\*\;$/\#include\ \/etc\/nginx\/sites-enabled\/\*\;/g;' /etc/nginx/nginx.conf

STOPSIGNAL SIGTERM
EXPOSE 80

RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ls -sf /dev/stderr /var/log/nginx/error.log

#CMD ["nginx", "-g", "daemon off;"]
CMD ["/bin/sh", "-c", "/usr/sbin/nginx -V; /usr/sbin/nginx -g 'daemon off;'"]
