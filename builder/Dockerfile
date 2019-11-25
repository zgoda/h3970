FROM zgoda/ubuntu-trusty-base

RUN \
    dpkg-reconfigure debconf --frontend=noninteractive && \
	apt-get install -yq sudo build-essential git \
	python diffstat gawk chrpath wget cpio \
	texinfo lzop apt-utils bc screen libncurses5-dev locales \
    doxygen libssl-dev dos2unix xvfb x11-utils \
	g++-multilib libtool && \
	rm -rf /var/lib/apt-lists/* && \
	echo "dash dash/sh boolean false" | debconf-set-selections && \
	dpkg-reconfigure dash

RUN useradd -ms /bin/bash -p build build && \
	usermod -aG sudo build

RUN echo "en_US.UTF-8 UTF-8" > /etc/locale.gen && \
    locale-gen

ENV LANG en_US.utf8

USER build
WORKDIR /home/build
