FROM php:8.5.2-fpm
RUN apt-get update && apt-get install -y wget git zip unzip jpegoptim optipng pngquant gifsicle libavif-bin ghostscript \
    && curl -fsSL -o /usr/local/bin/install-php-extensions https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions \
    && chmod +x /usr/local/bin/install-php-extensions \
    && install-php-extensions mysqli pdo pdo_mysql bcmath exif gd imagick xdebug \
    && curl -fsSL https://deb.nodesource.com/setup_24.x | bash - \
    && apt-get install -y nodejs && npm install -g svgo \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
    && rm -rf /var/lib/apt/lists/*
