ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y openjdk-11-jdk-headless=11.0.6+10-1ubuntu1~18.04.1 \
 --no-install-recommends && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
