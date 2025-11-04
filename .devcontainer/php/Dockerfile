FROM php:8.4.14-fpm
RUN apt-get update && apt-get install -y git zip unzip \
    && docker-php-ext-install mysqli pdo pdo_mysql bcmath \
    && pecl install xdebug-3.4.7 \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
