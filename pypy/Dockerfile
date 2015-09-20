FROM centos:7
MAINTAINER "Gert Van Gool <gert@vangool.mx>"

RUN yum update -y && \
    yum install -y epel-release && \
    yum clean all
RUN yum install -y bzip2 tar wget && \
    yum clean all
RUN wget https://bitbucket.org/squeaky/portable-pypy/downloads/pypy-2.6.1-linux_x86_64-portable.tar.bz2 && \
    tar --overwrite --no-overwrite-dir --directory=/usr/local --strip-components=1 -xjf pypy-2.6.1-linux_x86_64-portable.tar.bz2 && \
    rm -f  pypy-2.6.1-linux_x86_64-portable.tar.bz2
RUN wget https://bootstrap.pypa.io/get-pip.py && \
    pypy get-pip.py && \
    rm -f get-pip.py
