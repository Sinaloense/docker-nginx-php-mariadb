FROM php:8.3.17-fpm-alpine
ENV TZ="UTC"
RUN apk update && apk add --no-cache build-base php83-dev linux-headers tzdata \
    && cp /usr/share/zoneinfo/$TZ /etc/localtime \
    && docker-php-ext-install mysqli pdo pdo_mysql bcmath \
    && pecl install xdebug-3.4.2 \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
