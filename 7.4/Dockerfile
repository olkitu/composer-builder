FROM composer:latest as composer

FROM php:7.4-cli

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN BUILD_PACKAGES='libpng-dev libzip-dev' \
    && apt-get update && apt-get install -y zip exiftool unzip git $BUILD_PACKAGES \
    && docker-php-ext-install -j$(nproc) gd zip exif \
    && apt-get remove -y $BUILD_PACKAGES \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app