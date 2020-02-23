---
title: "Geometric Progression"
date: 2020-01-22T20:59:23+05:30
draft: false
weight: 4
---

## GP basics

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A **Geometric Progression** (or a GP) is a sequence of numbers such that the ratio between consecutive terms is a constant.
{{< /highlight-box >}}

Note that the constant can be a positive natural number (such as 10), or a fractional number (such as 1/2 or 0.25, etc), or even a negative number (such as -2).

### Examples

Here are a few examples of APs:

- The sequence of powers of two which is simply - \\( (1, 2, 4, 8, 16, \ldots ) \\) - is a GP, because the ratio between any two consecutive terms is \\(2\\).
- The sequence of trees planted by the group of men where each person gets a new person every day is - \\( (10, 20, 40, 80, 160, \ldots ) \\) - is a GP, because the ratio between any two consecutive terms is again \\(2\\).

### Terms of the sequence

With just the definition above, we can write out the terms of the sequence. Suppose, the first term of the sequence is \\(a\\) and the ratio between consecutive terms is \\(r\\), then the terms of the sequence can be written as follows:

{{< katex >}}
\begin{array}{rcl}
t_1 & = & a \\
t_2 & = & a \cdot r \\
t_3 & = & a \cdot r^2 \\
& \vdots & \\
t_{k - 1} & = & a \cdot r^{k-2} \\
t_k & = & a \cdot r^{k-1} \\
t_{k + 1} & = & a \cdot r^k \\
& \vdots & \\
t_n & = & a \cdot r^{n - 1} \\
\end{array}
{{< /katex >}}

The first three terms of the sequence should be easy to see. We had assumed that the first term is \\(a\\). Since the ratio between consecutive terms is \\(r\\), the second term becomes \\( a \cdot r \\). Since the ratio between the third term and the second term is again r, the third term becomes \\( a \cdot r \cdot r\\) or \\( a \cdot r^2 \\). 

We can continue in the same way, the fourth term would be \\( a \cdot r^2 \cdot r \\) or \\( a \cdot r^3\\), the fifth term would be \\( a \cdot r^4\\) and so on. A general k-th term of the sequence can thus be determined as \\( a \cdot r^{k - 1} \\), and the n-th term is simply \\( a \cdot r^{n - 1} \\).

### k-th term of example GPs

We can now write the above examples in the form of a GP, by determining the first term - \\( a \\) - and the constant ratio - \\( r\\).

- For the sequence of powers of 2 - \\( (1, 2, 4, 8, 16, \ldots ) \\):
  - The first term of the AP is \\( a = 1 \\).
  - The common difference of the AP is \\( r = 2 \\).
  - The k-th term of the GP can then be written as 
{{< katex >}}
\begin{array}{rcl}
t_k & = & 1 \cdot 2^{k - 1} \\
& = & 2^{k - 1} \\
\end{array}
{{< /katex >}}
- For the sequence of trees planted each day - \\( (10, 20, 40, 80, 160, \ldots ) \\):
  - The first term of the GP is \\( a = 10 \\).
  - The common ratio of the GP is \\( r = 2 \\).
  - The k-the term of the GP can be written as
{{< katex >}}
\begin{array}{rcl}
t_k & = & 10 \cdot 2^{k - 1} \\
\end{array}
{{< /katex >}}

## Sum of the GP

We now like to find a general expression for the sum of n terms of a Geometric Progression. And the way to find that involves a small trick.

{{< katex >}}
\begin{array}{rcl}
S_n & = & a + a\cdot r + a\cdot r^2 + a\cdot r^3 + \cdots + a\cdot r^{n - 1} \\ \\
\therefore r\cdot S_n & = & a\cdot r + a\cdot r^2 + a\cdot r^3 + \cdots + a\cdot r^{n - 1} + a\cdot r^n \\ \\
& & \text{Subtracting the two equations above} \\ \\
\therefore S_n - r\cdot S_n & = & a - a\cdot r^n \\ \\
\therefore S_n & = & a\cdot \displaystyle \frac{1 - r^n}{1 - r} \\ \\
\end{array}
{{< /katex >}}

### Sum of powers of 2

- For the sequence of powers of 2 - \\( (1, 2, 4, 8, 16, \ldots ) \\):
  - The first term of the AP is \\( a = 1 \\).
  - The common difference of the AP is \\( r = 2 \\).
  - The k-th term of the GP can then be written as 
{{< katex >}}
\begin{array}{rcl}
t_k & = & 1 \cdot 2^{k - 1} \\
& = & 2^{k - 1} \\
\end{array}
{{< /katex >}}
  - The sum of n terms of the GP (and for n = 5) is:
{{< katex >}}
\begin{array}{rcl}
S_n & = & 1\cdot \displaystyle \frac{1 - 2^n}{1 - 2} \\ \\
S_5 & = & 31 \\
\text{Also check, } \\
1 + 2 + 4 + 8 + 16 & = & 31 \\
\end{array}
{{< /katex >}}


### Total number of trees

- For the sequence of trees planted each day - \\( (10, 20, 40, 80, 160, \ldots ) \\):
  - The first term of the GP is \\( a = 10 \\).
  - The common ratio of the GP is \\( r = 2 \\).
  - The k-the term of the GP can be written as
{{< katex >}}
\begin{array}{rcl}
t_k & = & 10 \cdot 2^{k - 1} \\
\end{array}
{{< /katex >}}
  - The total number of trees planted in a month would be 
{{< katex >}}
\begin{array}{rcl}
S_{30} & = & 10\cdot \displaystyle \frac{1 - 2^{30}}{1 - 2} \\ \\
\therefore S_{30} & = & 10,737,418,230 \\
\end{array}
{{< /katex >}}

That's a total of over 10million trees in just a month!!!

### Plotting a GP

We can plot the above GP as points on a graph as shown below.

{{< figure src="images/plot_points_of_a_GP.png" class="figs" title="" >}}

Notice how each term of the GP falls on the exponential function curve - \\( y = 10\cdot 2^x \\).

### GP with ratio < 1

Consider the following GP with a = 1, r = 1/2, what will the sum of this GP be?
$$ 1, \frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \ldots $$

The sum of the GP for n-terms can be found using the formula:
$$ S_n = 1\cdot \frac{1 - (\frac{1}{2})^n}{1 - \frac{1}{2}} $$

As \\(n\\) becomes very large, the term \\( (\frac{1}{2})^n \\) becomes very small, almost close to \\( 0\\). In mathematical notation, this is written as follows:
$$ \text{As } n \to \infty \text{ , } (\frac{1}{2})^n \to 0 $$

{{< katex >}}
\begin{array}{rcl}
\therefore S_{\infty} & = & 1\cdot \displaystyle \frac{1 - 0}{1 - \frac{1}{2}} \\
& = & 2
\end{array}
{{< /katex >}}

What is interesting is that the series with an infinite number of terms still converges to a finite number, this is so because the common ratio of the GP is < 1.

We can also visualize this using the picture below, the series is the same as the total area of the rectangle:

{{< figure src="images/Geometric_progression_convergence_diagram.svg" class="figs" title="" >}}

## Summary

In summary, for a Geometric Progression with first term \\( a\\) and common ratio \\( r\\), the general k-th term and the sum of first n-terms can be written as follows:

{{< katex >}}
\begin{array}{rcl}
t_k & = & a \cdot r^{k - 1} \\ \\
S_n & = & a\cdot \displaystyle \frac{1 - r^n}{1 - r} \\ \\
\end{array}
{{< /katex >}}


