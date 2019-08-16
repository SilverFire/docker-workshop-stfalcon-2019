FROM php:7.3-fpm

RUN pecl install xdebug-2.7.2 \
    && docker-php-ext-enable xdebug

RUN docker-php-ext-install pdo pdo_mysql
