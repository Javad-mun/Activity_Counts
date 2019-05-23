
<!-- README.md is generated from README.Rmd. Please edit that file -->

# activityCounts

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/walkabillylab/activityCounts.svg?branch=master)](https://travis-ci.org/walkabillylab/activityCounts)
<!-- badges: end -->

The goal of activityCounts is to calculate ActiLife counts based on the
raw acceleration data.

## Installation

You can install the development version from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("walkabillylab/activityCounts")
```

## How to use

### import the accelerometer data

Note that your dataset should contain three columns. First column is the
raw accelerometer data in X direction and the second and the third
columns are raw accelerometer data in Y and Z directions respectively.
There is sample dataset available with this package which you can check
to make sure your data format is correct. to see the sample dataset run:

``` r
library(activityCounts)
View(sampleXYZ)
```

To calculate counts for your data, use the counts() function. Here is an
example of using the counts() function. We use sampleXYZ dataset
included in the package and then call the counts() function. The
sampling frequency of our data is 100 Hz so we need to pass this value
when calling the fucntion counts:

``` r
calculated_output <- counts(data = sampleXYZ,hertz = 100)
```

To verify the accuracy of the calculated counts for this particular
dataset,we can compare them with the provided sampleCounts dataset. It
contains counts calculated by ActiLife software and the counts()
function.

For more information, visit the [GitHub
repo](https://github.com/walkabillylab/activityCounts), and to see the
package help page use:

``` r
?activityCounts
```
