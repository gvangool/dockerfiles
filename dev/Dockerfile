FROM centos:7
LABEL maintainer="Gert Van Gool <gert@vangool.mx>"

RUN yum install -y epel-release && \
    yum update -y && \
    yum clean all

RUN yum install -y zsh git vim && \
    yum install -y bind-utils mtr whois && \
    yum clean all

RUN mkdir ~/src && \
    cd ~/src && \
    git clone https://github.com/gvangool/dotfiles.git && \
    mv dotfiles/.git ~/ && \
    cd ~ && \
    rm -rf ~/src && \
    git reset --hard && \
    git submodule update --init --recursive

WORKDIR /root
ENTRYPOINT ["/usr/bin/zsh"]
