FROM redis:7.0-alpine
MAINTAINER Ruslan Dovnar <ruslan.dovnar@gmail.com>

USER app:app

VOLUME /var/www

WORKDIR /var/www/html

CMD ["redis-server", "/etc/redis/redis.conf"]
