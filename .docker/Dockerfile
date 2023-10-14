FROM php:8.2-alpine

RUN apk add --no-cache $PHPIZE_DEPS \
    && apk add --update linux-headers \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
    && apk add nginx

COPY --from=composer/composer:latest-bin /composer /usr/bin/composer
