---
title: "Binomial Theorem"
date: 2020-01-22T20:58:57+05:30
draft: true
weight: 1
---

## Basic Mathematical Operations

We have come a long way as human beings exploring mathematical operations. We will take a quick refresher here before getting into the binomial theorem.

### Addition

We started of course with the addition operation, starting with the addition of natural numbers, like 3 and 2.

{{< figure src="images/Apple-Addition.png" width="20%" class="figs" title="3 + 2 = 5" >}}

In pioneering research conducted by psychologist Karen Wynn in 1990s, she reported that five-month-old human infants are able to compute the outcomes of simple addition and subtraction operations on small sets of physical objects. Her seminal experiment involving Mickey Mouse dolls manipulated behind a screen demonstrated that five-month-old infants expect 1 + 1 to be 2, and they are comparatively surprised when a physical situation seems to imply that 1 + 1 is either 1 or 3. This finding has since been affirmed by a variety of laboratories using different methodologies.

It turns out that not just humans, but also other species such as primates and elephants were also able to show a limited ability to add.

{{< columns >}}
<--->
<iframe width="560" height="315" src="https://www.youtube.com/embed/H2gRLCZSBEA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<--->
{{< /columns >}}

It should not come as much of a surprise, for a cheetah mother would likely need to be able to count to make sure all her cubs are with her, and a pack of hyenas would likely need to size up a group of bisons before attacking them.

Humans of course have taken addition a long way since, having written down the rules of how to add not just natural numbers, but also positive and negative integers, rational numbers, irrational numbers, and even other objects such as functions and matrices.

### Multiplication

Multiplication came next, as we took addition to the next level and explored the notion of repeated addition.

{{< columns >}}
{{< figure src="images/3x1=3.png" class="figs" title="3 x 1 = 3" >}}
<--->
{{< figure src="images/3x4=12.png" class="figs" title="3 x 4 = 12" >}}
{{< /columns >}}

As in the case of addition, we have written down the rules of how to multiply not just natural numbers like 3 and 4 abve, but also positive and negative integers, rational numbers, irrational numbers, and even other objects. We have also written down the rules that govern multiplication for each kind of object, for e.g.:

**Commutative Rule**: For real numbers (and we will learn later for complex numbers as well), that the order of multiplication does not matter. i.e.
$$ a\cdot b = b\cdot a $$

Addition of real numbers is also commutative, but as we know very well, subtraction of real numbers is *not* commutative, since \\( a - b \ne b - a \\). We will learn in advanced mathematics that we can define rules for multiplying objects called matrices, but matrix multiplication is not commutative, i.e. for two matrices \\(A\\) and \\(B\\), \\( A\cdot B \ne B\cdot A \\).

In other words, based on the nature of the operands involved a particular operation may or may not be commutative.

**Associative Rule**: For real numbers, we also know well the following property known as the associative rule:
$$ (a\cdot b)\cdot c = a\cdot (b\cdot c) $$

### Exponentiation

Just like multiplication can be looked at as an extension of addition by repeating it, we have come up with the operation of exponentiation which is simply repeated multiplication. As we know well:
$$ a^m = \underbrace{a \cdot a \cdot a \cdots a}_{m\text{ times}} $$

### Distributive property

We can take one step further and look at combining different mathematical operations. Of particular interest in this session is the combination of multiplication and addition operations. The distributive law concerns itself with the order of application of these two different operations.

For real numbers, we know that:
$$ a\cdot (b + c) = a\cdot b + a\cdot c $$
$$ (b + c)\cdot a = b\cdot a + c\cdot a $$

And since multiplication of real numbers is commutative, we can say that:
$$ a\cdot (b + c) = a\cdot b + a\cdot c = b\cdot a + c\cdot a = (b + c)\cdot a $$

As before, whether distributive laws apply or not depends on the nature of the operations as well as the operands. For e.g., it is worth taking a pause and noting that:
$$ (b + c) \div a = b\div a + c\div a $$
But,  
$$ a\div (b + c) \ne a\div b + a\div c $$
In words, for real numbers, the division operation is *"right-distributive"* over the addition operation, but it is *not "left-distributive"* over addition, or subtraction for that matter.

Our interest in this session is in the properties of the expression of the following form:
$$ (a + b)^m $$
where, \\(m\\) is a positive integer and \\(a\\) and \\(b\\) are real (either constants such as \\(2.534\\) or expressions such as \\(\displaystyle \frac{3x}{4}\\) ).

## Terms of the Expansion

### How many terms

Lets first get a grasp of how many terms are there in the expansion of the expression \\( (a + b)^m \\). Lets start with small values of m.

For \\(m = 1\\), it is very simple, of course:
$$ (a + b)^1 = a + b $$
there are obviously 2 terms.

For \\(m = 2\\), we probably know the formula for \\( (a + b)^2 \\) from earlier classes, but lets do it from scratch and check:
{{< katex >}}
\begin{array}{rcl}
(a + b)^2 & = & (a + b)\cdot (a + b) \\
& = & a\cdot (a + b) + b\cdot (a + b) \\
& & \text{(We can do this because a and b are real and} \\
& & \text{multiplication is right distributive over addition)} \\
\therefore (a + b)^2 & = & a\cdot a + a\cdot b + b\cdot a + b\cdot b \\
\end{array}
{{< /katex >}}
Thus \\((a + b)^2 \\) has 4 terms.  
(Note that we are not applying the commutative property of multiplication and simplifying \\( a\cdot b + b\cdot a = 2ab \\) yet.)

For \\(m = 3\\), lets do the expansion from scratch and check it out:
{{< katex >}}
\begin{array}{rcl}
(a + b)^3 & = & (a + b)\cdot (a + b)^2 \\
& = & (a + b)\cdot (a\cdot a + a\cdot b + b\cdot a + b\cdot b) \\
& = & a \cdot (a\cdot a + a\cdot b + b\cdot a + b\cdot b) + b \cdot (a\cdot a + a\cdot b + b\cdot a + b\cdot b) \\
& = & a \cdot a\cdot a + a \cdot a\cdot b + a \cdot b\cdot a + a \cdot b\cdot b + b \cdot a\cdot a + b \cdot a\cdot b + b \cdot b\cdot a + b \cdot b\cdot b \\
\end{array}
{{< /katex >}}
Thus \\((a + b)^3 \\) has 8 terms.   

Any guesses how many terms \\( (a + b)^{10} \\) will have?

We should be able to recognize this as a problem in counting, and use the techniques we learnt in the previous session. Each term in the expression has exactly 10 places to be filled, each place can be filled by either an \\(a\\) or with a \\(b\\), making it \\(2^{10}\\) ways. Therefore, the number of terms in the expansion of \\( (a + b)^{10} \\) is \\(2^{10}\\) or \\(1024\\).

In general, the expansion of \\((a + b)^m \\) will have \\( 2^m \\) terms.

### Nature of each term

We can see from the above expansion of \\( (a + b)^3 \\) that each term in the expansion is a product of 3 items, either all \\(a\\)'s or all \\(b\\)'s or some \\(a\\)'s and some \\(b\\)'s. 

For e.g. four example terms in the expansion are \\( a\cdot a\cdot a\\), \\(a \cdot a\cdot b\\), \\(b \cdot b\cdot a\\) and \\(b \cdot b\cdot b\\). We can rewrite each of these terms now using the commutative rule of multiplication and the definition of exponentiation as follows - \\(a^3\\), \\(a^2b\\), \\(ab^2\\) and \\(b^3\\) respectively.

Similarly, four example terms in the expansion of \\( (a + b)^{10} \\) are \\( a^{10}\\), \\(a^6b^4\\), \\(a^2b^8\\) and \\(b^{10}\\). Crucially, we can note that the power of \\(a\\) and the power of \\(b\\) in each term of the expansion add up to \\(10\\).

Thus, each term in the expansion of \\( (a + b)^m \\) can be written as:
$$ a^k\cdot b^{m - k} $$

### Number of unique terms

We can take the discussion in the previous section to arrive at the number of unique terms in the expansion. We can simply write out all the unique terms:
$$ a^mb^0\text{ , }a^{m-1}b^1\text{ , }a^{m-2}b^2\text{ , }\ldots\text{ , }a^2b^{m-2}\text{ , }a^1b^{m-1}\text{ , }a^0b^m $$

Notice how the powers of \\(b\\) are increasing from 0, 1, 2, \\(\ldots\\) up to m. Likewise, the powers of \\(a\\) are decreasing from m to 0. The total number of unique terms can thus be counted as \\((m + 1)\\).

We can check and confirm for small values of m:

As before, for \\(m = 1\\), it is very simple, of course:
$$ (a + b)^1 = a + b $$
there are obviously 2 terms.

For \\(m = 2\\), we can now combine the same terms together as follows:
{{< katex >}}
\begin{array}{rcl}
(a + b)^2 & = & (a + b)\cdot (a + b) \\
& = & a\cdot (a + b) + b\cdot (a + b) \\
& = & a\cdot a + a\cdot b + b\cdot a + b\cdot b \\
\therefore (a + b)^2 & = & a^2 + 2ab + b^2 \\
\end{array}
{{< /katex >}}
the well known formula for \\((a + b)^2 \\) which has 3 unique terms.   

And for \\(m = 3\\), we can combine the same terms together to get:
{{< katex >}}
\begin{array}{rcl}
(a + b)^3 & = & (a + b)\cdot (a + b)^2 \\
& = & (a + b)\cdot (a\cdot a + a\cdot b + b\cdot a + b\cdot b) \\
& = & a \cdot (a\cdot a + a\cdot b + b\cdot a + b\cdot b) + b \cdot (a\cdot a + a\cdot b + b\cdot a + b\cdot b) \\
& = & a \cdot a\cdot a + a \cdot a\cdot b + a \cdot b\cdot a + a \cdot b\cdot b + b \cdot a\cdot a + b \cdot a\cdot b + b \cdot b\cdot a + b \cdot b\cdot b \\
\therefore (a + b)^3 & = & a^3 + 3a^2b + 3ab^2 + b^3 \\
\end{array}
{{< /katex >}}
which has, as expected, 4 unique terms.

### Coefficient of each term

Now, we are all set to explore the coefficient of each term in the expansion.

Lets work with \\( m = 4 \\) as an example. We know that the total number of terms in the expansion of \\( (a + b)^4 \\) is \\(2^4\\). We also know that there is only 1 term with all \\(a\\)'s in it, and only one term with all \\(b\\)'s in it - i.e. \\(a^4\\) and \\(b^4\\) respectively occur only once each. But how many terms are there in the expansion with 3 \\(a\\)'s or with 2 \\(a\\)'s or with 1 \\(a\\). We can count these out:

{{< columns >}}
    a a a b
    a a b a
    a b a a
    b a a a
<--->
    a a b b
    a b a b
    a b b a
    b a a b
    b a b a
    b b a a
<--->
    b b b a
    b b a b
    b a b b
    a b b b
<--->
{{< /columns >}}

In other words:
$$ (a + b)^4 = 1\cdot a^4 + 4\cdot a^3b + 6\cdot a^2b^2 + 4\cdot ab^3 + 1\cdot b^4 $$

Can we now guess the coeeficient of say the term, \\( a^2b^8\\) in the expansion of \\( (a + b)^{10} \\)? As before this turns out to be a counting exercise and can be framed as follows - There are 10 places to fill with \\(a\\) or \\(b\\), how many ways are there to select 2 places to fill \\(a\\)'s? Note that when we choose 2 places to fill \\(a\\), we also mean that the remaining places will all be filled with \\(b\\)'s. Note also that the order does not matter, because multiplication is commutative. The answer should be simple. The number of ways of doing this is \\( ^{10}C_2 \\).

We can recheck the terms of the expansion of \\( (a + b)^4 \\). The coefficient of \\( a^3b^1\\) is \\( ^4C_3 = 4 \\), the coefficient of \\( a^2b^2\\) is \\( ^4C_2 = 6 \\) and coefficient of \\( a^1b^3\\) is \\( ^4C_1 = 4 \\).

In general, the coefficient of the k-th term (this term is \\(a^kb^{m-k} \\)) in the expansion of \\( (a + b)^m \\) is (surprise surprise) :
$$ ^mC_k $$

## Binomial Theorem

We have now understood all that we need to write out the general form of the Binomial Theorem:

{{< katex >}}
(a + b)^m = {}^mC_0 a^m b^0 + {}^mC_1 a^{m-1} b^1 + {}^mC_2 a^{m-2} b^2 + \cdots + {}^mC_{m - 2} a^2 b^{m-1} + {}^mC_{m-1} a^1 b^{m-1} + {}^mC_m a^0 b^m
{{< /katex >}}

Or written succinctly using the sigma notation:
$$ (a + b)^m = \displaystyle \sum_{k = 0}^{m} {}^mC_k a^k b^{m - k} $$

Lets go over a few examples using the binomial theorem.

{{< katex >}}
\begin{array}{rcl}
(a - b)^2 & = & (a + (- b))^2 \\
& = & {}^2C_0 a^2 (-b)^0 + {}^2C_1 a^1 (-b)^1 + {}^2C_2 a^0 (-b)^2 \\
& = & a^2 + 2 a (-b) + (-b)^2 \\
& = & a^2 - 2 a b + b^2 \\
\end{array}
{{< /katex >}}

The fact that we have \\( (a - b) \\) does not limit us from applying the Binomial Theorem above. Another example is as follows:

{{< katex >}}
\begin{array}{rcl}
(1 + \sqrt{2})^3 & = & {}^3C_0 1^3 {\sqrt{2}}^0 + {}^3C_1 1^2 {\sqrt{2}}^1 + {}^3C_2 1^1 {\sqrt{2}}^2 + {}^3C_3 1^0 {\sqrt{2}}^3\\
& = & 1 + 3{\sqrt{2}} + 3{\sqrt{2}}^2 + {\sqrt{2}}^3 \\
& = & 1 + 3{\sqrt{2}} + 6 + 2{\sqrt{2}} \\
& = & 7 + 5{\sqrt{2}} \\
\end{array}
{{< /katex >}}

We can check with a calculator that both sides above yield the same result of \\( 14.07\\). 

Note that the two terms in the Binomial Theorem can be any real numbers or even expressions. An example is below:

{{< katex >}}
\begin{array}{rcl}
(x + 2)^4 & = & {}^4C_0 x^4 2^0 + {}^4C_1 x^3 2^1 + {}^4C_2 x^2 2^2 + {}^4C_3 x^1 2^3 + {}^4C_4 x^0 2^4 \\
& = &  x^4 + 4x^3\cdot 2 + 6x^2\cdot 4 + 4x\cdot 8 + 16 \\
& = & x^4 + 8x^3 + 24x^2 + 32x +16 \\
\end{array}
{{< /katex >}}

### A visualization

A beautiful geometric visualization of the Binomial Theorem up to index 4 is shown below:

{{< figure src="images/binomial-geometric.png" class="figs" title="" >}}

## Patterns with Binomial Coefficients

### Recursive expansion

In some of the above examples we found the expansion of \\( (a + b)^4 \\). 
$$ (a + b)^4 = 1\cdot a^4 + 4\cdot a^3b + 6\cdot a^2b^2 + 4\cdot ab^3 + 1\cdot b^4 $$

Lets see if we can easily find the expansion for \\( (a + b)^5 \\) using the above.

{{< katex >}}
\begin{array}{rcl}
(a + b)^5 & = & (a + b)\cdot (a + b)^4 \\
& = & (a + b)\cdot (1\cdot a^4 + 4\cdot a^3b + 6\cdot a^2b^2 + 4\cdot ab^3 + 1\cdot b^4) \\ \\
\therefore (a + b)^5 & = & a\cdot (1\cdot a^4 + 4\cdot a^3b + 6\cdot a^2b^2 + 4\cdot ab^3 + 1\cdot b^4) \\
& & + b\cdot (1\cdot a^4 + 4\cdot a^3b + 6\cdot a^2b^2 + 4\cdot ab^3 + 1\cdot b^4) \\ \\
\end{array}
{{< /katex >}}

We can carefully rearrange the above expression by aligning similar terms together as follows:
{{< katex >}}
\begin{array}{rclclclclclcl}
\therefore (a + b)^5 & = & 1\cdot a^5 & + & 4\cdot a^4b & + & 6\cdot a^3b^2 & + & 4\cdot a^2b^3 & + & 1\cdot ab^4 & & \\
& & & + & 1\cdot a^4b & + & 4\cdot a^3b^2 & + & 6\cdot a^2b^3 & + & 4\cdot ab^4 & + & 1\cdot b^5 \\ \\
& = & 1\cdot a^5 & + & (1 + 4)\cdot a^4b & + & (4 + 6)\cdot a^3b^2 & + & (6 + 4)\cdot a^2b^3 & + & (4 + 1)\cdot ab^4 & + & 1\cdot b^5 \\
\end{array}
{{< /katex >}}

We already know that \\( (a + b)^4 \\) has 5 terms in the expansion and \\( (a + b)^5 \\) has 6 terms. What we are about to discover is the very interesting property between the coefficients of the terms in these expansions. Watch carefully 😎 :

{{< katex >}}
\begin{array}{rcccccccccccc}
(a + b)^4 & = & & 1\cdot a^4 & + & 4\cdot a^3b & + & 6\cdot a^2b^2 & + & 4\cdot ab^3 & + & 1\cdot b^4 & \\ \\
(a + b)^5 & = & 1\cdot a^5 & + & 5\cdot a^4b & + & 10\cdot a^3b^2 & + & 10\cdot a^2b^3 & + & 5\cdot ab^4 & + & 1\cdot b^5 \\
\end{array}
{{< /katex >}}

In words, the coefficient of \\( a^4b\\) in the expansion of \\( (a + b)^5 \\) is the sum of the coefficients of \\( a^4\\) and \\( a^3b \\) in the expansion of \\( (a + b)^4 \\).

### Another nCr property

This should not come as a surprise though if we know the following property of nCr. The proof is left as an exercise.

{{< theorem-block "Theorem" "Proof" >}}
{{< katex >}}
{}^nC_r = {}^{n - 1}C_{r - 1} + {}^{n - 1}C_{r}
{{< /katex >}}
<--->

{{< katex >}}
\begin{array}{rcl}
\text{LHS } & = & {}^nC_r \\
& = & \displaystyle \frac{n!}{r!\cdot (n - r)!} \\ \\
\text{RHS } & = & \\
\end{array}
{{< /katex >}}
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

## Pascal's Triangle

Arranging the Binomial Coefficients in the form of a triangle, where the m-th row has the coefficients from the expansion of \\( (a + b)^m \\), gives us the so-called Pascal's triangle.

{{< figure src="images/PascalTriangleAnimated2.gif" class="figs" title="First 5 rows of Pascal's triangle" >}}

### History of the triangle

(Borrowed from Wikipedia) The pattern of numbers that forms Pascal's triangle was known well before Pascal's time. Pascal innovated many previously unattested uses of the triangle's numbers, uses he described comprehensively in the earliest known mathematical treatise to be specially devoted to the triangle, his *Traité du triangle arithmétique* (1654; published 1665). Centuries before, discussion of the numbers had arisen in the context of Indian studies of combinatorics and of binomial numbers and the Greeks' study of figurate numbers.

From later commentary, it appears that the binomial coefficients and the additive formula for generating them, \\( {\displaystyle {\tbinom {n}{r}}={\tbinom {n-1}{r}}+{\tbinom {n-1}{r-1}}} \\), were known to Indian mathematician Pingala in or before the 2nd century BC. 

A picture from an [archived library manuscript](https://archive.org/details/PrakritPingalaPrastaraVarnaMatraPatakadiYantrani775GhaAlm4Shlf3DevanagariAlankarShastra/page/n5/mode/2up) at Dharmartha Trust at the Raghunath Temple in Jammu, India depicts this pictorially:

{{< figure src="images/Pingala-Meru-prastaara.png" class="figs" title="An ancient Indian manuscript with the depiction of the binomial coefficients as a triangle" >}}

### Interesting properties

The Pascal's triangle has innumerable interesting properties. Some of them are highlighted in this video. Some of them are so fascinating, they are bound to blow your mind off 😎😎 .

{{< columns >}}
<--->
<iframe width="560" height="315" src="https://www.youtube.com/embed/0iMtlus-afo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<--->
{{< /columns >}}

### Sierpinski triangle

We conclude this session by noting that if we color the odd and even numbers in the Pascal's triangle with different colors, then we get a picture that resembles the Sierpinski triangle.

{{< columns >}}
{{< figure src="images/Sierpinski_Pascal_triangle.svg" class="figs" title="" >}}
<--->
{{< figure src="images/Sierpinski_triangle.svg" class="figs" title="" >}}
{{< /columns >}}

Its almost like magic 😎😎😎.
