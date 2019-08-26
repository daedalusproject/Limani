ARG BASE_IMAGE=daedalusproject/base_deb_builder
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 python3-setuptools=39.0.1-2 \
 python3-pip=9.0.1-2.3~ubuntu1.18.04.1 \
 python3-dev=3.6.7-1~18.04 \
 libffi-dev=3.2.1-8 \
 equivs=2.1.0 \
 devscripts=2.17.12ubuntu1.1 \
 dh-virtualenv=1.0-1 \
 --no-install-recommends && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/* && \
 echo -e "DEBEMAIL=\"alvaro.castellano.vela@gmail.com\"\nDEBFULLNAME=\"Álvaro Castellano Vela\"\nexport DEBEMAIL DEBFULLNAME\n" >> ~/.bashrc.backup
