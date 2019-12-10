FROM rocker/tidyverse:3.6

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br)" \
      date="11/11/2019" \
      description="WGCNA package with RStudio."

RUN apt-get update && apt-get install -y libxt-dev
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN R -e "install.packages('BiocManager'); BiocManager::install('WGCNA')"