FROM php:7.3-fpm

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN apt-get update && apt-get install -y \
    wget \
    git \
    libzip-dev
RUN wget https://get.symfony.com/cli/installer -O - | bash
ENV PATH "/root/.symfony/bin:$PATH"
RUN docker-php-ext-install -j$(nproc) bcmath zip
WORKDIR  /var/www/app/