FROM php:8.2-fpm-alpine

COPY php.ini-production /usr/local/etc/php/php.ini
COPY www.conf           /usr/local/etc/php-fpm.d/www.conf

# extensions
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-enable mysqli pdo_mysql

ARG user=www-data
ARG group=www-data
ARG uid=1000
ARG gid=1000
ARG appdir=/app

#RUN pecl install xdebug && docker-php-ext-enable xdebug
#RUN echo "export UMASK=${UMASK:-002}" > /etc/profile.d/umask.sh && chmod +x /etc/profile.d/umask.sh

RUN set -x && deluser www-data && addgroup -g $gid www-data
RUN adduser -S $user -G $group --uid $uid

VOLUME $appdir
COPY app $appdir
RUN chown -R $user:$group $appdir

USER www-data
WORKDIR $appdir


