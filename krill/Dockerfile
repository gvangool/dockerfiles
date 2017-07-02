FROM alpine:3.6
LABEL maintainer="Gert Van Gool <gert@vangool.mx>"

RUN apk add --no-cache python2 py2-pip ca-certificates

RUN pip install krill==0.3.0

ENTRYPOINT ["/usr/bin/krill"]
CMD ["-s", "https://twitter.com/nasa"]
