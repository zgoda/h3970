FROM ubuntu:trusty

RUN dpkg-reconfigure debconf --frontend=noninteractive && \
    dpkg --add-architecture i386 && \
    apt-get update && \
    apt-get upgrade -yq
