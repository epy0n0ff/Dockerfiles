# golang
#
# VERSION	0.0.1
FROM centos
MAINTAINER epy0n.0ff <epy0n.0ff@mail.com>

RUN yum -y install tar
RUN cd /tmp

RUN curl -O -L https://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN rpm -ivh epel-release-6-8.noarch.rpm

RUN curl -O -L http://golang.org/dl/go1.3.linux-amd64.tar.gz
RUN tar -C /opt -xzf go1.3.linux-amd64.tar.gz

ENV GOROOT /opt/go
ENV PATH $PATH:$GOROOT/bin

RUN mkdir /opt/gocode
ENV GOPATH /opt/gocode
RUN yum -y install git.x86_64
RUN yum -y install mercurial.x86_64
