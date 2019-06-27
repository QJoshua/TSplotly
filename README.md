# Description of TSplotly package

<a href="http://www.socr.umich.edu/TCIU/"><img align="middle" src="https://github.com/QJoshua/TSplotly/raw/master/TS_temp_page.png"></a>

**Time series data and ARIMA(X) model visualization by plotly [TSplotly]**

Table of contents
=================

<!--ts-->
   * [Table of contents](#table-of-contents)
   * [Overview](#overview)
   * [R package](#r-package)
   * [Installation](#installation)
   * [Vignettes](#vignettes)
   * [Acknowledgments](#acknowledgments)
   * [References](#references)
<!--te-->


Overview
========

This page is set up to store package, description and related data of an R package **TSplotly**
 TSplotly package provides an effective mechanism to utilize the powerful plotly package for graphing time series data. It contains 4 core functions: 
    TSplot: create plot_ly plot on time series data or fitted ARIMA(X) models.
    ADDline: add lines on existing TSplot objects, as needed.
    GGtoPY: create a convinent way to transform (reformat) ggplot2 datasets into a format that can work on Plot_ly.
    GTSplot: create multiple plot_ly lines (timeseries) based on data frames containing multiple timeseries data

A manuscript entitled ["Controlled Feature Selection and Compressive Big Data Analytics: Applications to Big Biomedical and Health Studies"](https://www.ncbi.nlm.nih.gov/pubmed/30161148) has been published on PLOS ONE Bioinformatics.

R package
=========
The CBDA protocol has been developed in the [R environment](https://www.r-project.org), see the [CBDA R package download site on C-RAN](https://cran.r-project.org/package=CBDA) for the latest R version (currently R-3.5.1). Since a large number of smaller training sets are needed for the convergence of the protocol, we created a workflow that runs on the [LONI pipeline environment](http://pipeline.loni.usc.edu), a free platform for high performance computing that allows the simultaneous submission of hundreds of independent instances/jobs of the CBDA protocol. The methods, software, workflows, datssets and protocols developed here are publicly accessible and openly shared in our [first CBDA release](https://github.com/SOCR/CBDA/releases). 

The source code to run the CBDA protocol is at [source1.zip](https://github.com/SOCR/CBDA/archive/v0.1-alpha.zip) or at [source2.zip](https://github.com/SOCR/CBDA/archive/v0.1-alpha.tar.gz).

The CBDA protocol steps are illustrated in ![Figure](https://user-images.githubusercontent.com/18661302/30587406-0c2edf2c-9d01-11e7-8cef-45f3595ade65.png). 

Installation
============
The version 1.0.0 of the CBDA package can be downloaded and installed with the following command:
```{r Installation of the CBDA package from CRAN, eval = FALSE}
install.packages("CBDA",repos = 'https://cran.r-project.org/')
```

The historical CBDA stats (since publication in April 16 2018 on CRAN) are shown in the Figure below .
![figure0](https://github.com/SOCR/CBDA/blob/master/Images/CBDA_CRAN_stats.jpeg)

A comparison with some other similar packages for the month of November 2018 is shown below. ![figure0](https://github.com/SOCR/CBDA/blob/master/Images/CBDA_stats_comparison_Nov2018.jpeg)

Vignettes
=========
The documentation and vignettes, as well as the source and binary files can be found on  [CRAN](https://cran.r-project.org/web/packages/CBDA/index.html). 
The [binary](https://github.com/SOCR/CBDA/releases/download/1.0.0/CBDA_1.0.0.zip) and the  [source](https://github.com/SOCR/CBDA/releases/download/1.0.0/CBDA_1.0.0.tar.gz) files for the CBDA R package can also be downloaded from our [Github repository](https://github.com/SOCR/CBDA/releases) and install it via the following commands.

```{r Installation of the CBDA package, eval = FALSE}
# Installation from the Windows binary (recommended for Windows systems)
install.packages("/filepath/CBDA_1.0.0.zip", repos = NULL, type = "win.binary") 
# Installation from the source (recommended for Macs and Linux systems)
install.packages("/filepath/CBDA_1.0.0.tar.gz", repos = NULL, type = "source")
```

The necessary packages to run the CBDA algortihm are installed automatically at installation. However, they can also be installed/attached by launching the *CBDA_initialization()* function (see example in the R chunk below).  If the parameter *install* is set to *TRUE* (by default it's set to FALSE), then the *CBDA_initialization()* function installs (if needed) and attaches all the necessary packages to run the CBDA package v1.0.0. This function can be run before any production run or test. The list of packages can pe personalized to comprise extra packages needed for an expanded SL.library or for other needs by the user. The output shows a table (see Figure below) where for each package a TRUE or FALSE is displayed. Thus the necessary steps can be pursued in case some package has a FALSE. 

**N.B.: to eliminate a warning in Windows due to the "doMC" package not available (it was intended for Mac), install the "doMC" with the following command "install.packages("doMC", repos="http://R-Forge.R-project.org")"**

![ipaktable](https://user-images.githubusercontent.com/18661302/36685272-d55b23c0-1af0-11e8-9479-528ef2dfacf6.JPG)
![figure1](https://user-images.githubusercontent.com/18661302/30587406-0c2edf2c-9d01-11e7-8cef-45f3595ade65.png).

Acknowledgments
===============
This work is supported in part by NIH grants [U54 EB020406](http://bd2k.loni.usc.edu/), [P20 NR015331](www.socr.umich.edu/CSCD), [P50 NS091856](http://udallpd.umich.edu/), [P30 DK089503](http://mmoc.med.umich.edu/), [P30AG053760](https://alzheimers.med.umich.edu), [UL1TR002240](https://www.michr.umich.edu), and NSF grants [1734853](http://brain-life.org/), [1636840](http://neurosciencenetwork.org/), [1416953](http://distributome.org), [0716055](http://socr.umich.edu) and [1023115](http://distributome.org). Students, trainees, scholars, and researchers from SOCR, BDDS, MNORC, MIDAS, MADC, MICHR, and the broad R-statistical computing community have contributed ideas, code, and support.

References
==========

* [PMID:30161148](https://www.ncbi.nlm.nih.gov/pubmed/30161148)
* [PMID:26998309](https://www.ncbi.nlm.nih.gov/pubmed/26998309)
* [PMID:26918190](https://www.ncbi.nlm.nih.gov/pubmed/26918190)
* [CBDA R package](https://cran.r-project.org/package=CBDA)
* [CBDA Website](http://socr.umich.edu/HTML5/CBDA/).
