FROM php:7.2.2-fpm

LABEL maintainer="Anthony Lempriere"

RUN apt-get update && apt-get upgrade -y \
    g++ \
    openssl \
    git \
    unzip \
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