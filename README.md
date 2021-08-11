# OSTA Workshop Bioc2021

This repository contains materials for our [OSTA](https://lmweber.org/OSTA-book/) workshop at the [Bioc2021 conference](https://bioc2021.bioconductor.org/).


## Links

- Workshop website: https://lmweber.org/OSTAWorkshopBioc2021/
- Workshop source repository: https://github.com/lmweber/OSTAWorkshopBioc2021
- OSTA website: https://lmweber.org/OSTA-book/
- OSTA source repository: https://github.com/lmweber/OSTA-book


## Overview

Our online textbook [Orchestrating Spatially Resolved Transcriptomics Analysis with Bioconductor (OSTA)](https://lmweber.org/OSTA-book/) describes the steps in a computational analysis pipeline for spatially resolved transcriptomics (ST) data using the Bioconductor framework in R, including examples and workflows with R code and datasets.

OSTA is built around the [SpatialExperiment](https://bioconductor.org/packages/SpatialExperiment) object class and the Bioconductor principle of modularity, which allows users to easily adapt the pipeline to substitute alternative or updated methods for individual steps.

In particular, OSTA and `SpatialExperiment` are compatible with [SingleCellExperiment](https://bioconductor.org/packages/SingleCellExperiment), allowing existing methods and pipelines developed for single-cell RNA sequencing data (such as those described in [OSCA](https://bioconductor.org/books/release/OSCA/)) to be re-used and adapted to the spatial context.


## Prerequisites

- Intermediate level of R programming
- Basic familiarity with Bioconductor object classes, e.g. [SpatialExperiment](https://bioconductor.org/packages/SpatialExperiment) and/or [SingleCellExperiment](https://bioconductor.org/packages/SingleCellExperiment)
- Basic knowledge of spatially resolved transcriptomics (ST) technologies


## Installation

For this workshop, we will use R version 4.1 and a `devel` installation of Bioconductor 3.14. In addition, you will need to install the following package from GitHub:

```sh
remotes::install_github("lmweber/ggspavis", build_vignettes = TRUE)
```

Alternatively, you can use a `release` version of Bioconductor 3.13 along with the following versions of packages installed from GitHub:

```sh
remotes::install_github("drighelli/SpatialExperiment", build_vignettes = TRUE)
remotes::install_github("lmweber/STexampleData", ref = "no_accessors", build_vignettes = TRUE)
remotes::install_github("lmweber/ggspavis", build_vignettes = TRUE)
```


## Docker image

A Docker image containing a complete version of all materials used in the workshop is also available. Note this is a large download.

To run the Docker image:

```sh
docker run -e PASSWORD=abc -p 8787:8787 lmweber/ostaworkshopbioc2021:latest
```

Then navigate to http://localhost:8787/ in your browser, and log in with username `rstudio` and password `abc`.


## Acknowledgments

[OSTA](https://lmweber.org/OSTA-book/) contributors:

- Abby Spangler, *Lieber Institute for Brain Development, Baltimore, MD, USA*
- Madhavi Tippani, *Lieber Institute for Brain Development, Baltimore, MD, USA*
- Leonardo Collado-Torres, *Lieber Institute for Brain Development, Baltimore, MD, USA*
- Stephanie C. Hicks, *Johns Hopkins Bloomberg School of Public Health, Baltimore, MD, USA*

[SpatialExperiment](https://bioconductor.org/packages/SpatialExperiment):

- Dario Righelli, *Department of Statistical Sciences, University of Padova, Padova, Italy*
- Helena L. Crowell, *Department of Molecular Life Sciences, University of Zurich, Zurich, Switzerland*
- Aaron Lun, *Genentech, South San Francisco, CA, USA*
- Stephanie C. Hicks, *Johns Hopkins Bloomberg School of Public Health, Baltimore, MD, USA*
- Davide Risso, *Department of Statistical Sciences, University of Padova, Padova, Italy*

