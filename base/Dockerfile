FROM ubuntu:bionic
MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y gnupg ca-certificates --no-install-recommends && \
 wget -O - http://packages.windmaker.net/WINDMAKER-GPG-KEY.pub | apt-key add - && \
 wget -O - http://repo-bionic.windmaker.net/repo-bionic.windmaker.net.gpg-key.pub | apt-key add - && \
 wget -O - https://repo.daedalus-project.io/repo.daedalus-project.io.gpg-key.pub | apt-key add - && \
 rm -rf /var/lib/apt/lists/*
COPY repos/sources.list /etc/apt/sources.list
RUN apt-get update -qq && rm -rf /var/lib/apt/lists/*
