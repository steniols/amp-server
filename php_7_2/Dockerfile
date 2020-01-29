FROM php:7.2-apache

RUN apt-get update -y && apt-get install -y libpng-dev curl libcurl4-openssl-dev
RUN docker-php-ext-install mysqli gd curl pdo pdo_mysql exif gettext zip
RUN docker-php-ext-enable mysqli

# Instalação NODE 10 + NPM
RUN curl -sL https://deb.nodesource.com/setup_4.x | bash
RUN apt-get install nodejs -y
RUN a2enmod rewrite
RUN service apache2 restart

#Instalação YARN
RUN npm install -g yarn

RUN node -v
RUN npm -v
RUN yarn --version
