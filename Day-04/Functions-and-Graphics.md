Functions and Graphics 
========================================================


```r
countOdds <- function(x) {
    k <- 0
    for (n in x) {
        if (n%%2 == 1) 
            k <- k + 1
    }
    return(k)
}
countOdds(1:9)
```

```
## [1] 5
```

```r
countOdds(c(3, 5, 7))
```

```
## [1] 3
```

```r
countOdds(c(3, 5, 7, 6, 2, 0))
```

```
## [1] 3
```



```r
countEvens <- function(x) {
    k <- 0
    for (n in x) {
        if (n%%2 == 0) 
            k <- k + 1
    }
    return(k)
}
countEvens(1:10)
```

```
## [1] 5
```


```r
hypotenuseLength <- function(x, y) {
    h <- (x^2 + y^2)
    return(h)
}
hypotenuseLength(3, 4)
```

```
## [1] 25
```

```r
hypotenuseLength(13, 84)
```

```
## [1] 7225
```



```r
lawOfCosines <- function(a, b, theta) {
    x <- a^2 + b^2 - 2 * a * b * cos(theta)
    y <- sqrt(x)
    return(y)
}
lawOfCosines(13, 84, pi/2)
```

```
## [1] 85
```

```r
lawOfCosines(13, 84, 0)
```

```
## [1] 71
```

```r
lawOfCosines(5, 5, pi/3)
```

```
## [1] 5
```




```r
theatFromLengths <- function(a, b, c) {
    x <- c^2 - a^2 - b^2
    y <- x/(-2 * a * b)
    z <- acos(y)
    return(z)
}
theatFromLengths(3, 4, 5)
```

```
## [1] 1.571
```



```r
thetaFromLengthsTest <- function(a, b, theta) {
    x <- a^2 + b^2
    y <- -2 * a * b * cos(theta)
    h <- sqrt(x - y)
    q <- h^2 - a^2 - b^2
    w <- q/(-2 * a * b)
    e <- acos(y)
    u <- e - theta
    return(u)
}
thetaFromLengthsTest(13, 84, pi/2)
```

```
## [1] 1.339e-13
```




