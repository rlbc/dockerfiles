FROM ubuntu:16.04

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br) \
      version="2.6.4"

RUN apt-get update && apt-get install -y \
    build-essential \
    python \
    python-pip \
    r-base \
    python-numpy

RUN pip install python-lzo && \
    pip install RSeQC

RUN apt-get clean && \
    apt-get remove --yes --purge build-essential \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
