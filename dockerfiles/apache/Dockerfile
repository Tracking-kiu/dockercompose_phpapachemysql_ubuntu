FROM phusion/baseimage:0.9.22

RUN apt-get update
RUN apt-get -y install apache2 libapache2-mod-fastcgi
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN a2enmod proxy
RUN a2enmod proxy_http
RUN a2enmod proxy_fcgi
ENTRYPOINT ["apachectl"]