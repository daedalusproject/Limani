ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 golang-1.13 \
 golang-1.13-go \
 make \
 --no-install-recommends && \
 ln -s /usr/lib/go-1.13/bin/go /usr/bin/go && \
 adduser --disabled-password --gecos '' daedalus && \
 rm -rf /var/lib/apt/lists/*

USER daedalus
