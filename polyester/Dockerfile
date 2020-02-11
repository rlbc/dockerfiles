FROM rocker/tidyverse:3.6

LABEL maintainer="Rafael Coan (rafael.coan@unesp.br)" \
      date="11/02/2020" \
      description="Polyester for RNA-Seq reads simulation."

RUN R -e "install.packages('BiocManager'); BiocManager::install('polyester')"
