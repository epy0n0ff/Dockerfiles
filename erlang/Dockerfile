# erlang
#
# VERSION       0.0.1
FROM centos
MAINTAINER epy0n.0ff <epy0n.0ff@mail.com>

RUN yum -y install tar \
gcc-c++.x86_64 \
perl.x86_64 \
ncurses-devel.x86_64 \
systemtap-sdt-devel.x86_64 \
make.x86_64

RUN curl -O -L http://download.basho.co.jp.cs-ap-e2.ycloud.jp/otp/download/otp_src_17.1.tar.gz
RUN tar -xzf otp_src_17.1.tar.gz
RUN cd ./otp_src_17.1 && \
 ./configure --prefix=/opt/erlang/17.1 \
  --enable-smp-support \
  --enable-threads \
  --enable-m64-build \
  --enable-vm-probes \
  --enable-kernel-poll \
  --enable-hipe \
  --with-dynamic-trace=systemtap \
  --without-javac \
  --enable-dirty-schedulers \
  --enable-native-libs \
  --enable-sctp && \
 make && \
 make install

RUN rm -r ./otp_src_17.1
RUN rm otp_src_17.1.tar.gz

ENV ERLANG_ROOT /opt/erlang/17.1
ENV PATH $PATH:$ERLANG_ROOT/bin

