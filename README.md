##### Installation instructions
* Install R (see http://cran.fhcrc.org)
* Open R and install and load both the devtools and mes libraries by typing the following:
```r
install.packages('devtools',repos='http://cran.us.r-project.org')
library(devtools)
install_github('mercaldo/mes')
library(mes)
```
##### Example
```r
set.seed(1) 
dat <- rpois(1000, lambda=1)
table(dat)
```
Suppose it is of interest to obtain an MES sample of size 50
```r
(out <- mes(dat, N=50, seed=1, ix=TRUE))
```
| strata | freq | mes  |
| -------|:----:| ----:|
| 0      | 364  | 10   |
| 1      | 378  | 10   |
| 2      | 164  | 9    |
| 3      | 72   | 10   |
| 4      | 20   | 9    |
| 6      | 1    | 1    |
| 7      | 1    | 1    |
