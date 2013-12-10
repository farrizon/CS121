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
piSeries <- function(n) {
    k <- 1:n
    sum <- 4 * (1 - (1/k[3]))
    sum <- sum + (1/k[5])
    sum <- sum - (1/k[7])
    sum <- sum + (1/k[9])
    sum <- sum - (1/k[11])
    sum <- sum
    return(sum)
}
piSeries(4)
```

```
## [1] NA
```



```r
other <- function(n) {
    sum <- 0
    for (k in 1:n) {
        sum <- sum + ((-1)^k)
        if (k%%2 == 0) {
            k <- k + 1
        }
        return(sum)
    }
}
other(7)
```

```
## [1] -1
```



```r
howCloseToPi <- function(n) {
}
```

