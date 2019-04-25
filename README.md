
<!-- README.md is generated from README.Rmd. Please edit that file -->

# The `aleutpvdata` R Package and GitHub Repository

The goal of `aleutpvdata` is to provide collaborators and interested
users easy access to data associated with the Aleutian Islands harbor
seal research study. The focus, here, is on the satellite teleemtry data
colected between 2014 and 2017.

# Quick Start

The current only option for gaining access to the data in a usable
format is to install the `aleutpvdata` R package via the
`devtools::install_github()` function

``` r
if (!require('devtools')) install.packages('devtools')
devtools::install_github('jmlondon/aleutpvdata')

library(aleutpvdata)

# list the data sets in the aleutpv-data pkg
try(data(package = "aleutpvdata")) 

# for example, load the location data
data(tbl_locs)
head(tbl_locs)
```

Future plans will archive the raw and processed data files with the
Arctic Data Center and DataONE for direct download and access.

# Git Repository Organization

The git repository, hosted here on GitHub, serves two purposes:

1.  host the R package structure that allows other users to install the
    data within the R software environment
2.  host and document the provenance and workflow for downloading,
    processing, tidying satellite telemetry data associated with this
    project

## The `datapack-raw` Directory

This directory is where the raw archive/zip files downloaded from the
Wildlife Computers Data Portal are stored. They are not included within
the git repository for efficiency. The eventual plan is for these files
to be stored and archive on the Animal Telemetry Network and accessible
via DataONE. Most users will have no need or interest in accessing these
data files.

Any processing of data is all handled within the Rmarkdown (`*.Rmd`)
files included within the directory.

The HTML generated from the Rmarkdown is available at
[00-get-data.html](http://jmlondon.github.io/aleutpvdata/00-get-data.html)

## The `datapack` Directory

This directory is where the processed data are created and stored in
comma-separated format.They are not included within the git repository
for efficiency. The eventual plan is for these files to be stored and
archive on the Arctic Data Center and accessible via DataONE. Most users
who aren’t accessing these data through the R programming environment
will want to work with these data files.

Any processing of data is all handled within the Rmarkdown (`*.Rmd`)
files included within the directory.

The HTML generated from the Rmarkdown is available at
[01-tidy-data.html](http://jmlondon.github.io/aleutpvdata/01-tidy-data.html)

## LHX Deployments in 2016

In 2016, 10 harbor seals were released with surgically implanted
life-history tags (LHX). Below is a table of those animals and their
unique `speno`

| SpeNo        | Age       | Sex    |
| :----------- | :-------- | :----- |
| PV2014\_2005 | adult     | female |
| PV2016\_3011 | sub-adult | female |
| PV2016\_3012 | adult     | female |
| PV2016\_3016 | sub-adult | female |
| PV2016\_3019 | sub-adult | male   |
| PV2016\_3022 | adult     | male   |
| PV2016\_3027 | sub-adult | female |
| PV2016\_3031 | adult     | male   |
| PV2016\_3032 | sub-adult | male   |
| PV2016\_3033 | sub-adult | female |

Table of LHX Surgery Animals

### Citation – DRAFT: DO NOT CITE OR USE AT THIS TIME

This data package is under heavy development. Please do not cite this
data or this repository at this time. Any use should be done in close
coordination and communication with the package author.

### Contributions

We welcome contributions from everyone. Before you get started, please
see our [contributor guidelines](CONTRIBUTING.md). Please note that this
project is released with a [Contributor Code of Conduct](CONDUCT.md). By
participating in this project you agree to abide by its terms.

-----

##### NOAA/Dept. of Commerce Disclaimer

<sub>This repository is a scientific product and is not official
communication of the National Oceanic and Atmospheric Administration, or
the United States Department of Commerce. All NOAA GitHub project code
is provided on an ‘as is’ basis and the user assumes responsibility for
its use. Any claims against the Department of Commerce or Department of
Commerce bureaus stemming from the use of this GitHub project will be
governed by all applicable Federal law. Any reference to specific
commercial products, processes, or services by service mark, trademark,
manufacturer, or otherwise, does not constitute or imply their
endorsement, recommendation or favoring by the Department of Commerce.
The Department of Commerce seal and logo, or the seal and logo of a DOC
bureau, shall not be used in any manner to imply endorsement of any
commercial product or activity by DOC or the United States
Government.</sub>

-----
