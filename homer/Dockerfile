FROM continuumio/miniconda3:4.11.0

WORKDIR /home/homer

RUN conda config --add channels defaults
RUN conda config --add channels bioconda
RUN conda config --add channels conda-forge

RUN conda install wget samtools r-essentials bioconductor-deseq2 bioconductor-edger

ADD "http://homer.ucsd.edu/homer/configureHomer.pl" WORKDIR

RUN perl configureHomer.pl -install

ENV PATH=$PATH:/home/homer/bin/


