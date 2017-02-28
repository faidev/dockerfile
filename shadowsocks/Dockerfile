FROM centos:latest

MAINTAINER Faidev <25056592@qq.com>

RUN yum install -y m2crypto openssl-devel python-setuptools && \
yum clean all && \
easy_install pip && \
pip install shadowsocks && \
rm -rf ~/.cache/

ENV SS_ADDR 0.0.0.0
ENV SS_PORT 8388
ENV SS_PASSWORD 369qweASD.
ENV SS_METHOD aes-256-cfb
ENV SS_TIMEOUT 60

EXPOSE $SS_PORT $SS_PORT/udp

CMD ssserver -s $SS_ADDR \
-p $SS_PORT \
-k $SS_PASSWORD \
-m $SS_METHOD \
-t $SS_TIMEOUT
