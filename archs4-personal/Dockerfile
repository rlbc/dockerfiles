FROM rocker/tidyverse:4.0.4

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br)" \
      date="13/04/2021" \
      description="ARCHS4 and DESeq2."

RUN R -e "install.packages(c('BiocManager', 'tools', 'dendextend')); BiocManager::install(c('rhdf5', 'preprocessCore', 'sva', 'vioplot', 'GenomicFeatures', 'DESeq2', 'tximport', 'pheatmap', 'vsn', 'RColorBrewer'))"
