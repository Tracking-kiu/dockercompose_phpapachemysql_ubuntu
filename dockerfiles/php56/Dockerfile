FROM phusion/baseimage:0.9.22
RUN add-apt-repository ppa:ondrej/php
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 4F4EA0AAE5267A6C
RUN apt-get update
RUN mkdir /run/php
RUN apt-get -y install php5.6-fpm
RUN sed  -i.backup "s#listen = /run/php/php5\.6-fpm\.sock#listen = 9000#" /etc/php/5.6/fpm/pool.d/www.conf

RUN apt-get -y install php5.6-mysql
ENTRYPOINT ["php-fpm5.6", "--nodaemonize", "--fpm-config", "/etc/php/5.6/fpm/php-fpm.conf"]