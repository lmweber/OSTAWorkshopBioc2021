# OSTAWorkshopBioc2021

This repository contains materials for our [OSTA](https://lmweber.org/OSTA-book/) workshop for the [Bioc2021 conference](https://bioc2021.bioconductor.org/).


## Links

- Link to rendered workshop page: https://lmweber.org/OSTAWorkshopBioc2021/
- Link to source repository: https://github.com/lmweber/OSTAWorkshopBioc2021


## Overview

Our online textbook [Orchestrating Spatially Resolved Transcriptomics Analysis with Bioconductor (OSTA)](https://lmweber.org/OSTA-book/) describes the steps in a computational analysis pipeline for spatially resolved transcriptomics (ST) data using the Bioconductor framework in R, including examples and workflows with R code and datasets that can be run on your own laptop.

OSTA is built around the [SpatialExperiment](https://bioconductor.org/packages/SpatialExperiment) object class and the Bioconductor principle of modularity, which allows users to easily adapt the pipeline to substitute alternative or updated methods for individual steps.


## Prerequisites

- Intermediate level of R programming
- Basic familiarity with Bioconductor object classes, e.g. [SingleCellExperiment](https://bioconductor.org/packages/SingleCellExperiment) or [SpatialExperiment](https://bioconductor.org/packages/SpatialExperiment)
- Basic knowledge of spatially resolved transcriptomics (ST) technologies


## Installation

For this workshop, we will use R version 4.1 and a `release` installation of Bioconductor 3.13, along with the following updated packages installed from GitHub:

```sh
remotes::install_github("drighelli/SpatialExperiment", build_vignettes = TRUE)
remotes::install_github("lmweber/STexampleData", ref = "no_accessors", build_vignettes = TRUE)
remotes::install_github("lmweber/ggspavis", build_vignettes = TRUE)
remotes::install_github("PeteHaitch/DelayedMatrixStats", ref = "906ef69596558b0b7436ce95ad81a529062fa38c")
```

Alternatively, a `devel` installation of Bioconductor 3.14 can also be used, with the latest versions of the packages above.


## Docker image

A Docker image containing the tested version of all materials used in the workshop is also available. Note this is a large download.

To run the Docker image:

```sh
docker run -e PASSWORD=abc -p 8787:8787 lmweber/ostaworkshopbioc2021:latest
```

Then navigate to http://localhost:8787/ in your browser, and log in with username `rstudio` and password `abc`.

