ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 docker-ce=5:19.03.8~3-0~ubuntu-bionic \
 docker-ce-cli=:19.03.8~3-0~ubuntu-bionic \
 containerd.io=1.2.13-1 \
 daedalus-project-docker-build=0.2-4 \
 --no-install-recommends && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*

