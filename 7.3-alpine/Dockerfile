FROM php:7.3-fpm-alpine

COPY ./bin/docker-php-ext-get /usr/local/bin/

RUN apk add --no-cache openssl-dev libstdc++ supervisor composer &&\
    docker-php-source extract &&\
    docker-php-ext-get igbinary 3.1.2 &&\
    docker-php-ext-install pdo_mysql igbinary &&\
    docker-php-ext-get redis 5.2.2 &&\
    docker-php-ext-configure redis --enable-redis-igbinary &&\
    docker-php-ext-get swoole 4.5.2 &&\
    docker-php-ext-configure swoole --enable-openssl=yes &&\
    docker-php-ext-install redis swoole &&\
    docker-php-source delete
