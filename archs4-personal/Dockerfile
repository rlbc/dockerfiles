FROM rocker/tidyverse:4.0.4

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br)" \
      date="13/04/2021" \
      description="ARCHS4 and DESeq2."

RUN apt-get update && apt-get install -y tk libbz2-dev liblzma-dev
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

#RUN R -e "install.packages(c('BiocManager', 'tools', 'dendextend')); BiocManager::install(c('rhdf5', 'sva', 'vioplot', 'GenomicFeatures', 'DESeq2', 'tximport', 'pheatmap', 'vsn', 'RColorBrewer'))"
RUN R -e "BiocManager::install('preprocessCore', configure.args='--disable-threading')"

#GenomicFeatures não foi instalado - ok

#cram/cram_io.c:57:10: fatal error: bzlib.h: No such file or directory
#https://github.com/samtools/samtools/issues/692

#cram/cram_io.c:61:10: fatal error: lzma.h: No such file or directory
#https://stackoverflow.com/questions/22738077/backports-lzma-lzmamodule-c11518-fatal-error-lzma-h-no-such-file-or-direct/22764178
