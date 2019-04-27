ARG BASE_IMAGE=daedalusproject/base_develop
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 docker-ce \
 docker-ce-cli \
 containerd.io \
 daedalus-project-docker-build=0.1-1 \
 --no-install-recommends && \
 gem install bashcov --version 1.8.2 && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/* && \

