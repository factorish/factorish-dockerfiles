# Base Factorish Python Image
#
# Author: Paul Czarkowski
# Date: 08/16/2014

FROM ubuntu:trusty
MAINTAINER Paul Czarkowski "paul@paulcz.net"

# Base Deps
RUN \
  apt-get update -yq && \
  apt-get install -yq \
  make \
  ca-certificates \
  net-tools \
  sudo \
  wget \
  curl \
  vim \
  strace \
  lsof \
  netcat \
  lsb-release \
  locales \
  socat \
  supervisor \
  runit \
  --no-install-recommends && \
  locale-gen en_US.UTF-8

# install etcdctl and confd
RUN curl -sSL -o /usr/local/bin/etcdctl https://s3-us-west-2.amazonaws.com/opdemand/etcdctl-v0.4.6 \
&& chmod +x /usr/local/bin/etcdctl \
&& curl -sSL -o /usr/local/bin/confd https://github.com/kelseyhightower/confd/releases/download/v0.7.1/confd-0.7.1-linux-amd64 \
&& chmod +x /usr/local/bin/confd \
&& mkdir /app

WORKDIR /app
