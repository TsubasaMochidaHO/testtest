FROM php:7.2-apache
COPY php.ini /usr/local/etc/php/
RUN apt-get update && apt-get -y install \
  sudo \
  libmcrypt-dev \
  libmemcached-dev \
  libpng-dev \
  libicu-dev \
  wget \
  curl
RUN \
  docker-php-ext-install gd mbstring mysqli pcntl pdo_mysql zip intl
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

