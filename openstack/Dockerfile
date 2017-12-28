# OpenStack cli Container
#
# VERSION       0.2.0

FROM alpine:3.7

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

RUN apk update && \
    apk add python3 \
    ca-certificates \
    python3-dev \
    gcc \
    linux-headers \
    libc-dev \
    libffi-dev \
    openssl-dev && \
    pip3 install python-openstackclient \
    python-novaclient \
    python-cinderclient \
    python-neutronclient

ENV OS_AUTH_URL=
ENV OS_TENANT_ID=
ENV OS_TENANT_NAME=
ENV OS_USERNAME=
ENV OS_PASSWORD=
