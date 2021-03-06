
<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Build Status](https://travis-ci.org/vincenzocoia/powers.svg?branch=master)](https://travis-ci.org/vincenzocoia/powers)

**Note**: This R package is not mean to be "serious". It's just for teaching purposes. The original package is from <https://github.com/vincenzocoia/powers>. I have modified it for my homework.

powers
======

This is an R package that gives `sqrt()` friends by providing other power functions. With Alvin's version, you also get some new logarithm functions with different bases.

Installation
------------

You can install Alvin's version of powers from github with:

``` r
# install.packages("devtools")
devtools::install_github("STAT545-UBC-students/hw07-alvin-q/powers")
```

Example
-------

See the vignette for more extensive use, but here's an example:

``` r
powers::reciprocal(2)
#> [1] 0.5
```

As my homework expansion, I've added logarithm functions. More can be fouund in the vignettes, but here is an example:

``` r
powers::log3(1:10)
#>  [1] 0.0000000 0.6309298 1.0000000 1.2618595 1.4649735 1.6309298 1.7712437
#>  [8] 1.8927893 2.0000000 2.0959033
powers::log5(25)
#> [1] 2
```

For Developers
--------------

(Again, I don't actually intend for anyone to develop this silly package, but if I did, here's what I'd write.)

Use the internal `pow` function as the machinery for the front-end functions such as `square`, `cube`, and `reciprocal`.
