ARG BASE_IMAGE=daedalusproject/base
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 shellcheck=0.7.0-2build2 \
 shunit2=2.1.6-1.1ubuntu1 \
 make=4.2.1-1.2 \
 ruby=1:2.7+1 \
 sudo \
 --no-install-recommends && \
 gem install bashcov --version 1.8.2 && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/* && \
 adduser --disabled-password --gecos '' daedalus && \
 adduser daedalus sudo && \
 echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

 USER daedalus
