---
title: "Surds"
date: 2020-06-13T21:07:06+05:30
draft: false
weight: 4
---

## Working with Surds
Most textbook chapters on Surds cover the regular problems using the rules that pertain to addition, subtraction, mulitplication and division of surds, and of course, the most common of them all, rationalizing the denominator. We will only briefly touch upon these here, before moving on to some more interesting learnings on surds:

 * Addition/Subtraction of surds:
   * When an integer and a surd are added/subtracted, there is no more simplifcation possible: $$2 \pm \sqrt{3}$$
   * When two different surds are added/subtracted, there is no more simplifcation possible: $$ \sqrt{2} + \sqrt{3}$$
   * When two *similar* surds are added/subtracted, the result cab be simplified as follows: $$ \sqrt{5} + 3\sqrt{5} = 4\sqrt{5}$$ $$ \sqrt[3]{5} - 4\sqrt[3]{5} = -3\sqrt[3]{5}$$
 * Multiplication/Division of surds:
   * When an integer and a surd are multiplied/divided, there is no more simplifcation possible: $$2 \sqrt{3} \text{ , } \frac{\sqrt{5}}{4}$$
   * When two surds of the same n-th root but different bases are multiplied/divided, the result can be simplified as follows: $$ \sqrt{2} \sqrt{3} = \sqrt{2\cdot 3} = \sqrt{6} $$ $$ \frac{\sqrt[3]{10}}{\sqrt[3]{5}} = \sqrt[3]{\frac{10}{5}} = \sqrt[3]{2}$$
   * When two surds of different n-th root but same base are multiplied/divided, the result can be simplified using the laws of indices: $$ \sqrt[3]{2} \sqrt{2} = 2^{\frac{1}{3}}2^{\frac{1}{2}} = 2^{\frac{1}{3} + \frac{1}{2}} = 2^{\frac{5}{6}} = \sqrt[6]{2^5}$$ $$ \frac{\sqrt[3]{10}}{\sqrt[4]{10}} = \frac{10^{\frac{1}{3}}}{10^\frac{1}{4}} = 10^{\frac{1}{3} - \frac{1}{4}} = 10^{\frac{1}{12}} = \sqrt[12]{10}$$ 
   * When two *similar* surds are multiplied/divided, the result can be simplified as follows: $$ \sqrt{5} \cdot 3\sqrt{5} = 3\cdot{5} = 15$$ $$ \sqrt[3]{5} \div 4\sqrt[3]{5} = \frac{1}{4}$$
 * Rationalizing the denominator:
   * When a surd occurs in the denominator, the usual practice is to *rationalize* the denominator and *move* the surd to the numerator as follows: $$ \frac{\sqrt{3}}{\sqrt{2}} = \frac{\sqrt{3}\cdot\sqrt{2}}{\sqrt{2}\cdot\sqrt{2}} = \frac{\sqrt{3}\cdot\sqrt{2}}{2} = \frac{\sqrt{6}}{2} $$
   * Or as follows (the surds \\(3 - \sqrt{2}\\) and \\( 3 + \sqrt{2} \\) are called conjugates of each other): $$ \frac{1}{3 + \sqrt{2}} = \frac{1\cdot(3 - \sqrt{2})}{(3 + \sqrt{2})\cdot(3 - \sqrt{2})} = \frac{3 - \sqrt{2}}{3^2 - (\sqrt{2})^2} = \frac{3 - \sqrt{2}}{9 - 2} = \frac{3 - \sqrt{2}}{7} $$ 
 * A combination of operations:
   * An example with all of the above opertations is as follows:
{{< katex >}}
\begin{array}{rcl}
\displaystyle \frac{(1 + \sqrt{5})^2}{\sqrt{3} - 1} & = & \displaystyle \frac{1 + 2\sqrt{5} + (\sqrt{5})^2}{\sqrt{3} - 1} \\ \\
& = & \displaystyle \frac{6 + 2\sqrt{5}}{\sqrt{3} - 1} \\ \\
& = & \displaystyle \frac{2\cdot(3 + \sqrt{5})\cdot(\sqrt{3} + 1)}{(\sqrt{3} - 1)\cdot(\sqrt{3} + 1)} \\ \\
& = & \displaystyle \frac{2\cdot(3 + \sqrt{5})\cdot(\sqrt{3} + 1)}{(\sqrt{3})^2 - 1^2} \\ \\
& = & \displaystyle \frac{2\cdot(3 + \sqrt{5})\cdot(\sqrt{3} + 1)}{3 - 1} \\ \\
& = & \displaystyle \frac{\cancel{2}\cdot(3 + \sqrt{5})\cdot(\sqrt{3} + 1)}{\cancel{2}} \\ \\
& = & 3\sqrt{3} + \sqrt{5}\cdot\sqrt{3} + 3 + \sqrt{5}\\ \\
\therefore \displaystyle \frac{(1 + \sqrt{5})^2}{\sqrt{3} - 1} & = & 3 + 3\sqrt{3} + \sqrt{5} + \sqrt{15} \\
\end{array}
{{< /katex >}}

We will stop here with these purely algebraic manipulations of surds and look at some interesting ideas around them.

## Surds in interesting ways

### Triangle on the hypotenuse

Suppose we start with an isoceles right angled triangle. With the hypotenuse of this triangle as the side we draw another isoceles right angled triangle. And we keep repeating this to have a picture that looks somewhat like a spiral as shown below:

{{< figure src="images/triangle-on-the-hypotenuse.png" class="figs" title="Triangle on the hypotenuse spiral." >}}

The question is what is the ratio of the hypotenuse the last triangle here to the hypotenuse of the first, i.e. \\(\displaystyle \frac{OA_9}{OA_2} = ?\\) 

If we write out the following sequence of sides - \\(OA_1\\), \\(OA_2\\), ..., \\(OA_9\\), is there a pattern? 

What about the sequence of the areas of the triangles? 

What is the total area of this figure?

### Geometric construction

We know from right angled triangles, that a right triangle with sides of length 1 each would have a hypotenuse of length \\(\sqrt{2}\\). If we draw a right traingle with sides of length 1 and 2, then the hypotentuse would be of length \\( \sqrt{5}\\).

The question we want to ask is the following - suppose we are given a line segment of length \\(a\\), how do we construct a line segment, geometrically, with length \\(\sqrt{a}\\)?

It turns out that this can be done in a very interesting way, and requires a little bit of insight into circles to do so.

{{< theorem-block "Construction" "Proof" >}}

{{< columns "60,40" >}}
Given a line segment \\(AB = a\\) units. Extend \\(AB\\) by \\(BD = 1\\) unit. Now bisect the segment \\(AD\\) to find its center \\(C\\) and draw a circle with \\(AC\\) as the radius. Now draw a perpendicular to \\(AB\\) at \\(B\\) intersecting the circle at \\(X\\). Then \\(BX = \sqrt{a}\\) units.
<--->
{{< figure src="images/geometric-sqrt-a.png" class="figs" title="" >}}
{{< /columns >}}

<--->

{{< columns "60,40" >}}
The proof that this construction works is based on inscribed angle theorem to come up with similar triangles and what is called the Intersecting Chords theorem. 

Then the fact that \\(CB \perp XY \\) is used to relate \\(BX\\) and \\(BY\\) to each other. How?

And the result follows from there.
<--->
{{< figure src="images/geometric-sqrt-a-2.png" class="figs" title="" >}}
{{< /columns >}}

{{< /theorem-block >}}

### Nested Surds

Surds can also be nested. Just as we encountered \\( 2 + \sqrt{3} \\) as a surd, an equally valid surd is \\( \sqrt{2 + \sqrt{3}} \\). Now of course, the creativity of the human brain is such that it doesn't stop thinking. You can nest surds within surds infinitely and ask what would happen:
$$ \sqrt{2 + \sqrt{2 + \sqrt{2 + \sqrt{2 + \cdots}}}} $$

This particular infinitely nested surd is easy to unravel, and that is done as follows. The key is to note that since the nesting is infinitely repeated, the same number that we are looking for, lets call it \\(x\\), also appears under the radical sign.

$$ \underbrace{\sqrt{2 + {\sqrt{2 + \sqrt{2 + \sqrt{2 + \cdots}}}}}}_{x} $$

\\(x\\) also appears inside the radical (surprise!) as shown below:

$$ \sqrt{2 + \underbrace{\sqrt{2 + \sqrt{2 + \sqrt{2 + \cdots}}}}_{x}} $$

Hence we can simplify this nested surd as follows:

{{< katex >}}
\begin{array}{rcl}
x & = & \sqrt{2 + \sqrt{2 + \sqrt{2 + \sqrt{2 + \cdots}}}} \\ \\
\therefore x & = & \sqrt{2 + x} \\ \\
\end{array}
{{< /katex >}}

Now, this is a simple quadratic equation, and can be easily solved to find the value of \\(x\\):

{{< katex >}}
\begin{array}{rcl}
x & = & \sqrt{2 + x} \\ \\
\therefore x^2 & = & 2 + x \\ \\
\therefore x^2 -x - 2 & = & 0 \\ \\
\therefore (x - 2)\cdot(x + 1) & = & 0 \\ \\
\therefore x = 2 & \text{or} & x = -1 \\ \\
\end{array}
{{< /katex >}}

And since \\(x = 2\\) is the only valid solution, it turns out, almost magically, that:

$$ \sqrt{2 + \sqrt{2 + \sqrt{2 + \sqrt{2 + \cdots}}}} = 2 $$

### Golden Ratio

Another such nested surd of great interest is the following:
$$ \sqrt{1 + \sqrt{1 + \sqrt{1 + \sqrt{1 + \cdots}}}} $$

And this can be simplified in the same manner as above to arrive at the following:
$$ \sqrt{1 + \sqrt{1 + \sqrt{1 + \sqrt{1 + \cdots}}}} = \frac{1 + \sqrt{5}}{2} $$

This is an extremely well studied surd in mathematics and is called the Golden Ratio, denoted by \\(\varphi \\). 

Two quantities are considered to be in the golden ratio if their ratio is the same as the ratio of their sum to the larger of the two quantities. We can check that for the above surd:

{{< katex >}}
\begin{array}{lrcl}
\text{Let } & \displaystyle \frac{a}{b} & = & \displaystyle \frac{1 + \sqrt{5}}{2} \\\\
\text{Then } & \displaystyle \frac{a + b}{a} & = & \displaystyle \frac{(1 + \sqrt{5}) + 2}{(1 + \sqrt{5})} \\\\
& & = & \cdots \\
& & = & \cdots \\
& & = & \displaystyle \frac{1 + \sqrt{5}}{2} \\\\
\end{array}
{{< /katex >}}

It turns out that the Golden Ratio occurs in some very interesting places in nature:

 * The ratio of the diagonal of a regular pentagon to its side happens to be in the Golden Ratio.
 * The ratio of successive numbers of the Fibbonacci sequence is approximately equal to \\(\varphi \\). 
 * What's more, many flowers have *learnt* over the years (millions and millions of years of evolution) that the best way to organize the seeds on its surface is using the Golden Ratio!!

Here is a video that showcases why this is so:
{{< youtube id="sj8Sg8qnjOg" >}}


