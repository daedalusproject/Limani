ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE
MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 percona-server-client=8.0.20-11-1.bionic \
 daedalus-project-mysql-utils=0.4-7 \
 --no-install-recommends && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
