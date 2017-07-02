FROM centos:7
LABEL maintainer="Gert Van Gool <gert@vangool.mx>"

RUN yum install -y epel-release && \
    yum update -y && \
    yum clean all

RUN yum install -y python{,-setuptools} && \
    yum clean all && \
    easy_install pip

RUN pip install krill==0.3.0

ENTRYPOINT ["/usr/bin/krill"]
CMD ["-s", "https://twitter.com/nasa"]
