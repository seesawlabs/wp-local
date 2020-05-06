FROM php:7.2-fpm-alpine

RUN set -ex; \
  apk add --no-cache --virtual .build-deps \
  libjpeg-turbo-dev \
  libpng-dev; \
  docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; \
  docker-php-ext-install gd mysqli opcache zip; 

CMD ["php-fpm"]

EXPOSE 9000