ARG BASE_IMAGE=daedalusproject/base_java_11
FROM $BASE_IMAGE

MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/sonar-scanner/bin

RUN \
 apt-get update -qq && \
 apt-get install -qq -o=Dpkg::Use-Pty=0 -y wget unzip \
 --no-install-recommends && \
 wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.2.0.1873-linux.zip && \
 unzip sonar-scanner-cli-4.2.0.1873-linux.zip && \
 mv sonar-scanner-4.2.0.1873-linux /opt/sonar-scanner && \
 rm -f sonar-scanner-cli-4.2.0.1873-linux.zip && \
 apt-get purge -y wget unzip && \
 apt-get purge -y --auto-remove && \
 rm -rf /var/lib/apt/lists/*
