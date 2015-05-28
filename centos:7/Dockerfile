
FROM centos7:latest

MAINTAINER YT "<tao.yang@shuyun.com>" 

ADD Centos-7.repo CentOS-Base.repo

ENV TIMEZONE Asia/Shanghai
RUN echo ZONE="$TIMEZONE"> /etc/sysconfig/clock && \ 
    cp "/usr/share/zoneinfo/$TIMEZONE" /etc/localtime


ENV LANG zh_CN.UTF-8
RUN localedef -v -c -i zh_CN -f UTF-8 zh_CN.UTF-8 || true
