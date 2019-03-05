FROM php:7.2.2-fpm

LABEL maintainer="Anthony Lempriere"

RUN apt-get update && apt-get upgrade -y \
    g++ \
    openssl \
    git \
    unzip \
    &&  apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev && \
           docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ && \
           docker-php-ext-install gd \
    && docker-php-ext-install \
        bcmath \
    && docker-php-ext-install pdo pdo_mysql\
    mbstring \
    mysqli \
    && php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/local/bin --filename=composer \
    && echo \
    && apt-get autoremove -y --purge \
    && apt-get clean \

WORKDIR /var/www/html

