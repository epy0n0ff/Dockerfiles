# Bazel Container
#
# VERSION       0.0.3

FROM ubuntu:15.10

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

RUN apt-get install -y software-properties-common && \
    echo -e '\n' | add-apt-repository ppa:webupd8team/java && \
    apt-get update && apt-get -y install openjdk-8-jdk openjdk-8-source ca-certificates pkg-config zip g++ zlib1g-dev unzip wget && \
    wget https://github.com/bazelbuild/bazel/releases/download/0.3.0/bazel-0.3.0-installer-linux-x86_64.sh && \
    chmod +x bazel-0.3.0-installer-linux-x86_64.sh && \
    ./bazel-0.3.0-installer-linux-x86_64.sh && \
    export PATH="$PATH:$HOME/bin"
