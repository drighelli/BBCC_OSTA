# BBCC 2025: Orchestrating Spatial Transcriptomics Analysis with Bioconductor

[Tutorial homepage](https://drighelli.github.io/BBCC_OSTA/)

## Speakers

* Dario Righelli<sup>1<sup>
* Francesca Calanca<sup>2,3<sup>
* Emanuela Scafuri<sup>2,3<sup>
    1 Department of Electrical Engineer and Information Technology, University of Naples "Federico II", Italy\
    2 Department of Chemical, Materials and Production Engineering, University of Naples "Federico II", Italy\
    3 Institute for Applied Mathematics "M. Picone", IAC-CNR, Naples, Italy

## Description

This tutorial strives to be of interest to experimental biologists wanting to analyze their data and to bioinformaticians approaching spatial transcriptomics data.\
We use as a "textbook" the online book **"Orchestrating Spatial Transcriptomics Analysis with Bioconductor"** ([OSTA](https://lmweber.org/OSTA/)), 
which provides reproducible examples and discussion on computational analysis workflows for spatial omics data using Bioconductor in R.\
Like the book, this tutorial has been structured to provide a theoretical and practical overview of spatial transcriptomics analysis. Specifically, we will examine Cosmx's molecule-based approach, paying close attention to the key stages of the analysis process.

## Learning objectives

In particular, participants will learn:
* Overview of Spatial Transcriptomics' methodologies (spot-based & molecule-based)
* Cosmx's approach in detail
* Downloading, uploading and data preprocessing with Bioconductor
* Annotation of cell types 
* Identification of marker genes
* Analysis of Neighbourhood-based gene expression
* Cell-cell interaction using Neighbourhood graph
* Point-pattern Analysis

## Time outline

| Activity                     | Time |
|------------------------------|------|
| Introduction and Setup                                          | 9:00-9:15    |
| Theoretical overview                                            | 9:15-10:45   |
| Introduction to the workflow                                    | 10:45-11:00  |
| Coffee break                                                    | 11:00-11:15  |
| Exploratory Data Analysis and Quality Control (QC)              | 11:15-11:45  |
| Cell type annotation & marker genes identification              | 11:45-12:15  |
| Neighbourhood-based analyses                                    | 12:15-13:00  |
| Downstream Analyses                                             | 13:00-13:45  |
| Q&A + Discussion session                                        | 13:45-14:00  |

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
