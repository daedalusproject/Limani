FROM ubuntu:bionic
MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y gnupg ca-certificates wget --no-install-recommends && \
 wget -O - http://packages.windmaker.net/WINDMAKER-GPG-KEY.pub | apt-key add - && \
 wget -O - http://repo-bionic.windmaker.net/repo-bionic.windmaker.net.gpg-key.pub | apt-key add - && \
 wget -O - https://repo.daedalus-project.io/repo.daedalus-project.io.gpg-key.pub | apt-key add - && \
 apt-get purge -qq -o=Dpkg::Use-Pty=0 -y gnupg wget openssl && \
 apt-get autoremove -qq -o=Dpkg::Use-Pty=0 -y && \
 apt-get autoclean -qq -o=Dpkg::Use-Pty=0 -y && \
 echo "deb http://repo-bionic.windmaker.net/ bionic main" > /etc/apt/sources.list && \
 echo "deb http://packages.windmaker.net/ any main" >> /etc/apt/sources.list && \
 echo "deb [arch=amd64] http://packages.windmaker.net/ bionic main" >> /etc/apt/sources.list && \
 echo "deb [arch=amd64] http://repo.daedalus-project.io/ bionic main" >> /etc/apt/sources.list && \
 echo "Package: *" > /etc/apt/preferences.d/priority && \
 echo "Pin: origin repo.daedalus-project.io" >> /etc/apt/preferences.d/priority && \
 echo "Pin-Priority: 700" >> /etc/apt/preferences.d/priority && \
 apt-get update -qq && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
