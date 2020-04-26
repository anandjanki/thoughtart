---
title: "Polynomial Construction"
date: 2020-04-25T10:33:45+05:30
draft: false
weight: 2
---

**EC Note** - This topic is not in the syllabus of IGCSE Additional Mathematics curriculum, its an ExtraCurricular topic. But is an interesting topic nevertheless that learners can explore if interested. 

While finding the roots of a polynomial is an involved activity, doing the opposite turns out to be fairly simple. If we are given the roots of a polynomial, can we construct the polynomial back from it?

To keep it simple, we will restrict ourselves to real rools, and in fact to polynomials for whome all the roots of the polynomial are real.

## Polynomial from its roots
Lets take an example. Suppose the roots of a degree-3 polynomial are known to be \\( -3, -1 \text{ and } 2\\). Can we find the polynomial?

The answer, as you may expect, is fairly simple except for a small catch. You may have guessed a degree-3 polynomial with roots as above as:
{{< katex >}}
\begin{array}{rclcl}
p(x) & = & (x + 3)(x+1)(x-2) \\
\end{array}
{{< /katex >}}

In fact, we can even plot the graph of this polynomial function to see how it looks. As expected, it would cut the x-axis at exactly \\( -3, -1 \text{ and } 2\\).

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/poly-from-roots.png" class="figs" title="The graph of a cubic polynomial function with the roots marked" >}}
<--->
{{< /columns >}}

But is this the only degree-3 polynomial with these 3 roots? Well yes, but only up to a scale factor. The picture below depicts a few other degree-3 polynomials that all have the same roots. Notice that they are all simply scaled versions of \\( p(x) \\) above.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/poly-from-roots-scale.png" class="figs" title="The graph of multiple cubic polynomial functions all with the same roots" >}}
<--->
{{< /columns >}}

### Roots and scale
Well, it should be fairly obvious (though we need to actually prove it) that if we are given the 3 roots of a degree-3 polynomial *and* the leading coefficient (the scale factor above), i.e. the coefficient of the term \\(x^3\\), then we can uniquely identify the cubic polynomial. For e.g., the degree-3 polynomial with roots \\( -3, -1 \text{ and } 2\\) and with leading coefficient as \\(2\\) is simply:
$$ p(x)  = 2(x + 3)(x+1)(x-2) $$

### Roots and a point
With a little stretch, we can note that the scale factor is only one way to pin down the polynomial. We could have well asked the following question - find a degree-3 polynomial whose roots are \\( -3, -1 \text{ and } 2\\) and which passes through the point \\( (1, 4) \\).

We can do this algebraically as follows:

The general form of degree-3 polynomials which have roots as \\( -3, -1 \text{ and } 2\\) can be written as:
$$ p(x) = k\cdot (x + 3)(x+1)(x-2) $$
where \\( k\in \R \\). Since the polynomial we are looking for also passes through the point \\( (1, 4) \\), i.e. \\( p(1) = 4 \\), we get 
{{< katex >}}
\begin{array}{rclcl}
p(1) & = & 4 \\
\therefore k\cdot (1 + 3)(1+1)(1-2) & = & 4 \\
\therefore k & = & 0.5 \\
\therefore p(x) & = & 0.5(x + 3)(x+1)(x-2) \\
\end{array}
{{< /katex >}}

We can also visualize this graphically:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/poly-with-roots-point.png" class="figs" title="The graph of a cubic polynomial functions given its roots and one other point" >}}
<--->
{{< /columns >}}

## Polynomial from points

It turns out we can generalize even further. The 3 roots are also really points on the polynomial above. Suppose we are given 4 random points. Can we find a polynomial that passes through these points? It turns out that the answer is yes.

Lets do this one step at a time.

First lets take degree-1 polynomials, in other words linear functions. Suppose we know just two points on this function, can we determine the function and the value that it takes on any other point? We know this answer is yes, because graphically, we can draw one and only one line through two distinct points on a plane.

What about degree-2 polynomials? What if we have 2 points on a plane, can we draw a quadratic function passing through these points? Will there be only 1 quadratic, will there be many functions?

To answer that question, lets first answer a simpler one. 

### Linear functions one point
Suppose we are given only one point, let say \\( (1, 5) \\). Can we find a line passing through this point? Can we find a degree-1 polynomial or a linear function such that the value of this function at \\( x= 1\\) is \\( y = 5\\).

We can do this algebraically as follows. Consider a general linear function:
$$ p(x) = ax + b $$
Since the graph of this function passes through the point \\( (1,5) \\), we know that:

{{< katex >}}
\begin{array}{rcl}
5 & = & a\cdot 1 + b \\
\therefore b & = & 5 - a \\
\therefore p(x) & = & ax + 5 - a \\
\end{array}
{{< /katex >}}

A linear function that passes through the point \\( (1, 5) \\) has the above form. And vice-versa, any linear function of this form passes through the point \\( (1, 5) \\).

Indeed, if we say \\( a = 1\\), we get a linear function \\( y = x + 4 \\) that passes through \\( (1,5) \\). If we take \\( a = -6\\), we get another linear function \\( y = -6x + 11 \\) which also passes through this point.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/lines-through-point.png" class="figs" title="Linear functions given one known point - two functions which pass through the point, and one function that does not pass through it." >}}
<--->
{{< /columns >}}

And if we take some other linear function which is not in the above form, for e.g., \\( y = x + 2 \\), then we can see that this function does not pass through this point \\( (1, 5) \\).

### Quadratic with two points

We can do the exact same algebraic technique if we are given two points and we have to find a quadratic function passing through these two points.

Again lets do this with an example. Suppose we are given two points \\( (1, 5) \\) and \\( (4, 9) \\). Can we find a quadratic function passing through these two points?

We start with a general quadratic function:
$$ p(x) = ax^2 + bx + c $$

Since the graph of this function passes through the point \\( (1, 5) \\) and \\( (4, 9) \\), we know that:
{{< katex >}}
\begin{array}{rcl}
5 & = & a\cdot 1^2 + b\cdot 1 + c, \text{    and} \\
9 & = & a\cdot 4^2 + b\cdot 4 + c \\
\end{array}
{{< /katex >}}
We can consider these as simultaneous equations and solve for \\(b\\) and \\(c\\) in terms of \\(a\\).
{{< katex >}}
\begin{array}{rcl}
\therefore b & = & \displaystyle \frac{4 - 15a}{3} , \text{ and }\\ \\
c & = & \displaystyle \frac{12a + 11}{3} \\ \\
\therefore p(x) & = & ax^2 + (\displaystyle \frac{4 - 15a}{3})x + (\displaystyle \frac{12a + 11}{3})
\end{array}
{{< /katex >}}

As before, take different values of \\(a\\) and you will see that you get different quadratic equations. But all of them will pass through the points \\( (1, 5) \\) and \\( (4, 9) \\). We can visualize this as an animated graphic [here](https://www.geogebra.org/graphing/ghzhczfx).

### Quadratic with three points

Suppose we want to find the quadratic function that passes through three distinct points, any random three points, lets say \\( (1, 5) \\), \\( (4, 9) \\) and \\( (10, 3) \\).

As before, we start with a generic quadratic equation, and plug in these values:
{{< katex >}}
\begin{array}{rcl}
\text{Let } p(x) & = & a\cdot x^2 + b\cdot x + c \\ \\
5 & = & a\cdot 1^2 + b\cdot 1 + c \\
9 & = & a\cdot 4^2 + b\cdot 4 + c \\
3 & = & a\cdot 10^2 + b\cdot 10 + c \\
\end{array}
{{< /katex >}}

We have to carefully solve these three simultaneous equations to find the values of \\( a\\), \\(b\\) and \\(c\\). And it will turn out that the quadratic function is as follows:

$$ p(x) = -0.26x^2 + 2.63x + 2.63 $$

This is depicted graphically [here](https://www.geogebra.org/graphing/nqwnsydd). You can also change the points here, and each time you change the points, you will automatically get a new quadratic function that passes through these points.

(The way to easily find the solution in general uses ideas from a topic of mathematics called matrices. But we will skip that here.)

**Q1.** Under certain conditions, if the three points have certain peculiar placement, then it will NOT be possible to find a quadratic function that passes through the three points. Note that we said that the 3 points must be distinct, so we can ignore the case where we repeat the same point. Can you guess from the definition of functions, what that condition is? You can also check out by interacting with the GeoGebra graph here and playing with the points to find out the condition.

{{< expand "Solution" >}}
If any two points have the same value of \\( x\\) and different values for the \\(y\\) coordinate, then by definition it is not possible to find a function, because functions cannot be 1-to-many.
{{< /expand >}}

### General Rule

Based on what we have seen above, we can generalize to higher degree polynomials as well. In general, if we have \\( (n + 1) \\) points on a plane (as before, no two points should have the same x-value), then we can find a *unique* polynomial of degree \\(n\\) that passes through these points.

This is also known as polynomial interpolation and has great utility in modeling systems. A fun problem based on this idea is as follows:

**Q2.** Suppose I give all of you a secret code, essentially a number. And I keep a secret code with myself. The secret code that I have is the password to my secret account with my secret treasure (lets say a secret stash of finest chocolates.. :). You guys are sworn to not share your secret with each other. 

I have also given you a small device into which if you enter your code, it will give you the password to my secret account. However, the device has been coded such that at least 4 out of the 5 of you need to enter your codes to get the correct password. If only 2 of you enter your codes, or only 3 of you enter your codes, then the device will NOT provide the correct password. But if at least 4 of you enter your codes, then the device WILL provide you the correct code to my account. This is to ensure that majority of you come together to share the secret stash of chocolates :)

How do you think I have setup the code to my account??

{{< expand "Hint" >}}
I have come up with a function and coded it into the device. Lets say the secret password is the value of the function at \\(x = 0\\). Each of you has the value of the function at different x values, lets say student #1 has the value of the function at \\( x = 1 \\) and so on. When you enter your code into the device, you enter your number, say #1, as well as the code I gave you.

What function is such that if 2 of you enter your codes, the device cannot find my code. If 3 of you enter your codes, the device cannot find my code. But if 4 of you enter your codes, then the device can find my code, which is simply \\(f(0) \\).
{{< /expand >}}

{{< expand "Answer" "..." >}}
Since 4 of you are needed to find the underlying function, and hence my code, I will take a degree-3 polynomial.

Suppose I choose the function \\(f(x) = 123x^3 - 256x^2 + 34x + 7329 \\).

I give student #1 the code \\( f(1) = 7230 \\), I give student #2 the code \\( f(2) = 7357 \\) amd so on, I give student #5 the code \\( f(5) = 16474 \\).

When any 4 of you enter your codes, the device can uniquely find the degree-3 polynomial and hence also find \\( f(0) \\).

Apparently, this was used in the World War to protect critical weapons and stuff, and only if a pre-defined number of generals got together, would it be possible to get the code. If one or two generals were compromised and their codes stolen from them, that would still not provide access to the secret stash!!
{{< /expand >}}

### Bezier Curves

This idea also finds application in drawing software. To find a polynomial of degree-3, we saw that we need to specify 4 points on the curve. Another way to look at this is that we are simply constraining the freedom of the function by adding additional points. If we specify only 1 point there are a number of cubic functions that can pass through the point. If we specific 2 points, or 3 points the number of cubics that can pass through it gets further limited. Finally, if we specify 4 points, we get a unique cubic function.

It turns out that we can provide these constraints in other ways as well. That is the idea behind what are called Bezier curves. 

{{< columns "20,60,20" >}}
<--->
<p><a href="https://commons.wikimedia.org/wiki/File:B%C3%A9zier_3_big.gif#/media/File:Bézier_3_big.gif"><img src="https://upload.wikimedia.org/wikipedia/commons/d/db/B%C3%A9zier_3_big.gif" alt="Bézier 3 big.gif"></a><br>By Phil Tregoning - Created using ImageMagick, Public Domain, <a href="https://commons.wikimedia.org/w/index.php?curid=1727380">Link</a></p>
<--->
{{< /columns >}}

The 4 points \\( P_0, \ldots P_3\\) are fixed, and as the green points move on the lines joining these points, and the blue points move on the green lines, and the black point moves on the blue line, it traces a unique cubic equation governed by these points and the constraints they impose. This comes in handly while creating the design of say a new model of a car in a graphics software to draw the smooth curves that you want the car's design to have. That is the application that the French engineer Pierre Bézier had when he came up with these.
