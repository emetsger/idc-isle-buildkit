# syntax=docker/dockerfile:experimental
FROM local/base:latest

RUN --mount=type=cache,target=/var/cache/apk \ 
    --mount=type=cache,target=/etc/cache/apk \ 
    apk-install.sh \
        composer \
        nginx \
        php7-ctype \
        php7-curl \
        php7-dom \
        php7-fileinfo \
        php7-fpm \
        php7-gd \
        php7-opcache \
        php7-pdo \
        php7-pdo_mysql \ 
        php7-pdo_pgsql \ 
        php7-mysqli \
        php7-session \
        php7-simplexml \
        php7-tokenizer \
        php7-xml \
        php7-xmlwriter \
        php7-xsl \
        php7-fileinfo \
        php7-pdo_sqlite \
        php7-ldap \
        php7-mbstring \
        php7-sqlite3 \
    && \
    cleanup.sh

COPY rootfs /

RUN mkdir /var/sqlite && chmod 777 /var/sqlite