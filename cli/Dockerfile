# docker/php/Dockerfile
FROM php:8.1-cli

RUN apt-get update
RUN apt-get install -y autoconf pkg-config openssl zip unzip git curl exiftool
RUN apt-get install -y libzip-dev libonig-dev libicu-dev libxml2-dev libssl-dev libpng-dev

RUN docker-php-ext-install bcmath mbstring intl opcache xml gd zip exif
RUN docker-php-ext-install pdo pdo_mysql mysqli

RUN sed -i -e "s/short_open_tag = On/short_open_tag = Off/g" /usr/local/etc/php/php.ini-development
RUN sed -i -e "s/short_open_tag = On/short_open_tag = Off/g" /usr/local/etc/php/php.ini-production

RUN cp /usr/local/etc/php/php.ini-development /usr/local/etc/php/php.ini

USER 1000:1000

ENTRYPOINT [ "php", "artisan" ]

