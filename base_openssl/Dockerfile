ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y --no-install-recommends \
 openssl=1.1.1-1ubuntu2.1~18.04.4 && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
