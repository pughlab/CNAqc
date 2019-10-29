
# CNAqc <img src='man/figures/logo.png' align="right" height="139" />

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/caravagn/CNAqc.svg?branch=master)](https://travis-ci.org/caravagn/CNAqc)
[![Lifecycle:
maturing](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![](https://img.shields.io/badge/Part%20of-evoverse-blue.svg)](https://caravagn.github.io/evoverse)
<!-- badges: end -->

`CNAqc` is a package to process and assess the quality of absoluteCopy
Number Alteration (CNA) calls, in light of somatic mutation data and
purity estimates.

The package provides statistical methods to:

  - quantify the concordance between mutation and CNA calls;

  - determine estimates of mutations’ Cancer Cell Franctions (CCFs).

Most algorithms in `CNAqc` match the allelic imbalance of CNA segments
with the allelic frequencies of somatic mutations, in order to determine
a number of quantitative metrics. These metrics. can be used to measure
the quality of the current purity estimate, or to determine determine
CCF values.

`CNAqc` is part of the `evoverse` set of [R
packages](https://caravagn.github.io/evoverse) to implement Cancer
Evolution analyses.

#### Statistical models

`CNAqc` implements a karyotype-weighted linear score that exploits the
distance computed between a peak in the data (empirical), and its
theoretical expectation. This score is determined by standard CNA
computations accouting for normal plodiy, tumour purity and ploidy. The
peaks are determined uwing kernel density methods and peak-detection
heuristics.

To determine CCF, `CNAqc` uses an entropy-based heuristic for the
estimation of the number of copies of each mutation (mutation
multiplicity). Then, `CNAqc` uses standard equations to estimate CCFs
normalizing the allelic frequency for tumour purity, segment ploidy and
mutation
multiplicity.

#### Help and support

## [![](https://img.shields.io/badge/GitHub%20Pages-https://caravagn.github.io/CNAqc/-yellow.svg)](https://caravagn.github.io/CNAqc)

### Installation

You can install the released version of `CNAqc` from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("caravagn/CNAqc")
```

-----

#### Copyright and contacts

Giulio Caravagna, PhD. *Institute of Cancer Research, London,
UK*.

[![](https://img.shields.io/badge/Email-gcaravagn@gmail.com-seagreen.svg)](mailto:gcaravagn@gmail.com)
[![](https://img.shields.io/badge/Github-caravagn-seagreen.svg)](https://github.com/caravagn)
[![](https://img.shields.io/badge/Twitter-@gcaravagna-steelblue.svg)](https://twitter.com/gcaravagna)
[![](https://img.shields.io/badge/Personal%20webpage-https://bit.ly/2kc9E6Y-red.svg)](https://sites.google.com/site/giuliocaravagna/)
