FROM docker.io/ubuntu:14.04.2

MAINTAINER YT "<tao.yang@shuyun.com>"

ADD sources.list /etc/apt/sources.list

ENV LANG C.UTF-8

RUN echo "Asia/Shanghai" > /etc/timezone && \
        dpkg-reconfigure -f noninteractive tzdata

RUN apt-get update; apt-get upgrade -y; apt-get install locales

RUN export LANGUAGE=C.UTF-8; export LANG=C.UTF-8; export LC_ALL=C.UTF-8; locale-gen C.UTF-8; DEBIAN_FRONTEND=noninteractive dpkg-reconfigure locales



