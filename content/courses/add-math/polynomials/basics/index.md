---
title: "Basics"
date: 2020-04-18T21:49:46+05:30
draft: false
weight: 1
---

We have looked at linear functions, \\( f(x) = ax + b \\), quadratic functions of the form \\( f(x) = ax^2 + bx + c \\), and even cubic functions of the form \\( f(x) = ax^3 + bx^2 + cx + d \\). All these functions belong to a class of functions commonly known as polynomials. It should be easy to guess that a *quartic function* would follow the cubic function in the same pattern. 

These are all listed below:

{{< katex >}}
\begin{array}{rclcl}
\text{Linear} & : & f(x) = ax + b \\
\text{Quadratic} & : & f(x) = ax^2 + bx + c \\
\text{Cubic} & : & f(x) = ax^3 + bx^2 + cx + d \\
\text{Quartic} & : & f(x) = ax^4 + bx^3 + cx^2 + dx + e \\
\end{array}
{{< /katex >}}

To generalize these kinds of function, we notice that using \\( a, b, c\ldots \\) for the coefficients gets cumbersome. So, we switch over to numbered coefficients to have the following definition.

## Definition

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A polynomial function (simply called a **polynomial**) is a function of the form:

{{< katex >}} p(x) = a_n\cdot x^n + a_{n-1}\cdot x^{n-1} + \cdots + a_1\cdot x + a_0 {{< /katex >}}

where: 

- \\(n \\) is a whole number, 
- the domain of the function is \\( \R \\) (which means \\( x\\) takes real values),
- the coefficients are fixed real numbers, i.e. \\(a_i \in \R, i = 0, 1, 2, \ldots, n \\), with at least \\( a_n \ne 0 \\),
- the co-domain of the function therefore is also \\( \R \\) (which means \\(p(x)\\) takes real values).

{{< /highlight-box >}}

It may be noted that we have intently defined a polynomial with a single variable \\( x\\) for our purposes, these are called univariate polynomials, a more general definition would be multivariate polynomials, for e.g., \\( f(x,y) = x^3 + xy^2 + 4xy + 10 \\).

It may also be noted that we have intently defined the coefficients to be real numbers, a more general definition would have allowed for complex numbers as coefficients. We could also define polynomials where we allow only for say rational coefficients, or say only the set of integers \\( {0, 1, 2, \ldots, 9} \\) which are all the remainders upon division by 10, but we stick to real numbers for our purposes.

Finally, it may also be noted that we have intently defined the domain to be real numbers, a more general definition would have allowed for complex numbers as the domain for the function.

We can now re-write the list of functions we had earlier as follows:

{{< katex >}}
\begin{array}{rclcl}
\text{Constant} & : & f(x) = a_0 \\
\text{Linear} & : & f(x) = a_0 + a_1x \\
\text{Quadratic} & : & f(x) = a_0 + a_1x + a_2x^2 \\
\text{Cubic} & : & f(x) = a_0 + a_1x + a_2x^2 + a_3x^3 \\
\text{Quartic} & : & f(x) = a_0 + a_1x + a_2x^2 + a_3x^3 + a_4x^4 \\
\end{array}
{{< /katex >}}

Note that we have also used the general definition to say that a *constant function* also falls in the same category.

## Degree and Roots

Another definition, rather terminology, used very commonly with polynomials is the following:
{{< highlight-box "Defn 2:" "none" "" "part" >}}
The **degree** of a polynomial is the highest index of the variable \\( x\\) in the polynomial.
{{< /highlight-box >}}

Thus, the degree of a cubic polynomial, \\( f(x) = a_0 + a_1x + a_2x^2 + a_3x^3 \\), is obviously \\(3\\). Note that the degree of the constant polynomial is \\(0\\).

Since a polynomial is also a function, the roots of a polynomial has the same meaning as the roots of a function. A root of a polynomial (also called zero of the function) is a member \\( x\\) of the domain where the polynomial vanishes. 

For e.g., for a given polynomial, say \\( p(x) = x^3 - 1.25x^2 - 4.135x + 4.73 \\), if we know that say \\( p(2.15) = 0 \\), then \\( 2.15 \\) is called a root of the polynomial. You can also check that this polynomial has two more roots, \\( p(1.1) = 0\\) and \\( p(-2) = 0 \\), hence \\( 1.1 \\) and \\( -2\\) are also roots of the polynomial.

As for any other function, we can draw the graph of this polynomial function as shown below.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/Polynomial graph v3.png" class="figs" title="The graph of a cubic polynomial function with the roots marked" >}}
<--->
{{< /columns >}}

### Graphs of polynomials
There is a very interesting relationship between the degree of a polynomial and the number of roots it has. To see this, first lets visualize the graphs of a few example polynomials of different degrees.

{{< columns >}}
{{< figure src="images/pg0.png" class="figs" title="Polynomial of degree 0: f(x) = 2" >}}
{{< figure src="images/pg2.png" class="figs" title="" >}}
{{< figure src="images/pg4.png" class="figs" title="" >}}
{{< figure src="images/pg6.png" class="figs" title="" >}}
<--->
{{< figure src="images/pg1.png" class="figs" title="Polynomial of degree 1: f(x) = 4x - 3" >}}
{{< figure src="images/pg3.png" class="figs" title="" >}}
{{< figure src="images/pg5.png" class="figs" title="" >}}
{{< figure src="images/pg7.png" class="figs" title="" >}}
{{< /columns >}}

Next, lets count the number of roots for each of the polynomials above. The polynomial of degeee 0 has 0 roots, the polynomial of degree 1 has 1 root, the polynomial of degree 2 has 2 roots, the polynomial of degree 3 has 3 roots, and so on. If you are a little hasty, you may jump to the conlusion that the number of roots of a polynomial is the same as the degree of the polynomial. But that would not be the case.

Look carefully at the polynomial of degree 5 above. It does not have 5 roots, in fact it seems to have 3 roots only. The graph of this polynomial is plotted again below as \\( p_1(x)\\), but plotted alongside are two other polynomials which are just shifted up / down from this polynomial.
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/pg5-1-3-5-roots.png" class="figs" title="Polynomials of degree 5 - one with 1 root, another with 3 roots and a third one with 5 roots" >}}
<--->
{{< /columns >}}

Notice how the polynomial \\( p_1(x)\\) has 3 roots as was also seen before. The other polynomial \\( p_2(x) \\) which is plotted in blue and is just \\( p_1\\) shifted up by 3, i.e. \\( p_2(x) = p_1(x) + 3 \\) has only 1 root. The third polynomial \\( p_3(x) \\) which is plotted in green and is just \\( p_1\\) shifted down by 3, i.e. \\( p_2(x) = p_1(x) - 3 \\) and has 5 roots.

### Repeated Roots

Before we proceed further, it is important to note that a polynomial may have repeated roots. It is of course not necessary that all the roots of a polynomial should be distinct.

For e.g., the polynomial \\( f(x) = x^2 \\) has two real roots, but both the roots are the same, namely \\( x = 0\\), i.e., the polynomial has one repeated root, and this root itself is repeated twice.

Shown below are examples of a few polynomials, all of degree 5, with repeated roots.

{{< columns >}}
{{< figure src="images/p5-5c.png" class="figs" title="" >}}
$$ \text{1 repeated root, repeated 5 times} $$
{{< figure src="images/p5-3c.png" class="figs" title="" >}}
$$ \text{1 repeated root, repeated 3 times} $$
{{< figure src="images/p5-2c.png" class="figs" title="" >}}
$$ \text{1 repeated root, repeated 2 times} $$
<--->
{{< figure src="images/p5-4c.png" class="figs" title="" >}}
$$ \text{1 repeated root, repeated 4 times} $$
{{< figure src="images/p5-3-2c.png" class="figs" title="" >}}
$$ \text{2 repeated roots, one 3 times, one 2 times} $$
{{< figure src="images/p5-2-2c.png" class="figs" title="" >}}
$$ \text{2 repeated root, each repeated 2 times} $$
{{< /columns >}}

### End Behavior

In order to understand these graphs better, we need to look into what is called the end behavior of these polynomial functions.

End behavior simply means the sign of the function (whether it is positive or negative) when the x-value is at extremes ends of the domain. Since the domain of our polynomial functions is \\( \R \\), end behavior means the sign that the function has when \\( x \to +\infty \\) and when \\( x \to -\infty \\).

Lets take a few examples to understand this better:

- Consider a polynomial function with an even degree, say \\( y = x^2 \\). When \\( x \to +\infty \\), clearly y also becomes very large and importantly \\( y > 0 \\). Likewise, when \\( x \to -\infty \\), y again becomes very large and interestingly, stays positive, as \\( x \to -\infty, y > 0 \\).
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/q-large-3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

- You may say, lets add a negative value to the function, lets consider \\( y = x^2 - 10000 \\).  For small values of \\( x\\), in and around \\( x = 0\\), the function is indeed negative. For e.g., \\( f(10) = 10^2 - 10000 = -9900 \\), and \\( f(-20) = (-20)^2 - 10000 = -9600\\). But if we take a large enough value of \\(x\\), say \\( x = 400 \\) or \\( x = -300 \\), it is easy to see that the value of the function is positive.
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/q-large-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}


- You may say next, lets add more negativity to the function, lets consider \\( y = x^2 - 1,000,000x - 200,000,000,000 \\). But it doesnt matter. Of course, for small value of \\(x\\), the function would be negative. But if we take very large values of \\(x\\), say \\( x = 10,000,000 \\) or \\( x = -10,000,000 \\), the function remains positive.
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/q-large-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

In summary, the insight we get from these graphs is that it does not matter what the smaller terms of the polynomial are, the highest degree term dominates the sign of the function at very large values of x.

In all of the above, we have considered the highest degree term with a positive sign. If we were to consider the function \\( y = -x^2 \\), then, we can easily see that when \\( x \to \infty \\), then the function is negative, and likewise when \\( x \to -\infty \\).

This property also holds no matter what the degree of the polynomial. So, if we consider a polynomial of degree 3, a cubic polynomial, the same would hold true. The highest degree term would control the sign of the function at extreme values of x.

Polynomial functions with an odd degree behave slightly differently from even functions though in the following manner. For an odd degree polynomial, for e.g. say, \\( y = x^3 - 10x^2 - 100x - 1000 \\), for a large positive value of \\( x \\), say \\( x = 100 \\), or even just \\(x = 30 \\), the sign of this polynomial is positive, and for a negative value of \\( x\\), say \\( x = -20 \\), the sign of this polynomial is negative. Thus, as \\( x \to \infty\\), \\( y > 0 \\), and as \\( x \to -\infty \\), \\( y < 0\\). This is shown in the graph below.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/c-large-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We can prove this end behavior of polynomials (somewhat informally) as follows:

Consider,
{{< katex >}} p(x) = a_n\cdot x^n + a_{n-1}\cdot x^{n-1} + \cdots + a_1\cdot x + a_0 {{< /katex >}}
We can re-write \\(p(x) \\) as follows:
{{< katex >}} p(x) = a_n\cdot x^n\cdot r(x) {{< /katex >}}
where,
{{< katex >}} r(x) =  \frac{a_0}{a_n}\cdot\frac{1}{x^n} + \frac{a_1}{a_n}\cdot\frac{1}{x^{n-1}} + \cdots + \frac{a_{n-1}}{a_n}\cdot\frac{1}{x} + 1 {{< /katex >}}
Now, when \\(x\\) becomes very large negative or very large positive values, it can be seen that the above function \\(r(x) \\) will be almost equal to 1. This is written formally as,
{{< katex >}} \lim_{x\to \infty}r(x) = 1 {{< /katex >}}
In English, *in the limit* as \\(x\\) tends towards \\(\infty\\), \\(r(x)\\) tends to \\(1\\). Likewise, as \\( x \to -\infty \\),
{{< katex >}} \lim_{x\to -\infty}r(x) = 1 {{< /katex >}}
In other words, at the extreme values of \\(x\\), the value of the polynomial is dominated and thus its sign determined by the term \\(a_n \cdot x^n\\). This leads us to the following scenarios:

{{< columns "5,90,5" >}}
<--->
{{< figure src="images/Polynomial End Behavior.png" class="figs" title="" >}}
<--->
{{< /columns >}}

### How many roots

We are finally in a position to see how the number of roots of a polynomial is related to its degree. Lets state the result.

**An even degree real polynomial** (domain is \\( \R \\)) and coefficients are also from \\( \R \\) **has an even number of real roots**, it can be 0 or 2 or any even number \\( \leq \\) the degree of the polynomial.

**An odd degree real polynomial has an odd number of real roots**, it can be 1 or 3 or any odd number \\( \leq \\) the degree of the polynomial.

Notice how an even degree polynomial may not any real roots at all. But an odd degree polynomial will necessarily have at least 1 real root.

We will not prove this formally, but will simply note that this follows from the end behavior investigation we did in the previous section. 

Lets take the case of an odd degree polynomial with positive \\(a_n\\). We know that such a polynomial is negative as \\(x \to -\infty \\), and is positive as \\(x \to +\infty \\). Since polynomial functions are continuous functions (they dont have any breaks in them), it follows that at some point the function has to cross the x-axis from -ve values of y to +ve values of y. Hence it has at least 1 root. Suppose it crosses back to the negative side, meaning it has a second root, then it has to necessarily again cross back to the postiive side, because that is the only way it can get to positive values for \\( x \to \infty \\). We can make similar arguments in each of the cases above.

## Solving polynomial equations

We know very well how to solve polynomial equations of degree 1, these are simply linear equations of the form, $$ ax + b = 0 $$.

We also know how to solve polynomial equations of degree 2, these are simply quadratic equations of the form, $$ ax^2 + bx + c = 0 $$. We also know how to find solutions to this quadratic equation. The solution as we know very well is given by: $$ x = \displaystyle \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

It turns out that this solution was known to human beings many years ago, we have reason to believe that it was known way back in 2000 B.C.!

Since then, it took many many years before we could figure out how to solve polynomial equations of degree 3, that is cubic equations of the form: $$ ax^3 + bx^2 + cx + d = 0 $$

Solving cubic equations became quite interesting in the 1500s, when a couple of mathematicians engaged in an intense contest trying to find out who can solve cubic equations better. This included Italian mathematicians Tartaglia and Cardano, who are credited with a lot of background work on solving cubic equations. You can read a little bit of this interesting history [here](https://en.wikipedia.org/wiki/Cubic_equation#History).

The formula for the roots of the cubic equation turns out to be quite involved, a glimpse of it can be found [here](https://brilliant.org/wiki/cardano-method/). The roots of a quartic equation are even more involved. After many years of efforts, it was finally shown that for polynomial equations of degree 5 or higher, it is just not possible to write an algebraic formula for the solution! Note that this does not mean that these equations dont have any solutions, of course they do as we saw in the plots above, it only means that it is not possible to write out an algebraic expression for the roots in terms of the coefficients of the polynomial, using operations such as addition, multiplication, subtraction, division of the coefficients or their square roots, and in general, n-th roots.

However, we can infer some interesting properties about the roots of polynomial equations, even for polynomials of higher degrees.

### Sum and product of roots

Lets do this with an example. Suppose we have a degree-2 polynomial, \\( f(x) = ax^2 + bx + c \\), and suppose we know that the roots of this polynomial are \\( r_1\\) and \\(r_2\\). The question is what can we say about the sum of the roots, and the product of the roots in terms of the coefficients.

The way to go about this is as follows. Since, \\(r_1\\) and \\(r_2\\) are the roots of the quadratic, we can say the following:
{{< katex >}}
\begin{array}{rcl}
ax^2 + bx + c & \equiv & a(x - r_1)(x - r_2) \\
& \equiv & a(x^2 - (r_1 + r_2)x + r_1 r_2) \\
& \equiv & ax^2 - a(r_1 + r_2)x + a r_1 r_2 \\ \\
\therefore r_1 + r_2 & = & - \displaystyle \frac{b}{a} \\ \\
r_1 r_2 & = & \displaystyle \frac{c}{a} \\
\end{array}
{{< /katex >}}

Can you try it out for a degree-3 polynomial, \\( f(x) = ax^3 + bx^2 + cx + d \\), and suppose we know that the roots of this polynomial are \\( r_1\\), \\(r_2\\) and \\( r_3 \\). The question is what can we say about the sum of the roots, and the product of the roots in terms of the coefficients.

Similar relationships can be written for higher degree polynomials as well, and these were first published by François Viète, a French mathematician who lived around the same time that Tartaglia and Cardano did, and are hence known as Vieta's formulas for roots.

It is important to note that this equations above only serve to give us an *idea* of what the roots may be, but do not provide a formula or an expression for the roots. For e.g., you may note that the relationship between the sum and product of roots of a quadratic and its coefficients is indeed the underlying principle behind the factorization approach.

### Rational root theorem

Another technique that can aid in guessing the roots of a polynomial is the rational root theorem. 

{{< theorem-block "Theorem" "Proof" >}}
Given a polynomial with integer coefficients, i.e.,

{{< katex >}} P(x) = a_n\cdot x^n + a_{n-1}\cdot x^{n-1} + \cdots + a_1\cdot x + a_0 {{< /katex >}}

with \\( a_i \in \Z \\) and \\( a_0, a_n \neq 0 \\). If the polynomial has any rational roots of the form \\( r_i = \displaystyle \frac{p}{q} \\), where \\(p\\) and \\(q\\) are relatively prime, then \\(p\\) and \\(q\\) satisfies:

- \\(p\\) is an integer factor of the constant term \\(a_0\\), and
- \\(q\\) is an integer factor of the leading coefficient \\(a_n\\).


<--->

The proof starts as follows. If the polynomial has a rational root, say \\(\displaystyle \frac{p}{q} \\), then 

{{< katex >}}
\begin{array}{rcl}
P(\frac{p}{q}) & = & 0 \\ \\
\displaystyle a_n\cdot (\frac{p}{q})^n + a_{n-1}\cdot (\frac{p}{q})^{n-1} + \cdots + a_1\cdot (\frac{p}{q}) + a_0 & = & 0 
\end{array}
{{< /katex >}}

A little bit of algebraic manipulations and some reasoning based on divisibility will get us the desired result.
.   
.   
.   
.   
.   
.   
.   
.   
.   
.   
.   
.   
.   
.   
Hence proved.

{{< /theorem-block >}}

Lets look at a practical example:

**Q1.** Does the polynomial
$$ P(x) = x^{3}-7x+6 $$
have rational roots? If so, find them.

{{< expand "Hint" >}}
What the above theorem tells us is that, *if* this polynomial has any rational roots of the form \\( \displaystyle \frac{p}{q} \\), then \\( p\\) will divide the constant term \\(6\\), and \\(q\\) will divide the leading term \\(1\\). 
{{< /expand >}}

{{< expand "Solution" "..." >}}
Since the divisors of \\(1\\) are only \\( \pm 1\\), those are the only values that \\(q\\) can take. And the values that \\(p\\) can take are \\( \pm 1, \pm 2, \pm 3, \pm 6\\). So, we need to check only 8 values to find all the rational roots of this polynomial. 

Lets try \\( x = +1 \\)
$$ P(1) = 1^3 - 7\cdot 1 + 6 = 0 $$
Hence \\(+1\\) is a root of the polynomial.

Try out the rest.
{{< /expand >}}

Lets look at another example

**Q2.** Does the polynomial
$$ p(x) = 2x^{3}+x-1 $$
have rational roots? If so, find them.

{{< expand "Hint" >}}
If this polynomial has any rational roots, then the numerator of such a root has to divide \\(-1\\), and the denominator has to divide \\(2\\). The only possibilities are \\( \pm 1, \pm \frac{1}{2} \\). Try out these four values. 
{{< /expand >}}

{{< expand "Solution" "..." >}}
It turns out that none of these are roots. Hence, the theorem lets us say that this polynomial does not have *any* rational roots.
{{< /expand >}}
