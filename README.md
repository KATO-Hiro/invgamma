<!-- README.md is generated from README.Rmd. Please edit that file -->
**invgamma**
============

``` r
library(invgamma)
s <- seq(0, 5, .01)
plot(s, dinvgamma(s, 7, 10), type = 'l')
```

![](figures/README-unnamed-chunk-2-1.png)

``` r
f <- function(x) dinvgamma(x, 7, 10)
q <- 2
integrate(f, 0, q)
#> 0.7621835 with absolute error < 7.3e-05
(p <- pinvgamma(q, 7, 10))
#> [1] 0.7621835
qinvgamma(p, 7, 10) # = q
#> [1] 2
mean(rinvgamma(1e5, 7, 10) <= 2)
#> [1] 0.76168
```

Installation
------------

``` r
# install.packages("devtools")
devtools::install_github("dkahle/invgamma")
```
