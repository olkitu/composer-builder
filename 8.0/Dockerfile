FROM composer:latest as composer

FROM php:8.0-cli

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apk add --no-cache libpng-dev libzip-dev \
    docker-php-ext-install gd zip