---
title: "Laws of Indices"
date: 2020-06-06T15:11:27+05:30
draft: false
weight: 2
---

First lets revisit the definition of exponentiation:

{{< highlight-box "Defn:" "none" "" "part" >}}
**Exponentiation** is simply repeated application of multiplication. Given a postive number \\(a\\) and a positive integer \\(m\\), we define \\(a^m\\) (pronounced "a power m") simply as:

$$ a^m = \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} $$
{{< /highlight-box >}}

Note that we are starting with both \\( a \\) and \\( m \\) as positive integers. As we go along, we will expand the realm of applicability of the exponentiation operation.

In this notation, \\(a\\) is called the base, and \\(m\\) is called the exponent or some times also called the index or the power. \\(a^m\\) itself is commonly pronounced in different ways - "a power m", or "m-th power of a", or "a raised to m", or briefly as "a to the m".

So, how does this definition help us? Note that this is only a notation, one that helps reduce the amount of writing we would need to do, and makes expression succinct.

It does not help us do any calculation any better or any faster. For e.g., if we have to find the value of \\( 7^4 \\), we still have to do the multiplication step by step:

{{< katex >}}
\begin{array}{rcl}
7^4 & = & 7 \times 7 \times 7 \times 7 \\
& = & 49 \times 7 \times 7 \\
& = & 343 \times 7 \\
& = & 2401 \\
\end{array}
{{< /katex >}}

Now suppose we want to find the value of the \\( 2^3 \times 2^4 \\). We could do that as follows from the definition:

{{< TODO >}}
{{< katex >}}
\begin{array}{lrcl}
\text{First} & 2^4 & = & 2 \times 2 \times 2 \times 2 \\
& & = & 4 \times 2 \times 2 \\
& & = & 8 \times 2 \\
& & = & 16 \\
\text{Next} & 2^6 & = & 2 \times 2 \times 2 \times 2 \times 2 \times 2 \\
& & = & 4 \times 2 \times 2 \times 2 \times 2 \\
& & = & \cdots \\
& & = & 64 \\
\text{Hence} & 2^4 \times 2^6 & = & 16 \times 64 \\
& & = & 1024 \\
\end{array}
{{< /katex >}}
{{< /TODO >}}

{{< katex >}}
\begin{array}{lrcl}
\text{First} & 2^3 & = & 2 \times 2 \times 2 \\
& & = & 4 \times 2 \\
& & = & 8 \\
\text{Next} & 2^4 & = & 2 \times 2 \times 2 \times 2 \\
& & = & 4 \times 2 \times 2 \\
& & = & 8 \times 2 \\
& & = & 16 \\
\text{Hence} & 2^3 \times 2^4 & = & 8 \times 16 \\
& & = & 128 \\
\end{array}
{{< /katex >}}

Now, independently, we can find the value of \\( 2^7 \\) by multiplying \\( 2\\) repeatedly  \\( 7 \\) times. We find that the value is indeed the same, i.e. \\( 128 \\).

This is because:
{{< katex >}}
\begin{array}{rcl}
2^3 \times 2^4 & = & \underbrace{2 \times 2 \times 2}_{3\text{ times}} \times \underbrace{2 \times 2 \times 2 \times 2}_{4\text{ times}} \\ \\
& = & \underbrace{2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2}_{7\text{ times}} \\ \\
& = & 2^7 \\
\end{array}
{{< /katex >}}


This should not come as much of a surpise, and it gives us the first of the laws of indices.

## The First Law

{{< theorem-block "1st Law" "Proof" >}}
$$a^m \times a^n = a^{m + n} $$
<--->

The proof is fairly simple and follows from the definition, especially for integer values of \\(m\\) and \\(n\\):

{{< katex >}}
\begin{array}{rcl}
a^m\times a^n & = & \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} \times \underbrace{a \times a \times \cdots \times a}_{n\text{ times}} \\ \\
& = & \underbrace{a \times a \times a \times \cdots \times a \times a \times a \times \cdots \times a}_{(m + n)\text{ times}} \\ \\
& = & a^{m + n}
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

We can ask again, how this helps us and we will see that this helps simplify calculations wonderfully.

We had calcualted \\(7^4\\) by repeatedly multiplying \\(7\\) one at a time. But now, we can use the first law to speed it up.
{{< katex >}}
\begin{array}{rcl}
7^4 & = & 7^2 \times 7^2 \\
& & \text{(by using the first law)} \\
& = & 49 \times 49 \\
& = & 2401 \\
\end{array}
{{< /katex >}}

Well that is only 2 multiplications - once to find \\(7 \times 7\\) and another time to find \\( 49 \times 49\\), as compared to 3 multiplications that we did before - first to find \\(7 \times 7\\), then to find \\(49 \times 7\\) and finally to find \\(343 \times 7\\).

### Fast exponentiation
This idea can be extended further in a very nice and systematic way. Suppose, we have to find the value of \\( 2^{30} \\). What is the smallest number of multiplications that we need to perform? Do we need to do all of 29 multiplications to find out the value of this? Turns out no, and one of the ways to look at this is by applying the first law of indices that we just saw.

The key is to note that \\( 30 = 16 + 8 + 4 + 2 \\), and to find \\( 2^2\\), \\(2^4\\), \\(2^8\\), and \\(2^{16}\\) successively needs 4 multiplications in all, and then to find \\(2^{30}\\), we need to perform 3 more multiplication operations. This is illustrated below step by step:

{{< katex >}}
\begin{array}{rclcl}
2^2 & = & 2^{1+1} \\
& = & 2^1 \times 2^1 \\
& = & 2 \times 2 & \text{-->} & \text{1st multiplication} \\
& = & 4 \\ \\
2^4 & = & 2^{2+2} \\ 
& = & 2^2 \times 2^2 \\ 
& = & 4 \times 4 & \text{-->} & \text{2nd multiplication} \\
& = & 16 \\ \\
2^8 & = & 2^{4+4} \\
& = & 2^4 \times 2^4 \\ 
& = & 16 \times 16 & \text{-->} & \text{3rd multiplication} \\
& = & 256 \\ \\
2^{16} & = & 2^{8+8} \\
& = & 2^8 \times 2^8 \\
& = & 256 \times 256 & \text{-->} & \text{4th multiplication} \\
& = & 65,536 \\ \\
2^{30} & = & 2^{16+8+4+2} \\
& = & 2^{16} \times 2^8 \times 2^4 \times 2^2 \\ 
& = & 65,536 \times 256 \times 16 \times 4 & \text{-->} & \text{5th multiplication} \\
& = & 16,777,216 \times 16 \times 4 & \text{-->} & \text{6th multiplication} \\
& = & 268,435,456 \times 4 & \text{-->} & \text{7th multiplication} \\
& = & 1,073,741,824
\end{array}
{{< /katex >}}

Thus we see that using the First Law smartly has helped us go through this calculation in a short number of steps, just 7 instead of the 29 steps we would have had to. Can you guess what is the minimum number of multiplications needed for computing \\(2^{100}\\)?

## The Second Law

The second law of indices can also be stated and proved easily 

{{< theorem-block "2nd Law" "Proof" >}}
$$a^m \div a^n = a^{m - n} $$
<--->

The proof is fairly simple and follows from the definition, especially for integer values of \\(m\\) and \\(n\\) and when \\( m > n \\):

{{< katex >}}
\begin{array}{rcl}
a^m\div a^n & = & \displaystyle \frac{\overbrace{a \times \cdots \times a \times a \times a \times \cdots \times a}^{m\text{ times}}}{\underbrace{a \times a \times \cdots \times a}_{n\text{ times}}} \\ \\
& = & \displaystyle \frac{{a \times \cdots \times \sout{a \times a \times \cdots \times a \times a}}}{\sout{a \times a \times \cdots \times a}} \\ \\
& & \text{Since m is greater than n, all the n a's in the denominator} \\
& & \text{can be cancelled out with n a's in the numerator, and} \\
& & \text{we will be left with m - n a's in the numerator} \\ \\
& = & \underbrace{a \times \cdots \times a}_{(m - n)\text{ times}} \\ \\
& = & a^{m - n}
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

What this means is that to compute lets say the value of $$ \frac{2^{30}}{2^{20}} $$ it is not necessary to compute the values of the numerator and denominator separately and then do a long division like below: $$ \frac{2^{30}}{2^{20}} = \frac{1,073,741,824}{1,048,576} = 1,024 $$
We can simply do the following: $$ \frac{2^{30}}{2^{20}} = 2^{30-20} = 2^{10} = 1,024 $$

But this throws up an interesting question. Do we expect this law to work when \\(m\\) is equal to \\( n\\)? What if \\( m\\) is less than \\(n\\)? The point is that we only started with postiive values of the exponent, we havent defined what it means to have the exponent as \\(0\\), or as a negative integer. We can do that now.

### Negative exponentiation

In order to understand this, let us go back to our original definition again. We defined 
$$ a^m = \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} $$
for positive integer values of \\(m\\). For example, this means:

{{< katex >}}
\begin{array}{rcl}
2^1 & = & 2 \\
2^2 & = & 2\times 2 \\
2^3 & = & 2\times 2\times 2 \\
2^4 & = & 2\times 2\times 2\times 2\\
\cdots \\
2^m & = & \underbrace{2\times 2\times 2\times \cdots \times 2}_{m \text{ times}} \\
\end{array}
{{< /katex >}}

But this can also be rewritten as follows, eah subsequent term is got by multiplying the previous term by \\(2\\).
{{< katex >}}
\begin{array}{rcl}
2^1 & = & 2 \\
2^2 & = & 2^1\times 2 \\
2^3 & = & 2^2\times 2 \\
2^4 & = & 2^3\times 2 \\
\cdots \\
2^m & = & 2^{m - 1}\times 2 \\
\end{array}
{{< /katex >}}

But multiplication in one way is division in the other way.

So, we can rewrite the above in the reverse order as follows:
{{< katex >}}
\begin{array}{rcl}
2^{m-1} & = & 2^m \div 2 \\
\cdots \\
2^4 & = & 2^5\div 2 \\
2^3 & = & 2^4\div 2 \\
2^2 & = & 2^3\div 2 \\
2^1 & = & 2^2\div 2 \\
\end{array}
{{< /katex >}}

Now, it should be clear how we can extend the definition of indices to 0 and further on to negative numbers. We simply extend the above as follows:
{{< katex >}}
\begin{array}{rcl}
2^3 & = & 2^4\div 2 \\
2^2 & = & 2^3\div 2 \\
2^1 & = & 2^2\div 2 \\
2^0 & = & 2^1\div 2 \\
2^{-1} & = & 2^0\div 2 \\
2^{-2} & = & 2^{-1}\div 2 \\
2^{-3} & = & 2^{-2}\div 2 \\
\end{array}
{{< /katex >}}

In other words, we have the following:
{{< katex >}}
\begin{array}{rcl}
2^0 & = & 1 \\ \\
2^{-1} & = & \displaystyle \frac{1}{2} \\ \\
2^{-2} & = & \displaystyle \frac{1}{2^2} \\ \\
2^{-3} & = & \displaystyle \frac{1}{2^3} \\
\cdots \\
2^{-m} & = & \displaystyle \frac{1}{2^m} \\
\end{array}
{{< /katex >}}

Now, we *choose* to extend the original definition that we made as follows:

{{< highlight-box "Defn:" "none" "" "part" >}}
Given a postive number \\(a\\) and a positive integer \\(m\\), we define the following:

{{< katex >}}
\begin{array}{rclcl}
a^m & = & \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} \\ \\
a^0 & = & 1 & & \text{if } a \neq 0\\ \\
a^{-m} & = & \displaystyle \frac{1}{a^m} & & \text{if } a \neq 0\\ \\
\end{array}
{{< /katex >}}

{{< /highlight-box >}}

## The Third Law

The third law of indices is stated below and is simple to prove again for positive indices.

{{< theorem-block "3rd Law" "Proof" >}}
$$(a^m)^n = a^{m.n} $$
<--->

The proof is fairly simple and follows from the definition for integer values of \\(m\\) and \\(n\\):

{{< katex >}}
\begin{array}{rcl}
(a^m)^n & = & (\underbrace{a \times a \times \cdots \times a}_{m\text{ times}})^n  \\ \\
& = & \underbrace{\underbrace{a \times a \times \cdots \times a}_{m\text{ times}}\times \underbrace{a \times a \times \cdots \times a}_{m\text{ times}} \times \cdots \times \underbrace{a \times a \times \cdots \times a}_{m\text{ times}}}_{n\text{ times}} \\ \\
& = & \underbrace{a \times a \times \cdots \times a\times a \times a \times \cdots \times a \times \cdots \times a \times a \times \cdots \times a}_{m.n\text{ times}} \\ \\
& = & a^{m.n}
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

It should be easy to see that this law would hold true even if \\(m\\) is negative or \\(n\\) is negative or even if both are negative. Lets see, for eg, what happens if the outer exponent is negative (assume that \\(m\\) and \\(n\\) are positive, hence \\(-n\\) is negative below):

{{< katex >}}
\begin{array}{rclcl}
(a^m)^{-n} & = & \displaystyle \frac{1}{(a^m)^n} & & \text{using the definition for negative exponents} \\ \\
& = & \displaystyle \frac{1}{a^{m.n}} & & \text{using the third law for positive exponents} \\ \\
& = & a^{-m.n} & & \text{using the definition for negative exponents again}
\end{array}
{{< /katex >}}

In other words, as expected, the 3rd law holds true even if \\(n\\) is negative. In the same way we can check that it holds true even if the inner exponent is negative or if both the exponents are negative.

### Squares and Cubes

It is interesting to note how we have given special names to exponent of \\(2\\) and exponent of \\(3\\). For example \\(5^2\\) is hardly ever referred to as "five to the power 2", and is most commonly referred to as "5-squared". Similarly, 4^3 is hardly ever referred to as "four to the power of 3", and is most commonly referred to as "4-cubed". Ever wondered why?

It has a very simple reason. The area of a square is side x side, or side^2, so anything to the power 2 started being called squared. Likewise, because the volume of a cube is side x side x side or "side to the power 3", so the name "cubed" stuch for anything to the power 3.

### Rational exponentiation

An interesting question that people started asking long ago was the reverse of exponentiation in some ways. That is the following:

If we are given the number \\(25\\), and want to ask if there is a number when repeatedly multiplied \\( 2\\) times would give \\(25\\). We know very well what the answer to that question is, that number is \\(5\\) because: $$ 5^2 = \underbrace{5\times 5}_{2 \text{ times}} = 25 $$ For now, we are only considering positive bases.

Similarly, if we are given the number say \\(343\\), is there a number when repeatedly nultiplied \\(3\\) times would \\(343\\)? This may take a little effort, btu the answer to this question is \\(7\\), becuase: $$ 7^3 = \underbrace{7\times 7\times 7}_{3 \text{ times}} = 343 $$

We can ask a little harder question, for e.g., is there a number when repeatedlty multiple \\(2\\) times would give \\(30\\). Today, we can use a calculator to easily find out, but in olden days when this thought came up, one would have had to say \\(5^2 = 25\\) and \\(6^2 = 36\\), so *this number we are looking for* should be between \\(5\\) and \\(6\\). Then we could try with \\(5.5^2 = 30.25 \\), so *this number that we are looking for* should be between \\(5\\) and \\(5.5\\).

As you may have noticed, it is getting cumbersome to repeatedly keep saying "this number that we are looking for", or "this number which when repeatedly multiplied twice would give thirty", and that calls for a new notation. The original choice of notation was the \\(\sqrt{}\\) sign (called the radical sign) but the real obvious choice for this notation was a rational exponent, and both of these have stuck through history. Using the notation, we would say:

{{< katex >}}
\begin{array}{rcl}
\sqrt{30}\times \sqrt{30} & = & 30 \\ \\
\text{or equivalently} \\ \\
30^{\frac{1}{2}}\times 30^{\frac{1}{2}} & = & 30 \\
\end{array}
{{< /katex >}}

We can take one more example with this notation. The number which when multiplied repeatedly by itself \\(3\\) times yields \\(343\\) is denoted by \\(343^{\frac{1}{3}}\\) or equivalently \\(\sqrt[3]{343}\\). And since we know that \\(7^3 = 343\\), therefore \\(343^{\frac{1}{3}} = 7\\) or said in an other way \\(\sqrt[3]{343} = 7\\). 

As we know well this is called the square-root and the cube-root respectively of a number. Similarly, we can also find the \\(m\text{-th}\\) root of a number. The term root comes because finding say the fourth-root of \\(25\\) is synonymous with solving the polynomial equation $$ x^4 - 25 = 0$$
or finding the point(s) where the graph of the function \\( y = x^4 - 25\\) cuts the x-axis!

We are thus set to expan our definitions as follows

{{< highlight-box "Defn:" "none" "" "part" >}}
Given a postive number \\(a\\) and a positive integer \\(m\\), we define the following:

{{< katex >}}
\begin{array}{rclcl}
a^m & = & \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} \\ \\
\underbrace{a^{\frac{1}{m}} \times a^{\frac{1}{m}} \times a^{\frac{1}{m}} \times \cdots \times a^{\frac{1}{m}}}_{m\text{ times}} & = & a\\ \\
a^0 & = & 1 & & \text{if } a \neq 0\\ \\
a^{-m} & = & \displaystyle \frac{1}{a^m} & & \text{if } a \neq 0\\ \\
\end{array}
{{< /katex >}}

{{< /highlight-box >}}

This definition combined with the 3rd law gives us the following identities:
$$ a^{\frac{m}{n}} = a^{m\frac{1}{n}} = (a^m)^{\frac{1}{n}} = \sqrt[n]{a^m} $$
$$ a^{\frac{m}{n}} = a^{\frac{1}{n}m} = (a^{\frac{1}{n}})^m = (\sqrt[n]a)^m $$


## The Fourth Law

In the first and the second law, we dealt with multiplication and division where the base was the same, and the exponents were different. We can ask the question, what happens if we multiply/divide two quantities where the bases are different but the exponents are the same. That's the next two laws and is fairly easy to see for integer exponents.

{{< theorem-block "4th Law" "Proof" >}}
$$a^m \cdot b^m = (a\cdot b)^m $$
<--->

The proof is fairly simple and follows from the definition, especially for integer values of \\(m\\):

{{< katex >}}
\begin{array}{rcl}
a^m\cdot b^m & = & \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} \times \underbrace{b \times b \times b \times \cdots \times b}_{m\text{ times}} \\ \\
& = & \underbrace{(a \times b) \times (a \times b) \times (a \times b) \times \cdots \times (a \times b)}_{m \text{ times}} \\ \\
& = & (a\cdot b)^m
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

## And a Fifth Law

And finally, we end with a fifth law which can be derived from all of the above four laws instead of from first principles:

{{< theorem-block "5th Law" "Proof" >}}
$$\displaystyle \frac{a^m}{b^m} = (\displaystyle \frac{a}{b})^m $$
<--->

The proof is fairly simple and this time instead of doing it from the original definition we can derive this law from the previous laws that we have already learnt:

{{< katex >}}
\begin{array}{rclcl}
\displaystyle \frac{a^m}{b^m} & = & a^m \times b^{-m} & & \text{Using negative exponent defn} \\ \\
& = & a^m \times b^{-1\cdot m} \\ \\
& = & a^m \times (b^{-1})^m & & \text{Using the 3rd Law} \\ \\
& = & (a\times b^{-1})^m & & \text{Using the 4th Law} \\ \\
& = & (\displaystyle \frac{a}{b})^m
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

Now, lets put what we have learnt so far to some good use.
