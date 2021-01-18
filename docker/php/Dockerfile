FROM php:8.0-cli

RUN pecl install xdebug-3.0.2 \
  && docker-php-ext-enable xdebug

COPY xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

EXPOSE 8000

WORKDIR /var/www/html/

CMD ["php", "-S0.0.0.0:8000", "-t/var/www/html/public/"]
