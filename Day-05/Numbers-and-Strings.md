Numbers-and-Strings 
========================================================

Basic Statistics

Suppose you have a group of numbers. An “outlier” from the group is a quantity that fall outside of the mainstream. One useful rule of thumb for defining an outlier is as a quantity that falls far below the 25th percentile or far above the 75th percentile. “Far” is often defined to be 1.5 times the interval between the 25th and 75th percentile.

Write a function outlier(x) whose argument x is a vector of numbers. Your function should return a vector of logicals indicating whether each number in x is an outlier with respect to all of x. You can use the built-in function quantile() to compute the 25th and 75th percentile, setting probs to 0.25 and 0.75 respectively.

Numbers and Languages

In class, you wrote digitToWord(v) that converted a numerical vector of small integers, 0 to 9, into the corresponding word for each digit. Now you are to expand your function so that it takes two arguments, a numerical vector of small integers and a character vector, and translates the numerical vector into the corresponding word from the character vector. Give demonstrations that translate small digits into English, French, Spanish, and, if you know how to generate the characters, Chinese and Russian. If you speak another language, add in that as an example.

Help for Crossword Puzzles

Write a function lettersMatch(words,pattern) that takes a vector of strings as the first argument and a single character string (to be pedantic, a vector of length 1) and returns all the strings that match the pattern. You will want to use grepl() and a “regular expression.” Here's some examples of grepl() at work.

small <- c("first", "second","errand","arrest","are")
grepl("^...$",small) # three letters long
## [1] FALSE FALSE FALSE FALSE  TRUE
grepl("^.rr",small) # second and third are the letter r
## [1] FALSE FALSE  TRUE  TRUE FALSE
Give a few crossword-puzzle type examples, e.g. five letter words with the first two letters “ag” and the fourth letter “r”, and show that your function works. You will, of course, need a reasonable size dictionary. For the present, I encourage you to create one collaboratively, at this collaborative editor.

Have your π two ways

One way: A Series

A formula for the numerical value of π is the infinite sum
π=4(11−13+15−17+19−111+⋯)
Write a function piSeries(n) that generates this sum for the first n terms. Hints: −1k will be positive when k is even and negative when k is odd. Use sum() to add up the numbers in a vector.

How close?

Now, write howCloseToPi(n) that generates the first n terms of the series and makes a plot of how far the result is from π (well, pi at least) as each consecutive term is added in. Hint: Use cumsum() rather than sum().

How many terms in the sum you would need to approximate π to three digits?
Estimate how many terms you would need to get π to 15 digits. (Don't try the calculation for 15 digits, just make an estimate.
Another way: A “Monte Carlo” Method

You can generate n uniformly distributed random numbers with a statement like this:

x <- runif(100)
If you generate both x and y coordinates this way, then compute the square distance from the origin, x2+y2, the fraction of points closer than square distance 1 to the origin will approximate π/4.

Write the function randomApproxToPi(n) that generates n coordinate pairs and returns the approximation to π. (Remember the 14.)

How Close?

Make a plot showing the scatter of the approximation for a range of n, like this: plot of chunk unnamed-chunk-4

Some hints: sapply(x, fun) will apply a function fun to each element of vector x and return a vector. This plot was made with arguments pch=20, col=rgb(0,0,0,.4), log="x". To generate the random n, in a way that will look nice on log axes, I used 10^runif(1000,min=2,max=6). I encourage you to test out your plot with many fewer than 1000 points at first. When you have it working, you can increase the number of points.
