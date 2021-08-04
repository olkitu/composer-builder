FROM composer:latest as composer


FROM php:7.4-cli-alpine

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apk add --no-cache libpng-dev libzip-dev \
    && docker-php-ext-install gd zip