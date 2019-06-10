FROM php:5.6-apache

RUN apt-get update -y && apt-get install -y libpng-dev curl libcurl4-openssl-dev
RUN docker-php-ext-install mysqli curl exif gettext zip

RUN a2enmod rewrite
RUN service apache2 restart

RUN apt-get install -y libwebp-dev libjpeg62-turbo-dev libpng-dev libxpm-dev libfreetype6-dev
RUN docker-php-ext-configure gd --with-gd --with-webp-dir --with-jpeg-dir --with-png-dir --with-zlib-dir --with-xpm-dir --with-freetype-dir --enable-gd-native-ttf
RUN docker-php-ext-install gd

RUN a2enmod rewrite
RUN service apache2 restart