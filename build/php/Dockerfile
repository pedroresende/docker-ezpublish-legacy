FROM debian:jessie
RUN apt-get update && apt-get install -y php5 php5-cli php5-gd php5-fpm php5-mysql \
    curl php5-intl php5-curl php5-xsl php5-imagick imagemagick imagemagick-common \
    openjdk-7-jre

ADD conf/www.conf /etc/php5/fpm/pool.d/www.conf
ADD conf/php-fpm.conf /etc/php5/fpm/php-fpm.conf
ADD conf/memory.ini /etc/php5/fpm/conf.d/memory.ini

WORKDIR /var/www/html/ezpublish

EXPOSE 9000

CMD ["php5-fpm"]
