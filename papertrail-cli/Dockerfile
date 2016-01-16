FROM alpine:3.3
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN apk add --no-cache ruby ca-certificates

RUN gem install --no-document papertrail

ENTRYPOINT ["papertrail"]
