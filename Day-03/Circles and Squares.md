Circles and Squares In-Class Activity
===============================================


```r

plot(1:2, type = "n", xlim = c(0, 100), ylim = c(0, 100), xaxt = "n", yaxt = "n", 
    xlab = "", ylab = "")
angle = seq(0, 2 * pi, length = 1000)
d = 45 + 20 * cos(angle)
f = 48 + 20 * sin(angle)
polygon(d, f, col = "skyblue", border = FALSE)
angle = seq(0, 2 * pi, length = 1000)
e = 27 + 13 * cos(angle)
g = 59 + 22 * sin(angle)
polygon(e, g, col = "pink", border = FALSE)
polygon(c(19, 41, 41, 19), c(38, 38, 63, 63), col = "Blue")
polygon(c(20, 40, 40, 20), c(39, 39, 62, 62), col = "Green")
polygon(c(27, 40, 40, 27), c(19, 19, 32, 32), col = "red")
polygon(c(57, 73, 77, 65, 53), c(43, 43, 60, 69, 60), col = "yellow", border = NA)
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 




