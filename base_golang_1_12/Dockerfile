ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 golang-1.12 \
 golang-1.12-go \
 make=4.1-9.1ubuntu1 \
 git=1:2.17.1-1ubuntu0.5 \
 ca-certificates=20180409 \
 go-dep=0.3.2-2 \
 clang=1:6.0-41~exp5~ubuntu1 \
 golint=0.0+git20161013.3390df4-1 \
 --no-install-recommends && \
 ln -s /usr/lib/go-1.12/bin/go /usr/bin/go && \
 adduser --disabled-password --gecos '' daedalus && \
 rm -rf /var/lib/apt/lists/*

USER daedalus
