ARG BASE_IMAGE=daedalusproject/base_deb_builder
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y \
 dh-make-perl=0.109 \
 libmodule-install-perl=1.19-1 \
 libgit-wrapper-perl=0.048-1 \
 libcatalyst-modules-perl=48 \
 libmodule-build-perl=0.423100-1 \
 libmodule-build-tiny-perl=0.039-1 \
 --no-install-recommends && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/* && \
 echo -e "DEBEMAIL=\"alvaro.castellano.vela@gmail.com\"\nDEBFULLNAME=\"Álvaro Castellano Vela\"\nexport DEBEMAIL DEBFULLNAME\n" >> ~/.bashrc.backup
