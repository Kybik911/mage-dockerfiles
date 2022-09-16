FROM redis:7.0
MAINTAINER Ruslan Dovnar <ruslan.dovnar@gmail.com>

RUN apt-get update \
	&& apt-get install -y sudo \
    && rm -rf /var/lib/apt/lists/*

RUN groupadd -g 1000 app \
 && useradd -g 1000 -u 1000 -d /var/www -s /bin/bash app

COPY redis.conf /usr/local/etc/redis/redis.conf

USER app:app

VOLUME /var/www

WORKDIR /var/www/html

CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]
