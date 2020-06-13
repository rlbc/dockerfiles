## WGCNA

This image contains the [WGCNA](https://horvath.genetics.ucla.edu/html/CoexpressionNetwork/Rpackages/WGCNA/Tutorials/index.html) Bioconductor package for co-expression network construction. It is based on tidyverse 3.6 and no extra packages.

<u>Docker Pull Command:</u> `docker pull rcoan/wgcna`

### Usage

Run as rocker/tidyverse (mounting your current directory to the container):

`docker run -d -p 8787:8787 -e PASSWORD=wgcna -v $(PWD):/home/rstudio rcoan/wgcna`

Then type in browser:

`localhost:8787`

user/password: rstudio/wgcna
