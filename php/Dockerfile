FROM alpine:3.2
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN apk add --update php php-phar ca-certificates wget && \
    rm -rf /var/cache/apk/*
RUN wget -O /bin/phpunit.phar https://phar.phpunit.de/phpunit.phar && \
    chmod +x /bin/phpunit.phar

CMD ["php"]
