---
title: "Logarithm Basics"
date: 2020-08-09T08:50:14+05:30
draft: false
weight: 4
---

Having explored exponentials in great detail, we are now in a position to explore the world of Logarithms. 

Lets begin with the definition.

{{< highlight-box "Defn 1:" "none" "" "part" >}}
The **logarithm** of a given number \\( x\\) to a fixed number called a base, say \\(b\\), is the **exponent** to which the fixed number \\( b\\) must be raised to produce the given number \\(x\\), i.e.

$$ y = \log_b (x) \iff x = b^y $$

under the following conditions - \\( b > 0, b \neq 1 \text{, and } x > 0 \\)

{{< /highlight-box >}}

## Logarithm Examples

Lets understand this with a few examples. 

Suppose I give you a number, say \\( 1,000 \\) and ask you what is the logarithm of this number. The first question you have to ask me back is what is the base or the fixed number? Suppose I tell you that the base is \\( 10 \\). Then how do you go about finding the logarithm of the given number 1000 with the base 10?

To understand \\( \log_{10} (1,000) \\) better, lets go step by step from the definition:

 * The given number is \\( x = 1,000 \\)
 * The fixed number or the base is \\( b = 10 \\)
 * We note that \\( b > 0, b \neq 1 \text{, and } x > 0 \\), so all conditions for the definition are satisfied.
 * In order to find the logarithm of the given number \\( 1,000 \\) to the base \\( 10 \\), we have to find the *exponent* to which the base \\( 10 \\) must be raised to produce the given number \\( 1,000 \\).
 * Now, we know that \\( 10^3 \\) is equal to \\( 1,000 \\).
 * Hence the logarithm of the given number \\( 1,000 \\) to the fixed number or the base \\( 10 \\) is simply \\( 3 \\).

Thus,
$$ \log_{10} (1,000) = 3 $$

### log10 examples

Lets find the logarithms of more numbers with the base as \\( 10\\), as it is easy to do the calculation without the need for a calculator.

We know very well what the powers of \\( 10 \\) are as listed below:
{{< katex >}}
\begin{array}{rcl}
10^1 & = & 10 \\
10^2 & = & 100 \\
10^3 & = & 1,000 \\
10^4 & = & 10,000 \\
\ldots \\
10^8 & = & 100,000,000 \\
\ldots \\
\end{array}
{{< /katex >}}

The logarithm follows directly from these:
{{< katex >}}
\begin{array}{rclcrcl}
10^1 & = & 10 & \therefore & \log_{10} (10) & = & 1 \\ \\
10^2 & = & 100 & \therefore & \log_{10} (100) & = & 2 \\ \\
10^3 & = & 1,000 & \therefore & \log_{10} (1,000) & = & 3 \\ \\
10^4 & = & 10,000 & \therefore & \log_{10} (10,000) & = & 4 \\
\ldots \\
10^8 & = & 100,000,000 & \therefore & \log_{10} (100,000,000) & = & 8 \\
\ldots \\
\end{array}
{{< /katex >}}

### log2 examples

In the next set of examples below, lets use \\( 2\\) as the base, powers of \\( 2 \\) are again not that hard to calculate, as listed below:

{{< katex >}}
\begin{array}{rcl}
2^1 & = & 2 \\
2^2 & = & 4 \\
2^3 & = & 8 \\
2^4 & = & 16 \\
\ldots \\
2^8 & = & 256 \\
\ldots \\
\end{array}
{{< /katex >}}

The logarithm once again follows directly from these:
{{< katex >}}
\begin{array}{rclcrcl}
2^1 & = & 2 & \iff & \log_{2} (2) & = & 1 \\ \\
2^2 & = & 4 & \iff & \log_{2} (4) & = & 2 \\ \\
2^3 & = & 8 & \iff & \log_{2} (8) & = & 3 \\ \\
2^4 & = & 16 & \iff & \log_{2} (16) & = & 4 \\ \\
\ldots \\
2^8 & = & 256 & \iff & \log_{2} (256) & = & 8 \\ \\
\ldots \\
\end{array}
{{< /katex >}}

As before, to understand \\( \log_{2} (256) = 8 \\) better, it is good to note the following points with respect to the definition:

 * The given number is \\( x = 256 \\)
 * The fixed number or the base is \\( b = 2 \\)
 * We note that \\( b > 0, b \neq 1 \text{, and } x > 0 \\), so all conditions for the definition are satisfied.
 * In order to find the logarithm of the given number \\( 256 \\) to the base \\( 2 \\), we have to find the *exponent* to which the base \\( 2 \\) must be raised to produce the given number \\( 256 \\).
 * Now, we know that \\( 2^8 \\) is equal to \\( 256 \\).
 * Hence the logarithm of the given number \\( 256 \\) to the base or the fixed number \\( 2 \\) is simply \\( 8 \\).

Thus,
$$ \log_{2} 256 = 8 $$
Note that we do not need to have the bracket (around 256 above for example) when it is obvious what is the given number whose logartihm is being sought.

### log when x < b

In all the above examples, the given number \\( x \\) was greater than the fixed number \\( b \\). But the definition of logarithm does not have any constraint on this. 

So, lets take the fixed number as \\( b = 1000 \\), and try to find the logarithms in a few cases where the given number \\( x \\) is \\( < 1000 \\). What will be the values of these logarithms?

{{< katex >}}
\begin{array}{rcl}
\log_{1000} 100 & = & ? \\ \\
\log_{1000} 10 & = & ? \\ \\
\log_{1000} 1 & = & ? \\ \\
\end{array}
{{< /katex >}}

Take a minute to go back to the definition of logarithms and find these out carefully.

Lets consider \\( \log_{1000} (10) \\) and we note the following:

 * The given number is \\( x = 10 \\)
 * The fixed number or the base is \\( b = 1000 \\)
 * We note that \\( b > 0, b \neq 1 \text{, and } x > 0 \\), so all conditions for the definition are satisfied.
 * In order to find the logarithm of the given number \\( 10 \\) to the base \\( 1000 \\), we have to find the *exponent* to which the base \\( 1000 \\) must be raised to produce the given number \\( 10 \\).
 * Is is possible at all? Can we raise \\( 1000 \\) to some power and get \\( 10 \\). Indeed it is possible.
 * We know that \\( 1000 \\) is equal to \\( 10^3 \\), hence 

{{< katex >}}
\begin{array}{rclcl}
1000^\frac{1}{3} & = & (10^3)^\frac{1}{3} \\ \\
& = & 10^{(3\times \frac{1}{3})} & & \text{Using the 3rd Law - } (a^m)^n = a^{m\cdot n}\\ \\
& = & 10^1 \\ \\
& = & 10
\end{array}
{{< /katex >}}

Hence the logarithm of the given number \\( 10 \\) to the base or the fixed number \\( 1000 \\) is:
$$ \log_{1000} 10 = \displaystyle \frac{1}{3} $$

We can similarly write out the rest of the logarithms above:
{{< katex >}}
\begin{array}{rclcrcl}
\log_{1000} 100 & = & \displaystyle \frac{2}{3} & \because & 1000^\frac{2}{3} & = & (10^3)^\frac{1}{3} \\
& & & & & = & 10^{(3\times \frac{1}{3})} \\
& & & & & = & 10^2 \\
& & & & & = & 100 \\ \\
\log_{1000} 10 & = & \displaystyle \frac{1}{3} & \because & 1000^\frac{1}{3} & = & 10 \\ \\
\log_{1000} 1 & = & 0 & \because & 1000^0 & = & 1 \\ \\
\end{array}
{{< /katex >}}

### log of 1

The last example above is of particular interest. In fact we can take *any* fixed number \\( b \\) (satisfying the definition constraints of course), and we know that
$$ b^0 = 1 $$
Hence, we can say that if the given number is \\( 1\\), then the logarithm of the given number to any base is \\( 0 \\), i.e.
$$ \log_b 1 = 0 $$

### log when 0 < x < 1

In the definition of logarithm, we have a condition that the given number \\( x \\) should be \\( > 0\\), and the fixed number or the base \\( b\\) should also be \\( > 0 \\). But the result of finding the logarithm of the given number to a base number can perfectly well be negative. This happens only when \\( 0 < x < 1 \\).

We see a few examples of this below, using the base as \\( 10 \\):
{{< katex >}}
\begin{array}{rcl}
10^{-1} & = & 0.1 \\
10^{-2} & = & 0.01 \\
10^{-3} & = & 0.001 \\
\ldots \\
10^{-5} & = & \displaystyle \frac{1}{100,000} \\
\ldots \\
\end{array}
{{< /katex >}}

The logarithm follows directly from these, and note that the logarithm in each of these case is negative:
{{< katex >}}
\begin{array}{rclcrcl}
10^{-1} & = & 0.1 & \iff & \log_{10} 0.1 & = & -1 \\ \\
10^{-2} & = & 0.01 & \iff & \log_{10} 0.01 & = & -2 \\ \\
10^{-3} & = & 0.001 & \iff & \log_{10} 0.001 & = & -3 \\ \\
\ldots \\
10^{-5} & = & \displaystyle \frac{1}{100,000} & \iff & \log_{10} (\displaystyle \frac{1}{100,000}) & = & -5 \\ \\
\ldots \\
\end{array}
{{< /katex >}}

### log when x <= 0

Finally, if the given number \\( x\\) is \\( \leq 0 \\), then the logarithm of the given number is not defined. This is because no matter what base \\( b \\) we take, as long as the base is a real number, there is no way to raise the base to some power and get 0 or get a negative number.

Take a minute to think about it, if the base is real, there is no way to fill the boxes below with any number

{{< katex >}}
\begin{array}{rcl}
10^\Box & = & 0 \\
10^\Box & = & -1 \\
\end{array}
{{< /katex >}}

Hence the logarithm of negative numbers is undefined.

## Plotting Logarithm

Next, lets figure out how the graph of the logarithm function looks. 

### Graph of Exponential function

In order to do that we first start with the graph of the exponential function. We saw this briefly in the previous section, but lets go through it step by step here.

Lets use a fixed number or base of \\( 2 \\) and plot the graph of the function \\( 2^x \\). 

{{< columns >}}
<--->
{{< table "horizontal-table" >}}
| \\(x\\) | \\(2^x \\) |
| :-- | :-- |
| 1 | 2 |
| 2 | 4 |
| 3 | 8 |
| 4 | 16 |
| 5 | 32 |
| 6 | 64 |
| 7 | 128 |
| 8 | 256 |
{{< /table >}}
<--->
{{< table "horizontal-table" >}}
| \\(x\\) | \\(2^x \\) |
| :-- | :-- |
| -1 | 1/2 = 0.5 |
| -2 | 1/4 = 0.25 |
| -3 | 1/8 = 0.125 |
| -4 | 1/16 = 0.0625 |
| -5 | 1/32 ≈ 0.03125 |
| -6 | 1/64 ≈ 0 |
| -7 | 1/128 ≈ 0 |
| -8 | 1/256 ≈ 0 |
{{< /table >}}
<--->
{{< /columns >}}

In addition, we know that \\( 2^0 = 1 \\). We mark these points on the Cartesian co-ordinate system as shown below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/graph-of-2powx.png" class="figs" title="Points on the graph of 2^x" >}}
<--->
{{< /columns >}}

And then we connect up the points to get the graph of \\( 2^x \\):
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/graph-of-2powx-2.png" class="figs" title="Graph of 2^x" >}}
<--->
{{< /columns >}}

### Graph of Logarithm function

Now, we are ready to draw the graph of the Logarithm function. 

Lets draw up a table for the logarithm values. Recall that this follows from the definition of logarithms. If we know that \\( 2^3 = 8 \\), then that implies by definition that \\( \log_2 8 = 3 \\)

{{< columns >}}
<--->
{{< table "horizontal-table" >}}
| \\(x\\) | \\(2^x \\) |
| :-- | :-- |
| 3 | 8 |
| 2 | 4 |
| 1 | 2 |
| 0 | 1 |
| -1 | 0.5 |
| -3 | 0.125 |
| -5 | 1/32 |
| -7 | 1/128 |
{{< /table >}}
<--->
{{< table "horizontal-table" >}}
| \\(x\\) | \\(\log_2 (x) \\) |
| :-- | :-- |
| 8 | 3 |
| 4 | 2 |
| 2 | 1 |
| 1 | 0 |
| 0.5 | -1 |
| 0.125 | -3 |
| 1/32 | -5 |
| 1/128 | -7 |
{{< /table >}}
<--->
{{< /columns >}}

As before we can mark the points on the Cartesian coordinate system and then connect up the points to get the graph of \\( \log_2 (x) \\), as depicted in the picture below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/graph-of-2powx-log2x.png" class="figs" title="Graph of log2(x)" >}}
<--->
{{< /columns >}}

### Sections of the graph

As we saw in the examples on logarithms, we can mark out three sections of the graph as shown below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/graph-of-log2x-sections.png" class="figs" title="Sections on the graph of log2(x)" >}}
<--->
{{< /columns >}}

 * One colored in blue above, where the given number is greater than the base, i.e. \\( x > 2 \\), in this section the value of the logarithm is greater than 1,
 * Second colored in pink, where the given number is between 1 and the base, i.e. \\( 1 \leq x \leq 2 \\), in this section the value of the logarithm is a fraction between 0 and 1, and
 * Third colored in purple above, where the given number is less than 1 but still positive, i.e. \\( 0 < x < 1 \\), in this section, the value of the logarithm is negative.

Finally, we note as before that the value of the logarithm is not defined for \\( x \leq 0 \\).

### Log as inverse of Exp

The last concept we notice in the basics is the inverse function relationship between the logarithm and the exponential functions.

Recall the definition of the [inverse functions]({{< ref "inverse-function" >}}). Given a function, say \\( f \\) that maps some \\( x\\) to a value \\( y\\), if there is another function, say \\( g \\) which maps that \\( y \\) back to the original \\( x\\) and if that is true for each and every value of \\( x\\) mapped by the function \\( f\\), then the other function \\(g\\) is called the inverse function of \\(f\\). 

For the logarithm function, we note that this follows from the very definition of the logarithm in terms of the exponent. As we have seen above, the exponential function \\( 2^x \\) maps \\( x = 3\\) to the value \\( y = 2^3 = 8\\) and the logarithm function maps \\( x = 8 \\) back to the value \\( y = \log_2 8 = 3 \\). And this is true for each and every value of \\( x\\) mapped by the exponential function. Thus the logarithm function is the inverse of the exponential function.

{{< katex >}}
\begin{array}{lrcl}
\text{If } & f(x) & = & 2^x \\ \\
\text{Then }& f^{-1}(x) & = & \log_2 (x) \\
\end{array}
{{< /katex >}}

Also recall how the graph of the inverse function is a [reflection]({{< ref "inverse-function#finding-inverse-graphically" >}}) of the original function on the line \\( y = x\\). As expected, that is indeed the case with the graph of the exponential funciton and the corresponding logarithm function. This is shown in the picture below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/log2x-inverse-2powx.png" class="figs" title="2^x and log2(x) as reflections on y = x" >}}
<--->
{{< /columns >}}

Finally, recall how a function and its inverse are related using [function composition]({{< ref "inverse-function#another-definition" >}}). If a function \\(g\\) is the inverse of a function \\( f\\), then:

$$ (g\circ f)(x) = (f\circ g)(x) = x $$

From this, or even just using the definition of logarithms directly, we get the following relationships:

{{< katex >}}
\begin{array}{rcl}
b^{\log_b x} & = & x \\ \\
\log_b b^x & = & x
\end{array}
{{< /katex >}}

With that, we have uncovered a lot of basics on logarithms, and we now set to explore a few laws pertaining to logarithms.

