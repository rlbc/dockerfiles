FROM ubuntu:16.04

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br)" \
      version="1.2"

# install dependencies
RUN apt-get update && apt-get install -y \
    wget \
    build-essential \
    python

# download and compile PLEK
WORKDIR /docker
RUN wget -q "https://sourceforge.net/projects/plek/files/PLEK.1.2.tar.gz" && \
    tar -xzf PLEK.1.2.tar.gz && \
    cd PLEK.1.2

CMD ['PLEK_setup.py']

ENV PATH=$PATH:/docker/PLEK.1.2/

# clean
RUN rm -rf /docker/PLEK.1.2.tar.gz && \
    apt-get clean && \
    apt-get remove --yes --purge wget build-essential

#CMD ["/bin/bash"]

