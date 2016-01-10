# Simple container with PHP and (latest) phpunit.
# Remember it's a very minimal PHP installation, so it's possible you need to
# add extra packages (eg php-phar).
#
# Usage:
#
#   docker run --rm -v $(pwd):/app --workdir /app gvangool/php $@
#   docker run --rm -v $(pwd):/app --workdir /app --entrypoint phpunit.phar gvangool/php $@
FROM alpine:3.3
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN apk add --update php php-phar ca-certificates wget && \
    rm -rf /var/cache/apk/*
RUN wget -O /bin/phpunit.phar https://phar.phpunit.de/phpunit.phar && \
    chmod +x /bin/phpunit.phar

CMD ["php"]
