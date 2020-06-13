## Polyester

RNA-Seq reads simulator Polyester 1.22. Link to [Bioconductor](https://bioconductor.org/packages/release/bioc/html/polyester.html) and [GitHub](https://github.com/alyssafrazee/polyester). Based on rocker/tidyverse 3.6.

<u>Docker Pull Command:</u> `docker pull rcoan/polyester`

### Usage

Run as rocker/tidyverse (mounting your current directory to the container):

`docker run -d --rm -p 8787:8787 -e PASSWORD=poly -v $(PWD):/home/rstudio rcoan/polyester`

Then type in browser:

`localhost:8787`

user/password: rstudio/poly
