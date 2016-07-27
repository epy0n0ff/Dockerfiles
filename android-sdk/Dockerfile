# Android SDK Container
#
# VERSION       0.0.1

FROM ubuntu:15.10

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

ENV SDK_ARCHIVE android-sdk_r24.4.1-linux.tgz
ENV ANDROID_HOME /opt/android-sdk-linux
ENV PATH ${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools

RUN apt-get install -y software-properties-common && \
    echo -e '\n' | add-apt-repository ppa:webupd8team/java && \
    apt-get update && apt-get -y install openjdk-8-jdk wget git && \
    wget http://dl.google.com/android/${SDK_ARCHIVE} && \
    tar zxvf ${SDK_ARCHIVE} -C /opt > /dev/null && \
    rm ${SDK_ARCHIVE} && \
    rm -rf /etc/ssl/certs/java/cacerts && \
    /var/lib/dpkg/info/ca-certificates-java.postinst configure && \
    rm -rf /var/lib/apt/lists/*
