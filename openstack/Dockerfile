# OpenStack cli Container
#
# VERSION       0.1.0

FROM alpine:3.4

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

RUN apk update && \
    apk add py-pip \
    ca-certificates \ 
    python-dev \
    gcc \
    linux-headers \
    libc-dev && \
    pip install --upgrade pip && \
    pip install python-openstackclient \
    python-novaclient \
    python-neutronclient

ENV OS_AUTH_URL=
ENV OS_TENANT_ID=
ENV OS_TENANT_NAME=
ENV OS_USERNAME=
ENV OS_PASSWORD=
