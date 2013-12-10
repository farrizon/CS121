HuckFinn/ToolTips
========================================================


```r
formatWord <- function(word, trans, class1) {
    if (is.na(trans)) 
        return(word)
    ans1 <- paste("<span class='", class1, "' ", sep = "")
    ans2 <- paste(ans1, "title='", trans, "'>", sep = "")
    ans3 <- paste(ans2, word, "</span>", sep = "")
    return(ans3)
}

cat(formatWord("Hello", "hi there!", class = "hiword"))
```

```
## <span class='hiword' title='hi there!'>Hello</span>
```


