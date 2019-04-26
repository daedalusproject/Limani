ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 shellcheck=0.4.6-1 \
 shunit2=2.1.6-1.1ubuntu1 \
 make=4.1-9.1ubuntu1 \
 ruby=1:2.5.1 \
 --no-install-recommends && \
 gem install bashcov --version 1.8.2 && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
