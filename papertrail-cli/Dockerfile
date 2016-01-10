FROM alpine:3.3
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN apk add --update ruby ca-certificates && \
    rm -rf /var/cache/apk/*

RUN gem install --no-document papertrail

ENTRYPOINT ["papertrail"]
