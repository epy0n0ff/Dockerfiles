# Bazel Container
#
# VERSION       0.0.1

FROM ubuntu:15.10

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

RUN apt-get install -y software-properties-common
RUN echo -e '\n' | add-apt-repository ppa:webupd8team/java
RUN apt-get update && apt-get -y install openjdk-8-jdk openjdk-8-source ca-certificates pkg-config zip g++ zlib1g-dev unzip wget
RUN wget https://github.com/bazelbuild/bazel/releases/download/0.1.1/bazel-0.1.1-installer-linux-x86_64.sh
RUN chmod +x bazel-0.1.1-installer-linux-x86_64.sh 
RUN ./bazel-0.1.1-installer-linux-x86_64.sh
RUN export PATH="$PATH:$HOME/bin"
