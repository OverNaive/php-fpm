# php-fpm

## 如何使用

`Dockerfile` 只是个例子，可以修改安装所需要的软件和扩展，然后重新构建出特定的镜像

使用案例：[OverNaive/docker-nginx-php](https://github.com/OverNaive/docker-nginx-php)

## 关于 `docker-php-ext-get`

`docker-php-ext-get` 来自于文章： [Build Docker images with PECL packages without using the PECL command](https://olvlvl.com/2019-06-docker-pecl-without-pecl)

## 安装的软件

`openssl-dev`

`libstdc++`

`supervisor`

`git`

`composer`

## 安装的扩展

`pdo_mysql`

`igbinary 3.1.2`

`redis 5.2.2 --enable-redis-igbinary`

`swoole 4.5.2 --enable-openssl=yes`

## 镜像地址

[overnaive/php-fpm](https://hub.docker.com/r/overnaive/php-fpm)

## 源码地址

[OverNaive/php-fpm](https://github.com/OverNaive/php-fpm)