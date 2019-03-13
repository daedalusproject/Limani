FROM ubuntu:bionic
MAINTAINER Álvaro Castellano Vela <alvaro.castellano.vela@gmail.com>

RUN apt-get update -qq && apt-get install -qq -o=Dpkg::Use-Pty=0 -y gnupg ca-certificates --no-install-recommends && rm -rf /var/lib/apt/lists/*
COPY repos/keys/*.key /tmp/
RUN sudo apt-key add /tmp/*.key && rm -rf /tmp/*.key.pub

