FROM phpdockerio/php74-fpm:latest

LABEL maintainer="Anthony Lempriere"

RUN apt-get update \
    && apt-get -y install \
    apt-transport-https \
    git \
    software-properties-common \
    php7.4 \
    php7.4-bcmath \
    php7.4-curl \
    php7.4-gd \
    php7.4-imap \
    php7.4-intl \
    php7.4-mbstring \
    php7.4-pgsql \
    php7.4-mysqli \
    php7.4-soap \
    php7.4-xmlrpc \
    php7.4-xsl \
    php7.4-zip \
    php-imagick \
    && php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/local/bin --filename=composer \
    && echo \
    && apt-get autoremove -y --purge \
    && apt-get clean \

WORKDIR /var/www/html