FROM php:7.2.8-apache

RUN apt-get update && apt-get install -y zlib1g-dev

COPY php.ini /usr/local/etc/php/

RUN docker-php-ext-install mysqli
RUN docker-php-ext-install zip

RUN a2enmod rewrite 
RUN service apache2 restart 
