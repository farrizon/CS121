Recursion 
========================================================



```r
addEm <- function(v) {
    sum <- 0
    for (k in 1:length(v)) {
        sum <- sum + v[k]
    }
    return(sum)
}
addEm(1:3)
```

```
## [1] 6
```



```r
newAddEm <- function(v) {
    if (length(v) == 0) 
        return(0)
    return(v[1] + newAddEm(v[-1]))
}
newAddEm(1:10)
```

```
## [1] 55
```



```r
addNSeqLoop <- function(n) {
    sum <- c()
    for (k in n:0) {
        sum <- c(sum, k)
        k <- k - 1
    }
    
    return(sum(sum))
}
addNSeqLoop(10)
```

```
## [1] 55
```




```r
addNSeqSimp <- function(n) {
    ans <- n + (n - 1) + (n - 2) + (n - 3) + (n - 4)
    return(ans)
}
addNSeqSimp(4)
```

```
## [1] 10
```



```r
addRecurSimp <- function(n) {
    ans <- n[1] + n[2] + n[3] + n[4] + n[5]
    return(ans)
}
addRecurSimp(c(1, 2, 3, 4, 5))
```

```
## [1] 15
```

