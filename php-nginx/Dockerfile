FROM nginx:latest

MAINTAINER KFI pw@kf-interactive.com

RUN apt-get update && apt-get install -y  curl imagemagick  mysql-client supervisor openssl ca-certificates php5-fpm php5-cli php5-curl php5-mcrypt php5-gd php5-common php5-mysql php5-xmlrpc php5-xsl php5-dev

RUN groupadd --gid 1000 web
RUN useradd --gid 1000 --uid 1000 web

ADD config/etc/rc.local /etc/rc.local

ADD config/etc/nginx/nginx.conf /etc/nginx/nginx.conf
ADD config/etc/supervisord.conf /etc/supervisord.conf
ADD config/etc/nginx/nginx.conf /etc/nginx/nginx.conf
ADD config/etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf
ADD config/etc/php5/fpm/php-fpm.conf /etc/php5/fpm/php-fpm.conf
ADD config/etc/php5/fpm/pool.d/www.conf /etc/php5/fpm/pool.d/www.conf

ADD src/index.php /usr/share/nginx/html/index.php


RUN rm /etc/init.d/nginx /etc/init.d/php5-fpm /etc/init.d/supervisor


CMD ["/usr/bin/supervisord", "-n", "-c", "/etc/supervisord.conf" ]
