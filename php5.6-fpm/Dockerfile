FROM php:5.6-fpm
RUN apt update && apt install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd\
    && docker-php-ext-install  mysqli
   
EXPOSE 9000
