FROM ubuntu:12.04
RUN apt-get update \
&& apt-get -y upgrade \
&& apt-get -y install \
    php5-fpm php5-curl php5-mcrypt \
    php5-gd php5-imagick php5-imap \
    php5-intl php5-mysql php5-snmp \
    php5-tidy php5-xmlrpc php5-xsl
RUN sed -i 's/;daemonize = yes/daemonize = no/' /etc/php5/fpm/php-fpm.conf
RUN sed -i 's/listen = 127.0.0.1:9000/listen = 0.0.0.0:9000/' /etc/php5/fpm/pool.d/www.conf
RUN sed -i 's/display_errors = Off/display_errors = On/;' /etc/php5/fpm/php.ini
CMD ["/usr/sbin/php5-fpm"]
EXPOSE 9000