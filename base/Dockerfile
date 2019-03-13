FROM ubuntu:bionic
MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN apt-get update -qq && apt-get install -qq -o=Dpkg::Use-Pty=0 -y gnupg ca-certificates --no-install-recommends && rm -rf /var/lib/apt/lists/*
COPY repos/keys/*.key /tmp/
RUN for key in $(ls /tmp/*.key); do apt-key add $key; done && rm -rf /tmp/*.key.pub
COPY repos/sources.list /etc/apt/sources.list
RUN apt-get update -qq && rm -rf /var/lib/apt/lists/*
