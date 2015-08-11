FROM centos:7
MAINTAINER Gert Van Gool <gert@vangool.mx>

RUN yum install -y epel-release && \
    yum update -y && \
    yum clean all

RUN yum install -y figlet && \
    yum clean all 

ENTRYPOINT ["/usr/bin/figlet"]
