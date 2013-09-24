
========================================================

Exercises on Functions

These are functions that are not really of much use, but give you some practice in writing functions.

Sums of numbers

Write the following functions and, for each one, show that your function produces the correct answer.

How many are odd

Many operators work in a natural way on arrays. An example is %% which will calculate the remainder of division. For instance,

x <- 1:9
x %% 2 # also gives an array
## [1] 1 0 1 0 1 0 1 0 1
sum(x%%2)
## [1] 5
Write a function countOdds() that takes an array of numbers as an input and returns the number of odd ones. Make sure to use the name countOdds for your function.

# Your function here
It should work like this:

countOdds( 1:9 )
## [1] 5
countOdds(c(3,5,7))
## [1] 3
countOdds(c(3,5,7,6,2,0))
## [1] 3
How many are even

Write a function countEvens() that takes an array of numbers as the input and returns the number of even numbers. One algorithm is to figure out how many odds there are, and subtract that from the count of numbers. A third algorithm involves comparing x%%2 to a different number, e.g. x%%2 == 0. Still another algorithm builds on changing x (Hint: Look at (1+x)%%2 and at 1+x%%2.) Do what you like.

# Your function here
Test your function to demonstrate that it works

Triangles.

Pythagoras

Write a function hypotenuseLength() that takes two arguments, a and b specifying the length of the sides of a right triangle. Return the length of the hypotenuse of the triangle. Use the Pythagorean Theorem!

# Your function here
Test your function to make sure it satisfies the following tests:

hypotenuseLength(3,4)
## [1] 5
hypotenuseLength(13,84)
## [1] 85
Law of Cosines

The law of cosines is a generalization of the Pythagorean Theorem. It says that the length of the third size of a triangle is a function of the lengths of the other two sides a and b and the angle between them θ.
c2=a2+b2−2abcos(θ)
You can use the R cos() function which, like the software in most scientific packages, takes θ in radians.

Write a function lawOfCosines() that takes three arguments, a, b, and theta and returns the length of side c.

# Your function here
A partial test of your function is whether it works for a right triangle and for a triangle that's collapsed to a line:

lawOfCosines(13,84,pi/2) # right triangle
## [1] 85
lawOfCosines(13,84,0) # collapsed with theta=0
## [1] 71
You can also test it partially with an equilateral triangle:

lawOfCosines(5,5,pi/3)
## [1] 5
Find the angle

With paper and pencil, solve the law of cosines for the angle θ in terms of a, b, and c. It's pretty easy. Use your solution to implement a function thetaFromLengths() that takes three arguments, a, b and c and returns the corresponding θ. (Hint: there is an R function acos() that gives the inverse cosine (a.k.a. “arccos” or cos−1.)

# Your function here
Test it on some inputs for which you know the answer, e.g.

thetaFromLengths(3,4,5) # should be pi/2
## [1] 1.571
Test thetaFromLengths()

Now that you have both lawOfCosines() and thetaFromLengths(), write a function called thetaFromLengthsTest() that takes a, b and theta as arguments, computes c using your lawOfCosines(), then compares the result of thetaFromLengths(a,b,c) to theta, returning the difference between them.

# Your function here
Graphics

Write a function canvas() that takes a vector of two numbers to draw a blank canvas on that scale. Your canvas() function can be written using the built-in plot(). A description of some plotting arguments is here.

# Your function here
Write a function drawCircle() that takes a center and radius and a color and adds the filled circle to the current canvas. Use border=NULL as a default argument.

# Your function here
Modify drawCircle() so that it takes ... as an argument and passes this on to the basic drawing commands (e.g., polygon()). That way you can “automatically” use all the optional arguments to polygon() like border width, color, etc.

# Your modified function here
Draw some overlaping circles.

# Your drawing here
Draw the Olympic logo.

# Your commands for drawing the Olympic logo
