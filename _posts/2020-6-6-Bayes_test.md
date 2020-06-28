Bayes test
================

``` r
library(bnlearn)
```

    ## 
    ## Attaching package: 'bnlearn'

    ## The following object is masked from 'package:stats':
    ## 
    ##     sigma

``` r
data(learning.test)
d<-learning.test
res = gs(learning.test)

plot(res)
```

![](2020-6-6-Bayes_test_files/figure-markdown_github/unnamed-chunk-1-1.png)

``` r
## highlight node B and related arcs.
plot(res, highlight = "B")
```

![](2020-6-6-Bayes_test_files/figure-markdown_github/unnamed-chunk-1-2.png)

``` r
## highlight B and its Markov blanket.
plot(res, highlight = c("B", mb(res, "B")))
```

![](2020-6-6-Bayes_test_files/figure-markdown_github/unnamed-chunk-1-3.png)
