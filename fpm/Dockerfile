FROM php:8.1-fpm

RUN apt-get update
RUN apt-get install -y autoconf pkg-config openssl zip unzip git curl exiftool
RUN apt-get install -y libzip-dev libonig-dev libicu-dev libxml2-dev libssl-dev libpng-dev

RUN docker-php-ext-install bcmath mbstring intl opcache xml gd zip exif
RUN docker-php-ext-install pdo pdo_mysql mysqli

USER 1000