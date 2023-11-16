# hash:sha256:9482e39c88e03ee347ecc817d2535fb17b0e7920261604d0fbee8f488c426d3b
FROM registry.codeocean.com/codeocean/r-studio:1.2.5019-r4.0.3-ubuntu18.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        cmake=3.10.2-1ubuntu2.18.04.2 \
        dvipng=1.15-1 \
        libcairo2-dev=1.15.10-2ubuntu0.1 \
        libnlopt-dev=2.4.2+dfsg-4 \
        lmodern=2.004.5-3 \
        pandoc=1.19.2.4~dfsg-1build4 \
        pandoc-citeproc=0.10.5.1-1build4 \
        pkg-config=0.29.1-0ubuntu2 \
        texlive-fonts-recommended=2017.20180305-1 \
        texlive-generic-recommended=2017.20180305-1 \
        texlive-latex-extra=2017.20180305-2 \
        texlive-publishers=2017.20180305-2 \
    && rm -rf /var/lib/apt/lists/*

RUN Rscript -e 'remotes::install_version("kableExtra", "1.3.4")' \
    && Rscript -e 'remotes::install_version("knitr", "1.38")' \
    && Rscript -e 'remotes::install_version("tidyverse", "1.3.1")'
