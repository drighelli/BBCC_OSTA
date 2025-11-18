# BBCC 2025: Orchestrating Spatial Transcriptomics Analysis with Bioconductor

[Tutorial homepage](https://drighelli.github.io/BBCC_OSTA/)

## Speakers

* Dario Righelli, Department of Statistical Sciences, University of Padova, Italy
* Francesca Calanca, 
* Emanuela Scafuri, 

## Description
...
This tutorial uses as a "text-book" the online book "Orchestrating Single-Cell
Analysis with Bioconductor"
([OSCA](https://bioconductor.org/books/release/OSCA/)), 
started in 2018 and continuously updated by many contributors from the Bioconductor
community. 
Like the book, this tutorial strives to be of interest to the
experimental biologists wanting to analyze their data and to the bioinformaticians
approaching spatial transcriptomics data.

## Learning objectives

Attendees will learn how to analyze multi-condition single-cell RNA-seq from
raw data to statistical analyses and result interpretation.

In particular, participants will learn:
...

## Time outline

TO BE EDITED 

| Activity                     | Time |
|------------------------------|------|
| Introduction and Setup                                          | 9:00-9:30    |
| Introduction to Bioconductor and the SingleCellExperiment class | 9:30-10:00   |
| Exploratory Data Analysis and Quality Control (EDA/QC)          | 10:00-10:45  |
| Coffee break                                                    | 10:45-11:00  |
| Clustering and cell type annotation                             | 11:00-11:45  |
| Q&A session                                                     | 11:45-12:00  |
| Multi-sample analyses                                           | 12:00-12:45  |
| Q&A + Discussion session                                        | 12:45-13:30  |
| Lunch                                                           | 13:30        |

## Docker container

To locally run this tutorial in a
[Docker container](ghcr.io/drighelli/bbcc_osta:latest),
pull the Docker image via

```
docker pull ghcr.io/drighelli/bbcc_osta:latest
``` 

and then run the image via

```
docker run -e PASSWORD=bioc -p 8787:8787 ghcr.io/drighelli/bbcc.osta
```

Once running, navigate to http://localhost:8787/ in your browser and login with
username `rstudio` and password `bioc`.

## Local installation

This tutorial can be installed like an ordinary R package via:

```
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

if (!require("remotes", quietly = TRUE))
    install.packages("remotes")

BiocManager::install("Bioconductor/BBCC.OSTA",
                     dependencies = TRUE,
                     build_vignettes = TRUE)
```
