


```r

formatWord <- function(word, trans, class1) {
    if (is.na(trans)) 
        return(word)
    ans1 <- paste("<span class='", class1, "' ", sep = "")
    ans2 <- paste(ans1, "title='", trans, "'>", sep = "")
    ans3 <- paste(ans2, word, "</span>", sep = "")
    return(ans3)
}

cat(formatWord("Whats up", "hey!", class = "skyblue"))
```

<span class='skyblue' title='hey!'>Whats up</span>

```r

cat(formatWord("The weather", "in MN", class = "skyblue"), "is", "very", "cold", 
    "outside", formatWord("outside.", "-10", "hiword"))
```

<span class='skyblue' title='in MN'>The weather</span> is very cold outside <span class='hiword' title='-10'>outside.</span>




