FROM php:8.4.10-fpm
RUN docker-php-ext-install mysqli pdo pdo_mysql bcmath \
    && pecl install xdebug-3.4.5 \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
