String Transform
========================================================

# Reverser

```r
reverser <- function(x) {
    newFunc = strsplit(x, split = "")
    ans = newFunc[[1]][1:nchar(x)]
    return(rev(ans))
}
reverser("fabian")
```

```
## [1] "n" "a" "i" "b" "a" "f"
```


# Scrambler

```r
scrambler <- function(x) {
    newFunc = strsplit(x, split = "")
    ans = newFunc[[1]][1:nchar(x)]
    return(sample(ans))
}
scrambler("macalester")
```

```
##  [1] "t" "s" "e" "l" "a" "r" "a" "m" "c" "e"
```


# Vowel Bleeper

```r
vowelsOut <- function(x) {
    ans = gsub("[aeiou]", "*", x)
    return(ans)
}
vowelsOut("supercalafragalisticexpialadoshus")
```

```
## [1] "s*p*rc*l*fr*g*l*st*c*xp**l*d*sh*s"
```


# L33t


```r
L33t <- function(x) {
    newFunc = gsub("e", "3", x)
    newFunc1 = gsub("o", "0", newFunc)
    newFunc2 = gsub("s", "5", newFunc1)
    newFunc3 = gsub("g", "9", newFunc2)
    
    return(newFunc3)
}
L33t("geography")
```

```
## [1] "9309raphy"
```


# Sets of Words 


```r
x <- c("good", "sour", "hello")
sapply(x, FUN = L33t)
```

```
##    good    sour   hello 
##  "900d"  "50ur" "h3ll0"
```



```r
L33tApply <- function(x) {
    sapply(x, FUN = L33t)
}
L33t(c("good", "sour"))
```

```
## [1] "900d" "50ur"
```



```r
x <- c("fabian", "kaplan")
sapply(x, FUN = vowelsOut)
```

```
##   fabian   kaplan 
## "f*b**n" "k*pl*n"
```

```r

L33t <- function(input) {
    sapply(input, FUN = vowelsOut)
}

L33t(c("fabian", "kaplan"))
```

```
##   fabian   kaplan 
## "f*b**n" "k*pl*n"
```



