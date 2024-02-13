FROM nginx:1.25.3

ARG PROJ_DOMAIN
ARG appdir=/app

ENV NGINX_ENVSUBST_TEMPLATE_SUFFIX=.nginx
ENV PROJ_DOMAIN=${PROJ_DOMAIN}
ENV LARA_PUBLIC=/app/public
ENV WP_DIR=/app/public/blog

COPY ssl        /etc/nginx/ssl
COPY nginx.conf /etc/nginx/nginx.conf
COPY templates  /etc/nginx/templates

VOLUME $appdir
VOLUME $appdir/public/blog
VOLUME /etc/nginx/ssl