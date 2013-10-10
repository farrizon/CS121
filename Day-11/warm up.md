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



```r
mySumWhile <- function(v) {
    sofar <- 0
    k <- 1
    while (k != (length(v) + 1)) {
        sofar <- sofar + v[k]
        k <- k + 1
    }
    return(sofar)
}



mySumWhile(1:10)
```

```
## [1] 55
```



```r
mySumfor <- function(v) {
    sofar <- 0
    k <- 1
    for (k in 1:length(v)) {
        sofar <- sofar + v[k]
    }
    return(sofar)
}


mySumfor(1:10)
```

```
## [1] 55
```



```r
myUnique <- function(v) {
    already <- c()
    for (k in v) {
        if (k %in% already) 
            already <- c(already, k)
    }
    return(already)
}
myUnique(c("dog", "ant", "bee", "cat", "dog"))
```

```
## NULL
```

