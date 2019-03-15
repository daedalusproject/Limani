FROM daedalusproject/base
MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y nginx-light --no-install-recommends && \
 rm -rf /var/lib/apt/lists/*
