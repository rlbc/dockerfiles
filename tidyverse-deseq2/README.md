# dockerfiles

This repo contains the main Dockerfiles which I use regularly in bioinformatics analysis. Images are available at [Docker Hub](https://hub.docker.com/u/rcoan).

Feel free to use these docker images and if you have any questions message me at rafael.coan@unesp.br.

## tidyverse-deseq2

This image contains software for RNA sequencing (RNA-Seq) analysis. It's based on tidyverse 3.4.4, which is a complete R solution to tidy data. The added Bioconductor packages are intended to perform gene expression exploration with DESeq2 and also transform and annotate the gene IDs between GENCODE and NCBI. It also contains tximport, a package to import count tables from pseudo-alignment programs. Extra packages are:

- DESeq2
- tximport
- GenomicFeatures
- ensembldb
- org.Hs.eg.db
- pheatmap
- IHW
- vsn
- rjson

<u>Docker Pull Command:</u> `docker pull rcoan/tidyverse-deseq2`

### Usage

Run as rocker/tidyverse (mounting your current directory to the container):

`docker run -d --rm -p 8787:8787 -v $(PWD):/home/rstudio rcoan/tidyverse-deseq2`

(for a different password add -e PASSWORD=yourpassword)

Then type in browser:

`localhost:8787`

user/password: rstudio/rstudio
