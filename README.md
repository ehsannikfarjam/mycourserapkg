# mycourserapkg

[![Build Status](https://app.travis-ci.com/github/ehsannikfarjam/mycourserapkg.svg?branch=main)](https://app.travis-ci.com/github/ehsannikfarjam/mycourserapkg)

This repository contains the `mycourserapkg` R package for the Coursera
course "Mastering Software Development in R". The badge above shows the
current Travis CI build status for the main branch.

## Overview

`mycourserapkg` is a small example R package created for the Coursera
course "Mastering Software Development in R". It demonstrates how to:

- Organize R code in a package structure.
- Document functions with roxygen2 so that `.Rd` files and a
  `NAMESPACE` file are generated automatically.
- Write tests using the `testthat` framework.
- Include an R Markdown vignette built with `knitr` and `rmarkdown`.
- Integrate the package with continuous integration using Travis CI.

The package currently provides a single exported function,
`mean_two_numbers()`, which computes the arithmetic mean of two numeric
scalar values.

## Installation

Once this package is pushed to GitHub, it can be installed with
`devtools` from the R console:

```r
# install.packages("devtools")
devtools::install_github("ehsannikfarjam/mycourserapkg")
```

## Example

After installation, load the package and call `mean_two_numbers()`:

```r
library(mycourserapkg)

mean_two_numbers(1, 3)
mean_two_numbers(10, 20)
```

## Continuous integration with Travis CI

This repository contains a `.travis.yml` file configured for R. To
enable Travis CI:

1. Create a public GitHub repository whose root contains this package
   (the `DESCRIPTION` file should be at the top level of the repo).
2. Push all package files to GitHub.
3. Sign in to `https://travis-ci.com` using your GitHub account.
4. Enable builds for your repository.
5. Trigger a build by pushing a commit to GitHub.
6. Once the build is passing with no errors, warnings, or notes, obtain
   the Travis CI badge markdown snippet from the Travis web interface
   and replace the placeholder badge at the top of this README.

