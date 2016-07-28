# Apache Spark Container
#
# VERSION       0.0.1

FROM ubuntu:16.04

MAINTAINER epy0n.0ff <epy0n.0ff@gmail.com>

ENV SPARK_HOME /usr/local/spark
ENV PATH $SPARK_HOME/bin:$PATH

ADD http://d3kbcqa49mib13.cloudfront.net/spark-2.0.0-bin-hadoop2.7.tgz /usr/local
RUN cd /usr/local && \
     tar zxvf spark-2.0.0-bin-hadoop2.7.tgz && \
     ln -s spark-2.0.0-bin-hadoop2.7 spark && \
     apt-get update && apt-get install  -y openjdk-8-jdk && \
     rm /usr/local/spark-2.0.0-bin-hadoop2.7.tgz
