FROM ubuntu:xenial

LABEL maintainer="Podmajersky Marian <marian@decent.ch>" version="0.0.1" \
  description="cli_wallet"

RUN echo 'APT::Install-Recommends 0;' >> /etc/apt/apt.conf.d/01norecommends \
  && echo 'APT::Install-Suggests 0;' >> /etc/apt/apt.conf.d/01norecommends \
  && apt update \
  && DEBIAN_FRONTEND=noninteractive apt-get install -y sudo wget curl libcrypto++9v5 libcurl3

WORKDIR "~"
COPY DECENT-distribution-cli_wallet-1.2-Linux-x64.deb .

RUN dpkg -i DECENT-distribution-cli_wallet-1.2-Linux-x64.deb \
    && apt install -fy \
    && dpkg -i DECENT-distribution-cli_wallet-1.2-Linux-x64.deb

RUN rm DECENT-distribution-cli_wallet-1.2-Linux-x64.deb

RUN export LC_ALL=C; unset LANGUAGE

EXPOSE 8090
EXPOSE 8092
