---
title: "Polynomial Arithmetic"
date: 2020-04-26T06:22:01+05:30
draft: false
weight: 3
---

In this session, we will explore basic arithmetic operations that can be performed with polynomials, typically taking two of them together, but it can also be many.

## Addition and Subtraction

Addition and subtraction are the most basic operations that can be defined on two polynomials. Today, it may seem straighforward for us to define these operations. But when initially defined, it is likely it would have taken some amount of rigor to define it meaningfully. For e.g., how should we add two polynomials say, \\( p_1(x) = 4x^3 + 5x \\) and \\( p_2(x) = 4x^2 + 5 \\)? It might have taken a while to define that polynomials should be added by adding like power terms together. Lets see this in action.

### Of functions
First, lets be clear how to define addition and subtraction of two functions, any two general functions:
{{< katex >}}
\begin{array}{rcl}
(f + g)(x) & = & f(x) + g(x) \\
(f - g)(x) & = & f(x) - g(x) \\
\end{array}
{{< /katex >}}

That may sound obvious, but in words, what this is really saying is that:

- When we add two functions, say \\(f(x) \\) and \\( g(x) \\), we get a new function.
- The function can be called any name, we could call it \\(h(x)\\) or we could call it \\( (f+g)(x) \\). Note that \\( (f+g) \\) is just a name for this new function.
- In order to find the value of this new function for any \\(x\\), simply find the value of the function \\(f \\) for that \\(x\\), and the value of the function \\(g\\) for that \\(x\\), and add those two values.
- Similarly, for subtraction.

### Of polynomials
The question that we are asking is if the two functions are polynomial functions, then can we simplify this addition any further. Or do we have to painfully find the value of \\(f(x)\\) at each \\(x\\) and the value of \\(g(x)\\) at each \\(x\\) and then add them the values to find the value of the new function? Well, we can do better than that. If the two functions are polynomial functions, then we can write out the new function in a manner that we don't need to go back to the original functions each time. That is possible by defining addition of polynomials as follows:

{{< highlight-box "Defn 1:" "none" "" "part" >}}
Given two polynomial functions, the addition of the two functions is defined as follows:

{{< katex >}} 
\begin{array}{rcl}
p_1(x) & = & \displaystyle \sum_{i = 0}^m a_i x^i \\ \\
p_2(x) & = & \displaystyle \sum_{i = 0}^n b_i x^i \\ \\
(p_1\pm p_2)(x) & = & \displaystyle \sum_{i = 0}^{max(m,n)} (a_i \pm b_i) x^i
\end{array}
{{< /katex >}}

{{< /highlight-box >}}

In words, this simply says that addition and subtraction of two polynomials are performed by adding or subtracting corresponding coefficients.

Lets take a couple of examples to make sure this is clear:
{{< katex >}} 
\begin{array}{ccrcrcr}
& & x^2 & + & 2x & + & 3 \\ 
+ & & 4x^2 & - & 5x & + & 9 \\ 
\hline
& & 5x^2 & - & 3x & + & 12 \\ 
\end{array}
{{< /katex >}}

Another one with missing coefficients, and polynomials with different degrees:
{{< katex >}} 
\begin{array}{ccrcrcrcr}
& & 4x^3 & & & + & 5x & & \\ 
+ & & & & 4x^2 & & & + & 5 \\ 
\hline
& & 4x^3 & + & 4x^2 & + & 5x & + & 5 \\ 
\end{array}
{{< /katex >}}

Notice how the same degree terms are aligned before addition or subtraction in the example below:
{{< katex >}} 
\begin{array}{ccrcrcrcr}
& & 4x^3 & + & 3.2x^2 & + & 5x & + & 12 \\ 
- & & 5x^3 & + & 4x^2 & & & - & 5 \\ 
\hline
& & -x^3 & - & 0.8x^2 & + & 5x & + & 17 \\ 
\end{array}
{{< /katex >}}

Do take care to note that for the constant term above, we need to subtract \\( -5 \\) from \\( 12\\), and that is the same as adding \\( +5\\) to \\(12\\) yielding \\( 17\\).

**Q1.** What can we say about the degree of the new polynomial that we get upon adding two polynomials or subtracting one polynomial from the another? 

{{< expand "Hint" >}}
The simplest way to figure this out is by taking a few samples. Take two polynomials of degree-3 and see what is the degree of the resulting polynomial upon addition or subtraction. Try with various different degree-3 polynomials. Take a degree-3 polynomial and a degree-2 polynomial and try the same exercise.
{{< /expand >}}

{{< expand "Answer" "..." >}}
The degree of the resulting polynomial will be at most the max of the degrees of the original polynomials.
{{< /expand >}}

### Linear Combinations

We can take this one step further by defining multiplication of a polynomial with a number, in our case a polynomial with a real number. We can further combine this scaling operation with the addition and subtraction operations to come up with what are called linear combinations.

{{< highlight-box "Defn 2:" "none" "" "part" >}}
Given two polynomial functions, the linear combination of the two functions is defined as follows:

{{< katex >}} 
\begin{array}{rcl}
p_1(x) & = & \displaystyle \sum_{i = 0}^m a_i x^i \\ \\
p_2(x) & = & \displaystyle \sum_{i = 0}^n b_i x^i \\ \\
(k_1 p_1\pm k_2 p_2)(x) & = & \displaystyle \sum_{i = 0}^{max(m,n)} (k_1 a_i \pm k_2 b_i) x^i
\end{array}
{{< /katex >}}

{{< /highlight-box >}}

A few examples will help:

{{< katex >}} 
\begin{array}{crrcrcrl}
& 2\cdot (& x^2 & + & 2x & + & 3 & ) \\ 
+ & 3\cdot (& 4x^2 & - & 5x & + & 9 & )\\ 
\hline
& & 14x^2 & - & 11x & + & 33 \\ 
\end{array}
{{< /katex >}}

An example with a negative multiplier:

{{< katex >}} 
\begin{array}{crrcrcrcrl}
& 2\cdot (& 4x^3 & & & + & 5x & & & )\\ 
- & 3\cdot (& & & 4x^2 & & & + & 5 & )\\ 
\hline
& & 8x^3 & - & 12x^2 & + & 10x & - & 15 \\ 
\end{array}
{{< /katex >}}

## Multiplication

The multiplication of two polynomials throws open some very interesting and entirely new possiblities. The multiplication of polynomials follows from the following three basic properties of multiplication of real numbers:

{{< katex >}}
\begin{array}{rclcl}
a\cdot (b \pm c) & = & a\cdot b \pm a\cdot c & & \text{Distributive Law} \\
a\cdot b & = & b\cdot a & & \text{Commutative Law} \\
a^m\cdot a^n & = & a^{m + n} & & \text{Law of Indices} \\
\end{array}
{{< /katex >}}

Lets see how these get applied in the context of polynomials, with a few examples:
{{< katex >}}
\begin{array}{rcl}
x\cdot x^2 & = & x^{1 + 2} \\
& = & x^3 \\ \\
x\cdot (2x^2 + 3x + 4) & = & x\cdot 2x^2 + x\cdot 3x + x\cdot 4 \\
& = & 2x^3 + 3x^2 + 4x \\ \\
(x - 0.5)\cdot (2x^2 - 3x + 4) & = & x\cdot (2x^2 - 3x + 4) -0.5 \cdot (2x^2 - 3x + 4) \\
& = & (2x^3 - 3x^2 + 4x) - (x^2 - 1.5x + 2) \\
& = & 2x^3 - 3x^2 + 4x - x^2 - 1.5x + 2 \\
& = & 2x^3 - 3x^2 - x^2 + 4x - 1.5x + 2 \\
& = & 2x^3 - 4x^2 + 2.5x + 2 \\
\end{array}
{{< /katex >}}

**Q2.** What can we say about the degree of the new polynomial that we get upon multiplying two polynomials with one another? 

{{< expand "Hint" >}}
Unlike in addition and subtraction where the highest degree term could get canceled out, in multiplication, we can say exactly what the degree of the new polynomial will be. Intermediate degree terms may get canceled out, but the topmost degree term will always be present with a fixed degree.
{{< /expand >}}

{{< expand "Answer" "..." >}}
If the degree of one polynomial is \\( m\\) and the degree of another polynomial is \\( n\\), then the degree of the resulting polynomial will be at exactly \\( m + n \\).
{{< /expand >}}

Lets formally define multiplication:
{{< highlight-box "Defn 3:" "none" "" "part" >}}
Given two polynomial functions, the product of the two functions is defined as follows:

{{< katex >}} 
\begin{array}{rcl}
p_1(x) & = & \displaystyle \sum_{i = 0}^m a_i x^i \\ \\
p_2(x) & = & \displaystyle \sum_{i = 0}^n b_i x^i \\ \\
(p_1\cdot p_2)(x) & = & \displaystyle \sum_{i = 0}^{m+n} c_i x^i \\
\text{where } c_k & = & a_0b_k + a_1b_{k-1} + \cdots + a_{k-1}b_1 + a_kb_0 \\
\end{array}
{{< /katex >}}

{{< /highlight-box >}}

Lets look at the coefficient of the \\( x^k \\) term in the resulting polynomial closely. For e.g., if we have to find the coefficient of say \\( x^4 \\), that would be $$ c_4 = a_0b_4 + a_1b_3 + a_2b_2 + a_3b_1 + a_4b_0 $$
Suppose \\(p_1(x)\\) is a degree-5 polynomial while \\( p_2(x) \\) is only a degree-3 polynomial, then in the above computation of \\( c_4\\), \\(a_0b_4\\) will be \\(0\\) because \\( b_4 \\) is \\( 0\\).

As before, lets take an example to see how this works:

{{< katex >}}
\begin{array}{rcl}
p_1(x) & = & 2x^3 + 3x^2 + 4x + 5 \\
p_2(x) & = & 3x^2 + 2x + 1 \\
(p_1\cdot p_2)(x) & = & ? \\
\end{array}
{{< /katex >}}

**Approach 1.** We will look at different approaches to do this, lets first do this from the definition:
{{< katex >}}
\begin{array}{rcl}
p_1(x) & = & 2x^3 + 3x^2 + 4x + 5 \\
\therefore a_3 & = & 2 \\
a_2 & = & 3 \\
a_1 & = & 4 \\
a_0 & = & 5 \\ \\
p_2(x) & = & 3x^2 + 2x + 1 \\
\therefore b_2 & = & 3 \\
b_1 & = & 2 \\
b_0 & = & 1 \\ \\
\end{array}
{{< /katex >}}
And now we can do the calculation by definition for the multiplication of these two polynomials:
{{< katex >}}
\begin{array}{rclcl}
c_0 & = & a_0 b_0 & = & 5\cdot 1 & = & 5 \\
c_1 & = & a_0 b_1 + a_1 b_0 & = & 5\cdot 2 + 4\cdot 1& = & 14 \\
c_2 & = & a_0 b_2 + a_1 b_1 + a_2 b_0 & = & 5\cdot 3 + 4\cdot 2 + 3\cdot 1 & = & 26 \\
c_3 & = & a_0 b_3 + a_1 b_2 + a_2 b_1 + a_3 b_0 & = & 5\cdot 0 + 4\cdot 3 + 3\cdot 2 + 2\cdot 1 & = & 20 \\
c_4 & = & \ldots & & & & \\
c_5 & = & a_0 b_5 + \cdots + a_3 b_2 + \cdots + a_5 b_0 & = & 0 + \cdots + 6 + \cdots + 0 & = & 6 \\
\end{array}
{{< /katex >}}
And the final result follows:
{{< katex >}}
\begin{array}{rcl}
(p_1\cdot p_2)(x) & = & 6x^5 + 13x^4 + 20x^3 + 26x^2 + 14x + 5 \\
\end{array}
{{< /katex >}}

**Approach 2.** We can take another approach, more from basic definitions of multiplcation, rather than using the above definition directly:
{{< katex >}}
\begin{array}{rcl}
p_1(x) & = & 2x^3 + 3x^2 + 4x + 5 \\
p_2(x) & = & 3x^2 + 2x + 1 \\ \\
(p_1\cdot p_2)(x) & = & (2x^3 + 3x^2 + 4x + 5)\cdot(3x^2 + 2x + 1) \\ \\
& = & (2x^3 + 3x^2 + 4x + 5)\cdot 3x^2 \\
& & + (2x^3 + 3x^2 + 4x + 5)\cdot 2x \\
& & + (2x^3 + 3x^2 + 4x + 5)\cdot 1 \\ \\
& = & 6x^5 + 9x^4 + 12x^3 + 15x^2 \\
& & + 4x^4 + 6x^3 + 8x^2 + 10x \\
& & + 2x^3 + 3x^2 + 4x + 5 \\ \\
\therefore (p_1\cdot p_2)(x) & = & 6x^5 + 13x^4 + 20x^3 + 26x^2 + 14x + 5 \\
\end{array}
{{< /katex >}}

Clearly, with the same end result as before.

**Approach 3.** We can take yet another approach that will also help us see how these two approaches are basically the same and also relate to a basic technique that we learnt very early on in school.

{{< katex >}}
\begin{array}{rcrcrcrcrcr}
& & & & 2x^3 & + & 3x^2&  + & 4x & + & 5 \\
& & & & \times & & 3x^2 & + & 2x & + & 1 \\ \\
\hline \\
& & & & 2x^3 & + & 3x^2&  + & 4x & + & 5 \\
& & 4x^4 & + & 6x^3 & + & 8x^2&  + & 10x & & \\
6x^5 & + & 9x^4 & + & 12x^3 & + & 15x^2& & & & \\ \\
\hline \\
6x^5 & + & 13x^4 & + & 20x^3 & + & 26x^2& + & 14x & + & 5 \\
\end{array}
{{< /katex >}}

This is the familiar long method of multiplication that we have learnt in school. 

Notice the empty space at the end of the 2nd row. It happened automatically in the multiplication above because we were multiplying the first polynomial by the second term \\( 2x \\) in the second polynomial. 

Notice how the 3rd column in the multiplcation above adds up to \\( 20 x^2 \\) that is the same as the coefficient \\( c_3 \\) that we found earlier on.

## Division

### Long division

The Long Division example on Wikipedia [here](https://en.wikipedia.org/wiki/Polynomial_long_division#Polynomial_long_division) is a good read.

This video at Khan Academy [here](https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:poly-div/x2ec2f6f830c9fb89:quad-div-by-linear/v/polynomial-division) is also good to watch.

### Short division

**EC Note** - This is not a topic in Add Math syllabus, this is an ExtraCurricular topic.

People have come up with shorter methods to do division of polynomials. The regular synthetic division method can be understood from [here](https://en.wikipedia.org/wiki/Synthetic_division#Regular_synthetic_division). A similar method is what is called the polynomial short division, which can be found [here](https://en.wikipedia.org/wiki/Polynomial_long_division#Polynomial_short_division).

## Factors and Remainders

### Division Algorithm

The division algorithm for polynomials is quite similar to the one for numbers. It goes as follows:
{{< theorem-block "Theorem" "Proof" >}}
Given two polynomials \\(p_1(x)\\) and \\(p_2(x)\\), \\(\exists \\) unique polynomials \\(q(x)\\) and \\(r(x)\\), such that   
$$ p_1(x) = q(x)\cdot p_2(x) + r(x) $$ and degree of \\(r(x) < p_2(x) \\)
<--->
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
.  
.  

Hence proved.

{{< /theorem-block >}}

### Factor Theorem

For a given polynomial, \\( p(x) \\), we know that if \\( (x - c) \\) is a factor of the polynomial, then we can write the polynomial as:
$$ p(x) = (x - c)\cdot q(x) $$ 
where \\( q(x) \\) is some polynomial, i.e., the remainder \\( r(x) = 0 \\).

Hence, if \\( (x - c) \\) is a factor of \\( p(x) \\), then \\( p\(c\) = 0 \\).

Factor theorem says that the other way round is true as well.

{{< theorem-block "Theorem" "Proof" >}}
If \\(p\(c\) = 0\\) for a polynomial, then \\( (x - c) \\) is a factor of \\( p(x) \\).
<--->
This follows from the division algorithm above.
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

A slightly modified version of the Factor theorem is as follows for rational roots - If \\(p(\displaystyle\frac{b}{a}) = 0\\) for a polynomial, then \\( (ax - b) \\) is a factor of \\( p(x) \\).

### Remainder Theorem

Another striking result of the division algorithm is the Remainder theorem.
{{< theorem-block "Theorem" "Proof" >}}
If a polynomial \\( p(x) \\) is divided by \\( (x - c) \\) the remainder is \\(p\(c\)\\).
<--->
This follows from the division algorithm above.
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

Similar to above, a slightly modified version of the Remainder theorem is as follows for rational roots - If \\( p(x) \\) is divided by \\( (ax - b) \\), then the remainder is \\(p(\displaystyle\frac{b}{a}) \\).

## Summary

We have spent a lot of time now learning functions, equations, graphs and now polynomials and factors. We can summarize the learning over the last few sessions as follows.

For a polynomial function \\( p(x) \\), if the function \\(p\\) maps the element \\(c\\) in the domain to the element \\( 0\\) in the co-domain, then the following statements are all equivalent:

- \\( c\\) is a **zero** of the function.
- \\( c\\) is a **root** or a **solution** of the equation \\( p(x) = 0 \\).
- The graph of the function, i.e., \\( y = p(x)\\) has an **x-intercept** at \\( (c, 0) \\).
- The polynomial \\( p(x) \\) when divided by \\( (x - c) \\) has a **remainder** of \\(0\\).
- \\( (x - c) \\) is a linear **factor** of \\( p(x) \\).
