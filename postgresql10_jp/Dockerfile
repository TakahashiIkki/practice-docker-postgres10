FROM postgres:10.0

MAINTAINER i-takahashi

RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LANG ja_JP.utf8

COPY initdb/*.* /docker-entrypoint-initdb.d/

