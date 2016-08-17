
<!-- README.md is generated from README.Rmd. Please edit that file -->
okcupiddata
===========

[![Build Status](https://travis-ci.org/rudeboybert/okcupiddata.png?branch=master)](https://travis-ci.org/rudeboybert/okcupiddata) [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/okcupiddata)](http://cran.r-project.org/package=okcupiddata) [![CRAN RStudio mirror downloads](http://cranlogs.r-pkg.org/badges/okcupiddata)](http://www.r-pkg.org/pkg/okcupiddata)

R package of OkCupid profile data from [OkCupid Profile Data for Introductory Statistics and Data Science Courses](http://www.amstat.org/publications/jse/v23n2/kim.pdf): 59,946 OkCupid users who were living within 25 miles of San Francisco, had active profiles on June 26, 2012, were online in the previous year, and had at least one picture in their profile.

Note:

-   The code, data, and codebook for the original Journal of Statistics Education (JSE) paper can be found [here](https://github.com/rudeboybert/JSE_OkCupid).
-   Permission to use this data set was explicitly granted by OkCupid.
-   Usernames are not included.

Installation
------------

COMING SOON: Get the released version from CRAN:

``` r
install.packages("okcupiddata")
```

Or the development version from GitHub:

``` r
# If you haven't installed devtools yet, do so:
# install.packages("devtools")
devtools::install_github("rudeboybert/okcupiddata")
```

Data Sets
---------

To load the data, run:

``` r
data("profiles")
```

If you prefer having the raw and uncleaned profile data along with the complete essay data (as seen in the above mentioned JSE paper), then you do not need this package; simply run the following code:

``` r
# You only need to run the following once:
url <- "https://github.com/rudeboybert/JSE_OkCupid/blob/master/profiles.csv.zip?raw=true"
temp_zip_file <- tempfile()
download.file(url, temp_zip_file)
unzip(temp_zip_file, "profiles.csv")
# Run this to load CSV into R:
profiles <- read.csv(file="profiles.csv", header=TRUE, stringsAsFactors = FALSE)
```
