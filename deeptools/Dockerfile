FROM ubuntu:focal

RUN apt-get update && apt-get install -y \
    libbz2-dev liblzma-dev python3 python3-setuptools python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --no-cache-dir deeptools
