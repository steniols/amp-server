FROM php:7.2-apache

RUN apt-get update -y && apt-get install -y libpng-dev curl libcurl4-openssl-dev
RUN docker-php-ext-install mysqli gd curl pdo pdo_mysql exif gettext zip

RUN docker-php-ext-configure gd --with-gd --with-webp-dir --with-jpeg-dir --with-png-dir --with-zlib-dir --with-xpm-dir --with-freetype-dir --enable-gd-native-ttf
RUN docker-php-ext-install gd

RUN apt-get install -y libxml2-dev --no-install-recommends

RUN a2enmod rewrite
RUN service apache2 restart
