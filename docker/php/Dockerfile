FROM php:7.4-fpm

RUN apt-get update

# common
RUN apt-get install -y apt-utils libssl-dev libzip-dev libonig-dev
RUN docker-php-ext-install iconv mbstring zip bcmath

# GD
RUN apt-get install -y libpng-dev
RUN apt-get install -y libjpeg-dev
RUN docker-php-ext-configure gd --with-jpeg
RUN docker-php-ext-install gd

# cURL
#RUN apt-get install -y libcurl3-dev
#RUN docker-php-ext-install curl

# MySQL
RUN docker-php-ext-install mysqli pdo_mysql

