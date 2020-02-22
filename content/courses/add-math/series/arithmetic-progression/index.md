---
title: "Arithmetic Progression"
date: 2020-01-22T20:59:08+05:30
draft: false
weight: 3
---

## AP basics

{{< highlight-box "Defn 1:" "none" "" "part" >}}
An Arithmetic Progression (or an AP) is a sequence of numbers such that the difference between consecutive terms is a constant.
{{< /highlight-box >}}

### Examples

Here are a few examples of APs:

- The sequence of odd natural numbers which is simply - \\( (1, 3, 5, 7, 9, \ldots ) \\) - is an AP, because the difference between any two consecutive terms is \\(2\\).
- The sequence of trees planted by the group of men where one new person joins the group every day is - \\( (10, 20, 30, 40, 50, \ldots ) \\) - is an AP, because the difference between any two consecutive terms is \\(10\\).

### Terms of the sequence

With just the definition above, we can write out the terms of the sequence. Suppose, the first term of the sequence is \\(a\\) and the difference between consecutive terms is \\(d\\), then the terms of the sequence can be written as follows:

{{< katex >}}
\begin{array}{rcl}
t_1 & = & a \\
t_2 & = & a + d \\
t_3 & = & a + 2\cdot d \\
& \vdots & \\
t_{k - 1} & = & a + (k - 2)\cdot d \\
t_k & = & a + (k - 1)\cdot d \\
t_{k + 1} & = & a + k \cdot d \\
& \vdots & \\
t_n & = & a + (n - 1)\cdot d \\
\end{array}
{{< /katex >}}

The first three terms of the sequence should be easy to see. We had assumed that the first term is \\(a\\). Since the difference between consecutive terms is \\(d\\), the second term becomes \\( a + d \\). Since the difference between the third term and the second term is again d, the third term becomes \\( a + d + d\\) or \\( a + 2\cdot d\\). 

We can continue in the same way, the fourth term would be \\( a + 2\cdot d + d \\) or \\( a + 3\cdot d\\), the fifth term would be \\( a + 4\cdot d\\) and so on. A general k-th term of the sequence can thus be determined as \\( a + (k - 1)\cdot d\\), and the n-th term is simply \\( a + (n - 1)\cdot d \\).

### k-th term of example APs

We can now write the above examples in the form of an AP, by determining the first term - \\( a \\) - and the constant difference - \\( d\\).

- For the sequence of odd natural numbers - \\( (1, 3, 5, 7, 9, \ldots ) \\):
  - The first term of the AP is \\( a = 1 \\).
  - The common difference of the AP is \\( d = 2 \\).
  - The k-th term of the AP can then be written as 
{{< katex >}}
\begin{array}{rcl}
t_k & = & 1 + (k - 1)\cdot 2 \\
& = & 2\cdot k - 1 \\
\end{array}
{{< /katex >}}
- For the sequence of trees planted each day - \\( (10, 20, 30, 40, 50, \ldots ) \\):
  - The first term of the AP is \\( a = 10 \\).
  - The common difference of the AP is (also) \\( d = 10 \\).
  - The k-the term of the AP can be written as
{{< katex >}}
\begin{array}{rcl}
t_k & = & 10 + (k - 1)\cdot 10 \\
& = & 10\cdot k \\
\end{array}
{{< /katex >}}

## Sum of the AP

We now like to find a general expression for the sum of n terms of an Arithmetic Progression.

{{< katex >}}
\begin{array}{rcl}
t_1 & = & a \\
t_2 & = & a + d \\
t_3 & = & a + 2\cdot d \\
& \vdots & \\
t_{k - 1} & = & a + (k - 2)\cdot d \\
t_k & = & a + (k - 1)\cdot d \\
t_{k + 1} & = & a + k \cdot d \\
& \vdots & \\
t_n & = & a + (n - 1)\cdot d \\ \\
\hline \\
S_n & = & n\cdot a + d + 2\cdot d + 3\cdot d + \cdots + (n - 1)\cdot d \\ \\
& = & n\cdot a + d\cdot (1 + 2 + 3 + \cdots + (n - 1)) \\
\end{array}
{{< /katex >}}

In order to find the sum of an AP, we need to be able to find a formula (also called a closed-form expression) for the sum of the first (n - 1) natural numbers, i.e. for the sum - \\( 1 + 2 + 3 + \cdots + (n - 1) \\).

### Other practical scenarios

The sum of the first n natural numbers (denoted by \\( T_n\\)) arises in other practical situations as well.

- If there are \\(n + 1\\) people in a room, and everyone shakes hands with all the rest, the total number of handshakes would be \\(T_n\\). This is because, the first person would shake hands with all the remaining \\(n\\) people, then the second person would shake hands with \\( n - 1 \\) people since the first person has already shaken hands with this second person, and so on.
- The same scenario arises in the round-robin stage of a tournament. If there are 6 teams in a pool and if each team has to play all the remaining teams in the pool, then the total number of matches would be \\( 5 + 4 + 3 + 2 + 1 \\).

### Young Gauss and his way

It is said that when Gauss was a young kid, and already showing his genius at Math and restlessness with his regular class, his teacher asked him to find the sum of all the numbers up to 100, with the hope that it will keep him occupied for a few hours. The story of course goes on to describe how Gauss is supposed to have turned around with the solution in a very short time baffling his teacher.

Whether the story is true or not is not known, but this method attributed to Gauss is definitely ingenious. The numbers from 1 to 100 are written in the reverse order to discover how easy the addition then becomes.

{{< katex >}}
\begin{array}{crcrcrcccrcr}
& 1 & + & 2 & + & 3 & + & \cdots & + & 99 & + & 100 \\
+ & \\
& 100 & + & 99 & + & 98 & + & \cdots & + & 2 & + & 1 \\ \\
\hline \\
= & 101 & + & 101 & + & 101 & + & \cdots & + & 101 & + & 101 \\
\end{array}
{{< /katex >}}

The sum of these terms is simply \\( 100\cdot 101 \\), and hence the sum of all the numbers from 1 to 100 turns out to be simply $$ \displaystyle \frac{1}{2}\cdot 100\cdot 101 $$.

### Visual representation

The sum of these numbers can also be visualized in the form of stacked boxes shown below:

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_natural_numbers_1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Now, lets take another set of boxes, exactly the same number as the initial set, just turned upside down and lets stack them upside down on these boxes.

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_natural_numbers_2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

What we get is a plain simple rectangle, where the total number of boxes is \\(5\cdot 6\\).
{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_natural_numbers_3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

From this we can figure out (no pun intended), that the original set of boxes occupies half the area in the rectangle, and hence the sum is $$ 1 + 2 + 3 + 4 + 5 = \frac{5\cdot 6}{2} $$

### Adding up averages

Yet another way to find the sum of these numbers is by looking at the average of the first and the last number, and then finding the difference of each of the numbers from this average number. For e.g.,

{{< katex >}}
\begin{array}{cccccccccccccc}
& 1 & + & 2 & + & 3 & + & 4 & + & 5 & + & 6 & + & 7 \\
\\
& & & & & & & & & 1 & + & 2 & + & 3 \\
= & 4 & + & 4 & + & 4 & + & 4 & + & 4 & + & 4 & + & 4 \\
& -3 & + & -2 & + & -1 & & & & & & & & \\
\\
= & 4 & + & 4 & + & 4 & + & 4 & + & 4 & + & 4 & + & 4 \\
\\
= & 7\cdot 4 \\
\\
= & 7\cdot \displaystyle \frac{1 + 7}{2}
\end{array}
{{< /katex >}}

Notice how the differences of the numbers from the average cancels out - the \\( 1 + 2 + 3 \\) cancels out with \\( -3 -2 - 1\\), leaving us with \\( 7\cdot 4\\), where \\( 4\\) is really the average of the first term and the last term.

You may wonder how it would work out when the sum invovles even numbers, you can try it out, it will just be a little bit messy with a lot of terms with \\( .5\\) in them, but the same principle will hold true.

The other way to see this visually is depicted in the figures below:

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_natural_numbers_with_averages_1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

As before, the average is 4, and we see that the last 3 numbers are higher than the average by as much as the first 3 numbers are lower than the average.

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_natural_numbers_with_averages_2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

So all those boxes can be moved into the empty space to make a neat rectangle of size \\(7\cdot 4\\).

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_natural_numbers_with_averages_3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

### Triangular numbers

These numbers are also commonly called as Triangular numbers and are depicted below in the form of an equilateral triangle.

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/First_six_triangular_numbers.svg" class="figs" title="" >}}
<--->
{{< /columns >}}

### Combinatorics here too

Finally, we find the sum of these numbers using Combinatorics. Let's say we have \\( n \\) students and we want to pick \\( 2 \\) volunteers from amongst them. How many ways are there to do that?

The first student can be picked along with one of the remaining students in \\(n - 1\\) ways- \\( (s_1, s_2), (s_1, s_3), (s_1, s_4), \ldots, (s_1, s_n) \\), or the second student can be picked along with one of the remaining students in \\( n - 2 \\) ways - \\( (s_2, s_3), (s_2, s_4), (s_2, s_5), \ldots, (s_2, s_n) \\), and so on.

But we also know that the number of ways to do this is simply \\( {}^nC_2 \\). Thus

$$ 1 + 2 + 3 + \cdots + (n - 1) = {}^nC_2 = \displaystyle \frac{(n - 1)\cdot n}{2} $$

We can go back and check that all the above approches to find the sum of the first few natural numbers leads to this same answer.

Now that we have our generic formula, we can go back to what we had started doing, and find the sum of the AP.

### Sum of the AP, finally

Resuming from where we had left this off earlier:

{{< katex >}}
\begin{array}{rcl}
t_1 & = & a \\
t_2 & = & a + d \\
t_3 & = & a + 2\cdot d \\
& \vdots & \\
t_{k - 1} & = & a + (k - 2)\cdot d \\
t_k & = & a + (k - 1)\cdot d \\
t_{k + 1} & = & a + k \cdot d \\
& \vdots & \\
t_n & = & a + (n - 1)\cdot d \\ \\
\hline \\
S_n & = & n\cdot a + d + 2\cdot d + 3\cdot d + \cdots + (n - 1)\cdot d \\ \\
& = & n\cdot a + d\cdot (1 + 2 + 3 + \cdots + (n - 1)) \\ \\
\therefore S_n & = & n\cdot a + \displaystyle d\cdot \frac{(n - 1)\cdot n}{2} \\
\end{array}
{{< /katex >}}

### Total number of trees

- For the sequence of trees planted each day - \\( (10, 20, 30, 40, 50, \ldots ) \\):
  - The first term of the AP is \\( a = 10 \\),
  - The common difference of the AP is (also) \\( d = 10 \\), and
  - The k-the term of the AP can be written as
{{< katex >}}
\begin{array}{rcl}
t_k & = & 10 + (k - 1)\cdot 10 \\
& = & 10\cdot k \\
\end{array}
{{< /katex >}}
  - The total number of trees planted in a year would be 
{{< katex >}}
\begin{array}{rcl}
S_{365} & = & 365\cdot 10 + \displaystyle 10\cdot \frac{364\cdot 365}{2} \\ \\
\therefore S_{365} & = & 70,080 \\
\end{array}
{{< /katex >}}

### Sum of odd numbers

- For the sequence of odd natural numbers - \\( (1, 3, 5, 7, 9, \ldots ) \\):
  - The first term of the AP is \\( a = 1 \\).
  - The common difference of the AP is \\( d = 2 \\).
  - The k-th term of the AP can then be written as 
{{< katex >}}
\begin{array}{rcl}
t_k & = & 1 + (k - 1)\cdot 2 \\
& = & 2\cdot k - 1 \\
\end{array}
{{< /katex >}}
  - The sum of n terms of the AP is:
{{< katex >}}
\begin{array}{rcl}
S_n & = & n\cdot 1 + \displaystyle 2\cdot \frac{(n - 1)\cdot n}{2} \\
& = & n + n^2 - n \\ \\
\therefore S_n & = & n^2 \\
\end{array}
{{< /katex >}}

This can be visualized using the picture shown below.
{{< columns "30,40,30" >}}
<--->
{{< figure src="images/sum_of_odd_numbers.png" class="figs" title="" >}}
<--->
{{< /columns >}}
Having added the first 4 odd numbers, to add the next odd number 9, we will be adding 9 unit squares to the right of the picture above to get a \\( 5 \text{ x } 5 \\) square, yielding the sum as 25.

## Summary

In summary, for an Arithmetic Progression with first term \\( a\\) and common difference \\( d\\), the general k-th term and the sum of first n-terms can be written as follows:

{{< katex >}}
\begin{array}{rcl}
t_k & = & a + (k - 1)\cdot d \\ \\
S_n & = & n\cdot a + d\cdot \displaystyle \frac{(n - 1)\cdot n}{2} \\ \\
S_n & = & \displaystyle n\cdot \frac{t_1 + t_n}{2} \\
\end{array}
{{< /katex >}}

