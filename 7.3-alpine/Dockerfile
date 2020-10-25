FROM php:7.3-fpm-alpine

COPY ./bin/docker-php-ext-get /usr/local/bin/

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

RUN apk add --no-cache openssl-dev libstdc++ supervisor git &&\
    docker-php-source extract &&\
    docker-php-ext-get igbinary &&\
    docker-php-ext-install pdo_mysql igbinary &&\
    docker-php-ext-get redis &&\
    docker-php-ext-configure redis --enable-redis-igbinary &&\
    docker-php-ext-get swoole &&\
    docker-php-ext-configure swoole --enable-openssl=yes &&\
    docker-php-ext-install redis swoole &&\
    docker-php-source delete
