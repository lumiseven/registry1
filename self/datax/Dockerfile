FROM ubuntu:20.04

RUN echo "deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse" > /etc/apt/sources.list && \
    echo "deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse" >> /etc/apt/sources.list
RUN apt-get update && apt-get install -y \
    wget \
    tar \
    openjdk-8-jre \
    python2.7 && \
    rm -rf /var/lib/apt/lists/*
RUN wget -q -P / https://datax-opensource.oss-cn-hangzhou.aliyuncs.com/datax.tar.gz && \
    tar -xvf datax.tar.gz && \
    rm -rf datax.tar.gz && \
    ln -s /usr/bin/python2.7 /usr/bin/python && \
    ln -s /datax/bin/datax.py /usr/bin/datax.py