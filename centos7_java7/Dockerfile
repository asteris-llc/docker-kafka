FROM asteris/java:centos7_java7

MAINTAINER Steven Borrelli <steve@aster.is>

ENV KAFKA_VERSION 0.8.1.1
ENV SCALA_VERSION 2.10
ENV KAFKA_RELEASE kafka_$SCALA_VERSION-$KAFKA_VERSION
ENV KAFKA_URL https://archive.apache.org/dist/kafka/$KAFKA_VERSION/$KAFKA_RELEASE.tgz
ENV KAFKA_HOME /opt/$KAFKA_RELEASE

RUN yum -y install wget tar

RUN wget -nv $KAFKA_URL -O /tmp/$KAFKA_RELEASE.tgz
RUN tar xfz /tmp/$KAFKA_RELEASE.tgz -C /opt

EXPOSE 9092 7203

VOLUME [ "/data", "/logs" ]


