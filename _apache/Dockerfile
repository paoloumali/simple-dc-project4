FROM httpd:2.4.58

ARG proj_domain

ENV PROJ_DOMAIN=$proj_domain
ENV LARA_PUBLIC=/app/public
ENV WP_DIR=/app/public/blog

COPY httpd.conf         /usr/local/apache2/conf/httpd.conf
COPY httpd-vhosts.conf  /usr/local/apache2/conf/extra/httpd-vhosts.conf

ARG appdir=/app

VOLUME $appdir
VOLUME $appdir/public/blog