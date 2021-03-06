Numbers-and-Strings 
========================================================


```r
outliers <- function(x) {
    a <- quantile(x)[2]
    b <- quantile(x)[4]
    as.logical(x < a | x > b)
    
}
outliers(1:10)
```

```
##  [1]  TRUE  TRUE  TRUE FALSE FALSE FALSE FALSE  TRUE  TRUE  TRUE
```



```r
EnglishNumbers <- c("zero", "one", "two", "three", "four")
numToText <- function(num, lang) {
    ans <- lang[num + 1]
    return(ans)
}
numToText(2, EnglishNumbers)
```

```
## [1] "two"
```



```r
EnglishNumbers <- c("zero", "one", "two", "three", "four")
TextToNum <- function(word, lang) {
    ans = which(lang == word)
    return(ans - 1)
}
TextToNum("three", EnglishNumbers)
```

```
## [1] 3
```



```r
digitToWord <- function(integer, language) {
    if (language == "English") {
        if (integer == "0") 
            print("zero")
        if (integer == "1") 
            print("one")
        if (integer == "2") 
            print("two")
        if (integer == "3") 
            print("three")
        if (integer == "4") 
            print("four")
        if (integer == "5") 
            print("five")
        if (integer == "6") 
            print("six")
        if (integer == "7") 
            print("seven")
        if (integer == "8") 
            print("eight")
        if (integer == "9") 
            print("nine")
    }
    if (language == "Spanish") {
        if (integer == "0") 
            print("cero")
        if (integer == "1") 
            print("uno")
        if (integer == "2") 
            print("dos")
        if (integer == "3") 
            print("tres")
        if (integer == "4") 
            print("cuatro")
        if (integer == "5") 
            print("cinco")
        if (integer == "6") 
            print("seis")
        if (integer == "7") 
            print("siete")
        if (integer == "8") 
            print("ocho")
        if (integer == "9") 
            print("nueve")
    }
    if (language == "French") {
        if (integer == "0") 
            print("zero")
        if (integer == "1") 
            print("un")
        if (integer == "2") 
            print("deux")
        if (integer == "3") 
            print("trois")
        if (integer == "4") 
            print("quatre")
        if (integer == "5") 
            print("cinq")
        if (integer == "6") 
            print("six")
        if (integer == "7") 
            print("sept")
        if (integer == "8") 
            print("huit")
        if (integer == "9") 
            print("neuf")
    }
}

digitToWord("1", "Spanish")
```

```
## [1] "uno"
```

```r

digitToWord("2", "English")
```

```
## [1] "two"
```

```r

digitToWord("3", "French")
```

```
## [1] "trois"
```



```r
lettersMatch <- function(words, pattern) {
    a = grep(pattern, words)
    return(a)
}
lettersMatch(c("apple", "berry", "carrie", "rr"), "rr")
```

```
## [1] 2 3 4
```



```r
piseries <- function(k) {
    signs <- -(-1)^c(1:k)
    num <- (seq(1, by = 2, length.out = k) * signs)^(-1)
    sum(4 * num)
    
}
piseries(101)
```

```
## [1] 3.151
```



```r
piseries <- function(k) {
    signs <- -(-1)^c(1:k)
    num <- (seq(1, by = 2, length.out = k) * signs)^(-1)
    sum(4 * num)
    
}
howClosetoPi <- function(n) {
    ests <- c()
    for (k in 1:n) {
        ests <- c(ests, piseries(k))
    }
    distancefrompi <- ests - pi
    plot(distancefrompi)
}
howClosetoPi(50)
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7.png) 



```r
randApproxtoPi <- function(n) {
    x <- runif(n)
    y <- runif(n)
    sd <- x^2 + y^2
    4 * (length(sd[sd < 1])/length(sd))
}
randApproxtoPi(1000)
```

```
## [1] 3.192
```



```r
approxes <- sapply(1:10000, randApproxtoPi)
plot(approxes, pch = 20, col = rgb(0, 0, 0, 0.4), log = "x")
lines(c(1, 10000), c(pi, pi), col = "green")
```

![plot of chunk unnamed-chunk-9](figure/unnamed-chunk-9.png) 

