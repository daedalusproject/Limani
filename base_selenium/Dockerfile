ARG BASE_IMAGE=daedalusproject/base_java_11
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 wget \
 --no-install-recommends && \
 adduser --disabled-password --gecos '' daedalus && \
 wget https://selenium-release.storage.googleapis.com/3.141/selenium-server-standalone-3.141.59.jar -o selenium-server-standalone.jar -P /home/daedalus/ && \
 apt-get purge -y wget --auto-remove && \
 rm -rf /var/lib/apt/lists/*
