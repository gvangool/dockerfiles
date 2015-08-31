FROM centos:7
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN yum install -y epel-release && \
    yum update -y && \
    yum clean all

RUN yum install -y ruby && \
    yum clean all 
RUN gem install --no-document papertrail

ENTRYPOINT ["papertrail"]
