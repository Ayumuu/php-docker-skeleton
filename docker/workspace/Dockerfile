FROM php:8.0-rc-fpm-alpine
RUN apk update \
  && apk add libzip-dev mariadb-client
#  && docker-php-ext-install zip pdo_mysql mbstring bcmath openssl pdo tokenizer xml
#  && docker-php-ext-install zip pdo_mysql mbstring bcmath ctype fileinfo json openssl pdo tokenizer xml

RUN php -r "readfile('https://getcomposer.org/installer');" > composer-setup.php \
&& php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" \
&& php ./composer-setup.php \
&& mv ./composer.phar /usr/local/bin/composer

WORKDIR /var/www

