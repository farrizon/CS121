Circles and Squares In-Class Activity
===============================================


```r

plot(1:2, type = "n", xlim = c(0, 100), ylim = c(0, 100), xaxt = "n", yaxt = "n", 
    xlab = "", ylab = "")

drawEllipse <- function(x, y, r) {
    angs <- seq(0, 2 * pi, length = 400)
    xpts <- x + r * cos(angs)
    ypts <- y + 25 * sin(angs)
    polygon(xpts, ypts, col = "purple", density = 80)
}
drawEllipse(25, 63, 15)

drawCircle <- function(x, y, r) {
    angs <- seq(0, 2 * pi, length = 400)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, col = "light blue", density = 80)
}
drawCircle(46, 48, 21)


polygon(c(27, 40, 40, 27), c(19, 19, 32, 32), col = "red", density = 80)

polygon(c(19, 41, 41, 19), c(38, 38, 63, 63), col = "Blue", density = 80)

polygon(c(20, 40, 40, 20), c(39, 39, 62, 62), col = "Green", density = 80)

polygon(c(57, 73, 77, 65, 53), c(43, 43, 60, 69, 60), col = "yellow", border = NA, 
    density = 80)
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 





