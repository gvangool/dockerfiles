# Usage:
#
#   $ docker run --rm --net=host gvangool/nmap 192.168.15.1
#
#   Starting Nmap 6.47 ( http://nmap.org ) at 2015-11-02 23:17 UTC
#   Nmap scan report for 192.168.15.1
#   Host is up (0.018s latency).
#   Not shown: 995 closed ports
#   PORT    STATE SERVICE
#   22/tcp  open  ssh
#   53/tcp  open  domain
#   80/tcp  open  http
#   443/tcp open  https
#   843/tcp open  unknown
#
#   Nmap done: 1 IP address (1 host up) scanned in 1.87 seconds
#
FROM alpine:3.3
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN apk add --no-cache nmap

ENTRYPOINT ["nmap"]
