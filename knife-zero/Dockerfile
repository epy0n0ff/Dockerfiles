# knife-zero Container
#
# VERSION       0.0.1

FROM alpine:3.4

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

RUN apk update && \ 
    apk add ca-certificates wget g++ make openssl-dev zlib-dev linux-headers && \
    mkdir -p /usr/local/src && \
    wget https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.1.tar.gz && \
    tar zxvf ruby-2.3.1.tar.gz && \
    cd ruby-2.3.1 && \
    ./configure && \
    make && \
    make install && \
    gem install knife-zero
