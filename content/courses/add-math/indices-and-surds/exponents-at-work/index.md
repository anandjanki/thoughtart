---
title: "Exponents at Work"
date: 2020-06-20T19:57:41+05:30
draft: false
weight: 3
---

## Very large numbers

Lets see how the notation for exponentiation and the laws of indices can be used to effectively manage large numbers. Recall the story of Reoh, our hero, who was on the maiden human flight to Andromeda Galaxy. 

Suppose he has to estimate the size of the Milky Way Galaxy from the following:

 * The distance from the Sun to the nearest star, Alpha Centauri, is 40,000,000,000,000 kms. 
 * The total number of stars in the Milky Way is estimated at 250,000,000,000. 

The intent of these calculations are not to arrive at the exact size of the Milky Way galaxy, but really to show how the exponent notation and the laws of indices come in handy while handling large numbers.

We know that the Milky Way Galaxy can be considered a somewhat of a plane figure. Further, for ease of calculations, we will assume that the galaxy is shaped like a square. And further assume  that all the stars in the galaxy are uniformly distributed on a 2-D grid on this square shape. This is depicted pictorially here:

{{< figure src="images/Milky-Way-Galaxy.jpg" class="figs" title="Estimating the size of the Milky Way Galaxy." >}}

Without the exponentiation notation our calculations might have looked as follows, side of the square : $$ 40,000,000,000,000 \times \sqrt{250,000,000,000} \text{ kms} $$

To try and continue that calculation looks onerous already, and this is where our exponentiation notation comes in handy:

{{< katex >}}
\begin{array}{rclcl}
\text{Distance between any two stars} & = & 40,000,000,000,000 \text{ kms} \\
& = & 40 \times \underbrace{10\times 10\times 10\times \cdots \times 10}_{12 \text{ times}}  \text{ kms}\\
& = & 40 \times 10^{12}  \text{ kms} \\ \\
\text{Number of stars on one side of the square} & = & \sqrt{250,000,000,000} \text{ stars} \\
& = & \sqrt{25 \times 10^{10}}  \text{ stars} \\ \\
\text{Now, using the laws of indices:} \\
\sqrt{25 \times 10^{10}} & = & (25 \times 10^{10})^{\frac{1}{2}} \\
& = & 25^{\frac{1}{2}} \times (10^{10})^{\frac{1}{2}} & & \text{Using 4th Law}\\
& = & (5^2)^{\frac{1}{2}} \times (10^{10})^{\frac{1}{2}} \\ 
& = & 5^{2\cdot \frac{1}{2}} \times 10^{10\cdot \frac{1}{2}}& & \text{Using 3rd Law}\\
& = & 5\times 10^5 \\ \\
\therefore \text{Size of the side of the square} & = & (5\times 10^5) \times (40 \times 10^{12}) \\
& = & 200 \times 10^5\times 10^{12} \\
& = & 200 \times 10^{5 + 12} & & \text{Using 1st Law}\\
& = & 200 \times 10^{17} \\
& = & 20 \times 10^{18} \\
\end{array}
{{< /katex >}}

So, thats our estimate of the diameter of the Milky Way Galaxy - \\( 20 \times 10^{18} \text{ kms} \\), which is not too far from the estimate that a [Google search](https://www.google.com/search?q=what+is+the+diameter+of+the+milky+way+galaxy+in+kms) yields.

More than the estimate, the key point is to note how the exponentiation notation saved us from having to write out very long sequences of digits for very large numbers throughout the calculation, and how the laws of indices helped us from doing the calculations easily.

## Very small numbers

Next lets see how the exponentiation notation and the laws of indices help us work with small numbers. Recall again the story of Reoh, who before his maiden flight had a fall in his backyard that jolted each one of the 37 trillion cells in his body.

Suppose we had to estimate the size of a Carbon atom fron the following:

 * The diameter of the nucleus of a cell is 0.000006 meters
 * The number of nucleotides packed within the nucleus is about 12,000,000,000
 * Each nucleotide is made up of roughly 15 atoms, mostly Carbon atoms.

The intent of these calculations are again not in order to arrive at the exact size of a Carbon atom, but really to show how the exponent notation and the laws of indices come in handy while handling very small numbers, just like they came in handy with handling very large numbers!

We will approximate the nucleus of a cell by a sphere, and each atom also by a sphere and neglect all spaces. This is depicted pictorially here:

{{< figure src="images/Cell-Nucleus.jpg" class="figs" title="Estimating the size of a Carbon atom." >}}

Without the exponentiation notation, our calculations might have looked as follows for the size of the atom:
$$ \sqrt[3]{(0.000,006)^3 \div 12,000,000,000 \div 15} $$

As before, to try and continue this calculation would be quite cumbersome, and our exponentiation notations come in handy.

{{< katex >}}
\begin{array}{rclcl}
\text{Diameter of the nucleus of the cell} & = & 0.000,006 \text{ m} \\
& = & 0.6 \times \underbrace{0.1\times 0.1\times 0.1\times 0.1 \times 0.1}_{5 \text{ times}}  \text{ m}\\
& = & 0.6 \times (0.1)^5 \\
& = & 6 \times 0.1 \times (0.1)^5 \\
& = & 6 \times (0.1)^6 & & \text{Using 1st Law}\\ \\
& = & 6 \times (\frac{1}{10})^6 \\ \\
& = & 6 \times \frac{1^6}{10^6} & & \text{Using 4th Law} \\ \\
& = & 6 \times \frac{1}{10^6} \\ \\
& = & 6 \times 10^{-6} & & \text{Using negative exponent defn} \\ \\
\therefore \text{Radius of the nucleus of the cell} & = & \displaystyle \frac{6 \times 10^{-6}}{2} \\ \\
& = & 3\times 10^{-6} \\ \\
\therefore \text{Volume of the nucleus of the cell} & = & \displaystyle \frac{4}{3}\pi (3 \times 10^{-6})^3 & & \text{Assuming the nucleus is a sphere}\\ \\
\text{Number of atoms in the nucleus of the cell} & = & 15 \times 12\times \underbrace{10\times 10\times 10\times \cdots \times 10}_{9 \text{ times}} \\ \\
& = & 15 \times 12\times 10^{9} \\ \\
& = & 180 \times 10^{9} \\ \\
\therefore \text{Volume of each atom} & = & \displaystyle \frac{\displaystyle \frac{4}{3}\pi (3 \times 10^{-6})^3}{180 \times 10^{9}} \\ \\
\therefore \displaystyle \frac{4}{3}\pi R_{\text{atom}}^3 & = & \displaystyle \frac{\displaystyle \frac{4}{3}\pi (3 \times 10^{-6})^3}{180 \times 10^{9}} & & \text{Assuming each atom is a sphere} \\ \\
\therefore \displaystyle \cancel{\frac{4}{3}}\pi R_{\text{atom}}^3 & = & \displaystyle \frac{\displaystyle \cancel{\frac{4}{3}\pi} (3 \times 10^{-6})^3}{180 \times 10^{9}} \\ \\
\therefore R_{\text{atom}} & = & \bigg\lbrack \displaystyle \frac{(3 \times 10^{-6})^3}{180 \times 10^{9}} \bigg\rbrack^{\frac{1}{3}} \\ \\
& = & \displaystyle \frac{((3 \times 10^{-6})^3)^{\frac{1}{3}}}{180^{\frac{1}{3}} \times (10^{9})^{\frac{1}{3}}} & & \text{Using 4th and 5th Law}\\ \\
& = & \displaystyle \frac{3 \times 10^{-6}}{180^{\frac{1}{3}} \times 10^3} & & \text{Using 3rd Law}\\ \\
\text{Now, } 5^3 & = & 125 \\
\text{And, } 6^3 & = & 216 \\
\text{So, for now, lets approximate, } 180^{\frac{1}{3}} & \approx & 6 \\ \\
\therefore R_{\text{atom}} & = & \displaystyle \frac{3}{6} \times \frac{10^{-6}}{10^3} \\ \\
& = & 0.5 \times 10^{-6-3} & & \text{Using 2nd Law} \\ \\
& = & 5 \times 0.1 \times 10^{-9} \\ \\
\therefore R_{\text{atom}} & = & 5 \times 10^{-10} \\ \\
\end{array}
{{< /katex >}}

So, thats our estimate of the radius of the Carbon atom - \\( 5 \times 10^{-10} \text{ m} \\), which is actually very close to the estimate that a [Google search](https://www.google.com/search?q=what+is+the+radius+of+a+carbon+atom+in+m) yields.

More than the estimate, the key point is to note how the exponentiation notation saved us from having to write out long sequences of decimal digits for very small numbers throughout the calculation, and how the laws of indices helped us from doing the calculations of such small numbers easily.

## Irrational numbers

So far, we have considered the base to be a positive number, and have steadily expanded the definition of exponentiation from positive integer exponents to zero and negative integer exponents, and then to rational exponents as well. Apart from providing us the ability to handle very large numbers and very small numbers, the exponentiation operation also gave rise to new kinds of numbers.

We know that the exponentiation of positive numbers, even just positive integers, to rational exponents gave rise to the discovery of new kind of numbers - the irrational numbers.

The very first irrational number to be discovered was of course \\(\sqrt{2}\\). We also know how this came about - in trying to find the length of the hypotenuse a right-angled triangle with both sides as 1, one had to find the square root of \\(2\\).

This discovery was made by a Greek mathematician Hippasus in 5th century BC, and legend has it that he was rewarded for this discovery by being thrown into the sea, simply becasue other mathematicians (they were really philosophers then) were scared of this new kind of number and did not know how to deal with it!

In general, the nth roots of almost all numbers (all integers except the nth powers, and all rationals except the quotients of two nth powers) are irrational. For eg, \\(\sqrt[3]{5}\\), \\(\sqrt[5]{3}\\) or \\({\frac{2}{3}}^{\frac{3}{2}}\\) are all of this kind. 

These numbers are called surds.

We may be a little suprised to find how many surds there are. Lets do a little experiment to find this out.

Suppose we were to take the number line and lets take the points representing the numbers 0 and 1. Suppose we mark 10 intervals between these points corresponding to the fractions \\(\frac{1}{10}, \frac{2}{10}, \ldots , \frac{9}{10} \\). This is depicted in the pic below. 

{{< figure src="images/How-dense-are-rationals-1.png" class="figs" title="Fractional points 0.1, 0.2, ... , 0.9 marked between 0 and 1" >}}

Now, you can draw this pic on a sheet of paper, take a pencil and randomly choose a point between 0 and 1 by touching the sheet of paper with closed eyes (If you are not on the line, you can simply go vertically up or vertically down to touch the line, and if you are outside of 0 and 1, you can just close your eyes and repeat this). What's your guess where the pencil will land - do you generally expect it to fall on one of the 10 points or is it more likely to fall in the space between the points?

You may probably correctly guess that the randomly chosen number is more likely to be in between these fractions, than exactly one of them.

What if we mark out points more closely, suppose we mark 100 intervals between these points corresponding to the fractions \\(\frac{1}{100}, \frac{2}{100}, \ldots, \frac{10}{100}, \frac{11}{100}, \ldots , \frac{90}{100}, \frac{91}{100}, \ldots , \frac{99}{100}\\). This is depicted in the pic below.

{{< figure src="images/How-dense-are-rationals-2.png" class="figs" title="Fractional points 0.01, 0.02, ... , 0.99 marked between 0 and 1" >}}

Now, we may start having some doubts. Maybe there is now a greater chance that the pencil will land on one of these 100 numbers, rather than in between them?

Well, lets take it one step further and make 1000 divisions, and mare out the corresponding numbers. This is shown in the figure below:

{{< figure src="images/How-dense-are-rationals-3.png" class="figs" title="Fractional points 0.001, 0.002, ... , 0.999 marked between 0 and 1" >}}

Now, we may be tempted to say that there is a very high chance that we will land on one of these 1000 numbers.

Surprisingly, that would be incorrect. The key is to notice that the above pictures are just approximations. The tics that we have drawn to depict the fractional points have a certain thickness, but in reality they should not have any thickness, because they are just points. And our pencil is also a very fine pointed pencil.

Even more suprising is the fact that even if divide the line between 0 and 1 into a billion intervals, and mark these fractions, these rational numbers using a very very very fine tip pencil, it turns out that the space between these numbers is way way more than the space occupied by the billion numbers themselves!

Thats the space that the surds occupy!!

As a result of this, contrary to our expectations, it turns out that there are way way more surds than there are rational numbers. When people realized this, it must have been a most mind boggling revelation.

We can get a glimpse here of why this is so. It is easy to list out the rational numbers between 0 and 1 as follows:
{{< katex >}}
\begin{array}{rclcl}
\text{Fractions with denominator 2} & \rarr & \frac{1}{2} \\ \\
\text{with denominator 3} & \rarr & \frac{1}{3}, \frac{2}{3} \\ \\
\text{with denominator 4} & \rarr & \frac{1}{4}, \frac{3}{4} \\ \\
\text{with denominator 5} & \rarr & \frac{1}{5}, \frac{2}{5}, \frac{3}{5}, \frac{4}{5} \\ \\
\text{with denominator 6} & \rarr & \frac{1}{6}, \frac{5}{6} \\ \\
\ldots \ldots
\end{array}
{{< /katex >}}

Note that we skipped \\(\frac{2}{4}\\) because that is already accounted for in \\(\frac{1}{2}\\). Likewise, we skipped \\(\frac{2}{6}\\), \\(\frac{3}{6}\\) and \\(\frac{4}{6}\\) as well.

(Technically speaking, as seen above, it is possible to create a mapping between integers and rational numbers. Hence the cardinality of the set of the integers and the set of rational numbers is said to be the same and they are called countably infinite. This is also denoted as \\(\aleph_0 \\)).

Now, lets try and write out irrational numbers, just to get a feel for how many of them are there. Lets start with \\( \sqrt{2}\\).

We can look at integer multiples of \\( \sqrt{2}\\), and they would all be irrational numbers:
$$ 2\sqrt{2}, 3\sqrt{2}, 4\sqrt{2}, \ldots $$
We can look at \\( \sqrt{2}\\) divided by integers, and they would all be irrational numbers:
$$ \frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{3}, \frac{\sqrt{2}}{4}, \ldots $$
In fact, we can take every rational number that we listed out above, and multiply it by \\( \sqrt{2}\\) and we will get a new irrational number:
$$ \frac{1}{2}\sqrt{2}, \frac{1}{3}\sqrt{2},\frac{2}{3}\sqrt{2},\frac{1}{4}\sqrt{2},\frac{3}{4}\sqrt{2},\frac{1}{5}\sqrt{2},\frac{2}{5}\sqrt{2},\frac{3}{5}\sqrt{2},\frac{4}{5}\sqrt{2},\ldots $$
And that is just with \\(\sqrt{2}\\). We can get more irrational numbers by raising \\(2\\) to other rational exponents, for eg:
$$ \sqrt[3]{2}, \sqrt[4]{2}, \sqrt[5]{2}, \ldots $$
And we can raise 2 to odd integers and then take a square root:
$$ \sqrt{2^3}, \sqrt{2^5}, \sqrt{2^7}, \ldots $$
Really, we can take each of the rational numbers above and raise \\(2\\) to it, to get a new irrational number:
$$ 2^\frac{1}{2}, 2^\frac{1}{3},2^\frac{2}{3},2^\frac{1}{4},2^\frac{3}{4},2^\frac{1}{5},2^\frac{2}{5},2^\frac{3}{5},2^\frac{4}{5},\ldots $$
Each and every one of these is a new irrational number, and we can take any one of them and repeat what we did earlier with \\(\sqrt{2}\\)!! For e.g, with \\(2^\frac{1}{4}\\), we can do the following:
$$ \frac{1}{2}2^\frac{1}{4}, \frac{1}{3}2^\frac{1}{4},\frac{2}{3}2^\frac{1}{4},\frac{1}{4}2^\frac{1}{4},\frac{3}{4}2^\frac{1}{4},\frac{1}{5}2^\frac{1}{4},\frac{2}{5}2^\frac{1}{4},\frac{3}{5}2^\frac{1}{4},\frac{4}{5}2^\frac{1}{4},\ldots $$
We can also add, we can subtract and get new irrational numbers, simply as:
$$ 1+\sqrt{2}, 2+\sqrt{2},3+\sqrt{2},4+\sqrt{2},\ldots $$
Or by adding each rational number we listed earlier as below:
$$ \frac{1}{2}+\sqrt{2}, \frac{1}{3}+\sqrt{2},\frac{2}{3}+\sqrt{2},\frac{1}{4}+\sqrt{2},\frac{3}{4}+\sqrt{2},\frac{1}{5}+\sqrt{2},\frac{2}{5}+\sqrt{2},\frac{3}{5}+\sqrt{2},\frac{4}{5}+\sqrt{2},\ldots $$
We can take the first of these and repeat everything we did so far, or for eg:
$$ \frac{1}{2}+\frac{1}{2}\sqrt{2}, \frac{1}{2}+\frac{1}{3}\sqrt{2},\frac{1}{2}+\frac{2}{3}\sqrt{2},\frac{1}{2}+\frac{1}{4}\sqrt{2},\frac{1}{2}+\frac{3}{4}\sqrt{2},\frac{1}{2}+\frac{1}{5}\sqrt{2},\ldots $$
It seems never ending. We can take one of these irrational numbers and find an n-th root of it, that is irrational again:
$$ \sqrt{1+\sqrt{2}}, \sqrt[3]{1+\sqrt{2}}, \sqrt[4]{1+\sqrt{2}}, \sqrt[5]{1+\sqrt{2}}, \ldots $$
And even now, we have only scratched the surface of these surds. We can add surds to get new surds:
$$ \sqrt{2}+\sqrt{3}, \sqrt{2}+\sqrt{5}, \sqrt{2}+\sqrt{3}+\sqrt{5}, \ldots $$
As you may start getting the idea, these surds are all over the place. We may not have encountered them so far, and may be they dont show up so much in our day to day life, but if you start digging deeper, they are way way way more in number than the rational numbers, in some ways exponentially more. And these are just one type of irrational numbers called algebraic irrationals, there is yet another type of irrationals called transcendtal irrationals.

We encountered this picture in the topic on Sets, and is reproduced below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/number sets.png" class="figs" title="Different kinds of numbers depicted as sets" >}}
<--->
{{< /columns >}}

Hopefully, this would have given you a good feel for the fact that if we randomly pick a number between 0 and 1, it is way way way more likely that it will be an irrational number than a rational number.

(Technically speaking, it is NOT possible to create a mapping between integers and irrational numbers. The cardinality of the set of the irrational numbers is said to be uncountably infinite. This is also denoted as \\(\aleph_1 \\)).

Since there are so many of these surds lying around, it make sense that we figure out how to deal with them, how to work with them, and in the process we will also discover some very interesting places where surds show up, in the next session.

## Complex numbers

Finally, when we started exploring exponents of negative numbers, a startling discovery opened up the entire new world of complex numbers. 

* We know well that a negative number raised to the power of an even integer is a positive number, for eg, \\((-5)^2 = 25 \\). A negative number raised to a negative exponent is also fairly simple \\((-5)^{-2} = \frac{1}{25} \\)
* We also know well that a negative number raised to the power an odd number is a negative number, for eg, \\((-5)^3 = -125 \\). Likewise, a negative number raised to a negative odd exponent \\((-5)^{-3} = \frac{-1}{125} \\).
* Around the 15th century, Italian mathematician Cardano (who was working on solving cubic equations) had the courage to ask what would happen if we raise a negative number to a rational number such as \\( (-1)^\frac{1}{2}\\) and that opened up the most fascinating new space of complex numbers.

The vastness of complex numbers is even more beautiful than the irrational numbers. But for now, we will stick to irrational numbers, specifically surds in the next session.

