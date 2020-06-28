FROM php:8.0-rc-fpm-alpine
RUN apk update \
  && apk add libzip-dev mariadb-client
#  && docker-php-ext-install zip pdo_mysql mbstring bcmath ctype fileinfo json openssl pdo tokenizer xml
WORKDIR /var/www
