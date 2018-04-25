FROM php:7.2-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd pdo_mysql mysqli \
    && pecl install redis-4.0.1 \
    && pecl install xdebug-2.6.0 \
    && pecl install yaf-3.0.7

COPY ["./extensions/yaf.ini","extensions/redis.ini","extensions/xdebug.ini","/usr/local/etc/php/conf.d/"]
