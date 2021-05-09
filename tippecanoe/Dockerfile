FROM ubuntu:latest

ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
  && apt-get -y upgrade \
  && apt-get -y install software-properties-common git build-essential libsqlite3-dev zlib1g-dev \
  && add-apt-repository ppa:ubuntu-toolchain-r/test \
  && apt-get update -y

RUN mkdir -p /tmp/tippecanoe-src
RUN mkdir -p /tmp/tippecanoe-workdir
RUN git clone https://github.com/mapbox/tippecanoe.git /tmp/tippecanoe-src
WORKDIR /tmp/tippecanoe-src

RUN make -j \
  && make install

WORKDIR /
RUN rm -rf /tmp/tippecanoe-src \
  && apt-get -y remove --purge build-essential && apt-get -y autoremove

WORKDIR /tmp/tippecanoe-workdir