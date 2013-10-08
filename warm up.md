Warm Up 10-08-2013
========================================================


```r
mySum <- function(v) {
    sofar <- 0
    k <- 1
    repeat {
        sofar <- sofar + v[k]
        k <- k + 1
        if (k == (length(v) + 1)) 
            break
    }
    
    return(sofar)
}
mySum(1:10)
```

```
## [1] 55
```

