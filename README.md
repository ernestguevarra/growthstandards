# growthstandards [![Build Status](https://travis-ci.org/HBGDki/growthstandards.svg?branch=master)](https://travis-ci.org/HBGDki/growthstandards) [![codecov.io](https://codecov.io/gh/HBGDki/growthstandards/coverage.svg?branch=master)](https://codecov.io/gh/HBGDki/growthstandards?branch=master)

A collection of utility functions for conveniently converting anthropometric measurements to z-scores or centiles (and converting z-scores / centiles to measurements) for three major growth standards:

- WHO growth standard (functions prefixed with `who_`)
- INTERGROWTH newborn size standard including very preterm (functions prefixed with `igb_`)
- INTERGROWTH fetal growth standard (functions prefixed with `igfet_`)

These growth standards have previously not necessarily been easy to access inside an R analysis. In some cases R code has been provided for making conversions with the growth standard but in a form that is difficult to embed and generalize (copying and pasting code that will be frequently used is messy will almost surely lead to errors). Some standards are provided only through published coefficients. The goal here is to put all the standards into a single package with a unified interface, while providing additional functionality like interpolation for regions where standard's provided tables are sparse.

The growth standard conversion methods have been painstakingly checked for accuracy through comparisons with the standards provided by the original sources. However, we advise caution and double checking against the original sources when results will impact decisions. Links to the original sources can be found in the sections for each standard below.

## Installation

```r
options(repos = c(CRAN = "http://cran.rstudio.com/",
  deltarho = "http://packages.deltarho.org"))
install.packages("growthstandards")
```

Or:

```r
devtools::install_github("HBGDki/growthstandards")
```

## Usage

See [here](articles/docs.html) for several examples of how to use this package.
