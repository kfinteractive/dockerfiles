FROM nginx:latest

MAINTAINER KFI pw@kf-interactive.com

RUN apt-get update && apt-get install -y  curl imagemagick  mysql-client supervisor openssl ca-certificates php5-fpm php5-cli php5-curl php5-mcrypt php5-gd php5-common php5-mysql php5-xmlrpc php5-xsl php5-dev




RUN groupadd --gid 1000 web
RUN useradd --gid 1000 --uid 1000 web

ADD supervisord.conf /etc/supervisord.conf
ADD nginx.conf /etc/nginx/nginx.conf
RUN rm /etc/init.d/nginx /etc/init.d/php5-fpm /etc/init.d/supervisor


#CMD ["/usr/bin/supervisord", "-n"]
CMD ["/usr/sbin/nginx"]
