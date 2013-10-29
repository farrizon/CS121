Interactig With Loops
========================================================


```r
blastoffFor <- function(time) {
    for (k in length(time):1) cat(k, "")
    Sys.sleep(1)
    k <- k - 1
    
    Sys.sleep(1)
    cat("Blastoff!")
}
blastoffFor(5)
```

```
## 1 Blastoff!
```



```r
blastoffWhile <- function(time) {
    while (time != 0) {
        Sys.sleep(1)
        cat(time, "")
        time <- time - 1
    }
    Sys.sleep(1)
    cat("Blastoff!")
}
blastoffWhile(5)
```

```
## 5 4 3 2 1 Blastoff!
```



```r
blastoffRepeat <- function(time) {
    
    repeat {
        cat(time, " ")
        Sys.sleep(1)
        time <- time - 1
        if (time < 1) 
            break
    }
    
    Sys.sleep(1)
    cat("Blastoff!")
}
blastoffRepeat(5)
```

```
## 5  4  3  2  1  Blastoff!
```


