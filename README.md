# dockerfiles

This repo contains the main Dockerfiles which I use regularly in bioinformatics analysis. Feel free to use these docker images and if you have any questions message me at rafael.coan@unesp.br.

Here is a brief description of all current software.

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

### Usage

Run as rocker/tidyverse (mounting your current directory to the container):

`docker run -d --rm -p 8787:8787 -v $(PWD):/home/rstudio rcoan/tidyverse-deseq2`

(for a different password add -e PASSWORD=yourpassword)

Then type in browser:

`localhost:8787`

user/password: rstudio/rstudio

## PLEK

PLEK 1.2 for lncRNA discovery.

## FEELnc

[FEELnc](https://github.com/tderrien/FEELnc) is a program to identify and classify new lncRNA. It is fast and accurate. This image is based on version 0.1.1 - [Paper](http://nar.oxfordjournals.org/content/early/2017/01/03/nar.gkw1306.full).

### Usage

FEELnc has three modules runned separetly in a terminal window.

`docker run -w /mnt -v $(PWD):/mnt --rm rcoan/feelnc FEELnc_filter.pl <OPTIONS> > <OUTPUT_FILE>`

`docker run -w /mnt -v $(PWD):/mnt --rm rcoan/feelnc FEELnc_codpot.pl <OPTIONS>`

`docker run -w /mnt -v $(PWD):/mnt --rm rcoan/feelnc FEELnc_classifier.pl <OPTIONS> > <OUTPUT_CLASSES.TXT>`

All options found in the manual can be added.

The above commands mount your current directory to the container.

## WGCNA

This image contains the [WGCNA](https://horvath.genetics.ucla.edu/html/CoexpressionNetwork/Rpackages/WGCNA/Tutorials/index.html) Bioconductor package for co-expression network construction. It is based on tidyverse 3.6 and no extra packages.

### Usage

Run as rocker/tidyverse (mounting your current directory to the container):

`docker run -d -p 8787:8787 -e PASSWORD=wgcna -v $(PWD):/home/rstudio rcoan/wgcna`

Then type in browser:

`localhost:8787`

user/password: rstudio/wgcna
