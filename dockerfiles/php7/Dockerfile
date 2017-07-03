FROM phusion/baseimage:0.9.22

RUN apt-get update
RUN apt-get -y install php-fpm
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN sed  -i.backup "s#listen = /run/php/php7\.0-fpm\.sock#listen = 9000#" /etc/php/7.0/fpm/pool.d/www.conf
RUN mkdir /run/php
ENTRYPOINT ["php-fpm7.0", "--nodaemonize", "--fpm-config", "/etc/php/7.0/fpm/php-fpm.conf"]
