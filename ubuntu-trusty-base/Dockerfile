FROM ubuntu:trusty

RUN \
    dpkg --add-architecture i386 && \
    DEBIAN_FRONTEND=noninteractive apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get upgrade -yq
