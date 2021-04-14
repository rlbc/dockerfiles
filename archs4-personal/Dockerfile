FROM rocker/tidyverse:4.0.4

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br)" \
      date="13/04/2021" \
      description="ARCHS4 and DESeq2."

RUN apt-get update && apt-get install -y tk
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN R -e "install.packages(c('BiocManager', 'tools', 'dendextend')); BiocManager::install(c('rhdf5', 'preprocessCore', 'sva', 'vioplot', 'GenomicFeatures', 'DESeq2', 'tximport', 'pheatmap', 'vsn', 'RColorBrewer'))"
