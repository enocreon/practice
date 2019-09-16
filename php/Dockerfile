FROM php:fpm

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN apt-get update && apt-get install -y \
    wget \
    git
RUN wget https://get.symfony.com/cli/installer -O - | bash
ENV PATH "/root/.symfony/bin:$PATH"