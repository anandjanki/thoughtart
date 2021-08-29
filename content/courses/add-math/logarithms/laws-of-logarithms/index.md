---
title: "Laws of Logarithms"
date: 2020-08-08T12:27:06+05:30
draft: false
weight: 5
---

We have already come across the following properties from the basics of logarithms:
{{< katex >}}
\begin{array}{rcl}
\log_b 1 & = & 0 \\ \\
\log_b b & = & 1 \\ \\
b^{\log_b x} & = & x \\ \\
\log_b b^x & = & x
\end{array}
{{< /katex >}}

We now derive the following laws from the basic definition of Logarithm, the [Laws of Indices]({{ref "laws-of-indices"}}) and the above properties:
{{< katex >}}
\begin{array}{rcl}
\log_b (x\cdot y) & = & \log_b (x) + \log_b (y) \\ \\
\displaystyle \log_b (\frac{x}{y}) & = & \log_b (x) - \log_b (y) \\ \\
\log_b (x^y) & = & y\cdot \log_b (x) \\
\end{array}
{{< /katex >}}

## The First Law

{{< theorem-block "1st Law" "Proof" >}}
$$ \log_b (x\cdot y) = \log_b (x) + \log_b (y) $$
<--->

The proof is fairly simple and starts as follows:

{{< katex >}}
\begin{array}{lrcl}
\text{Let } & x & = & b^u \\ \\
\text{And let } &  y & = & b^v \\ \\
\end{array}
{{< /katex >}}

Note that, from the definition of Logarithms, \\(b > 0 \text{ and } b \neq 1\\) as always, \\(x\\) and \\(y\\) have to be positive, and since they are positive, it is possible to find \\(u\\) and \\(v\\), which can be positive, zero or negative such that the above are satisfied. Then we proceed as follows:

{{< katex >}}
\begin{array}{lclr}
\text{LHS } & = & \log_b (x\cdot y) & \\ \\
& = & \log_b (b^u \cdot b^v) & \text{by substitution above}\\ \\
& = & \log_b (b^{(u+v)}) & \text{by Laws of Indices}\\ \\
& = & u+v & \text{by Basics of Logarithms}\\ \\
& = & \log_b (x) + \log_b (y) & \text{by definition of Logarithm}\\ \\
& = & \text{RHS} \\
\end{array}
{{< /katex >}}

{{< /theorem-block >}}


## The Second Law

{{< theorem-block "2nd Law" "Proof" >}}
$$ \log_b (\frac{x}{y}) = \log_b (x) - \log_b (y) $$
<--->

The proof is fairly simple and works the same way as above, parts of it are left blank to try out:

{{< katex >}}
\begin{array}{lrcl}
\text{Let } & x & = & b^u \\ \\
\text{And let } &  y & = & b^v \\ \\
\end{array}
{{< /katex >}}

Then we proceed as follows:

{{< katex >}}
\begin{array}{lclr}
\text{LHS } & = & \log_b (\frac{x}{y}) & \\ \\
& = & & \text{by substitution above}\\ \\
& = & & \text{by Laws of Indices}\\ \\
& = & & \text{by Basics of Logarithms}\\ \\
& = & & \text{by definition of Logarithm}\\ \\
& = & \text{RHS} \\
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

## The Third Law

{{< theorem-block "3rd Law" "Proof" >}}
$$ \log_b (x^y) = y\cdot \log_b (x) $$
<--->

The proof is fairly simple and is very similar to the ones above, parts of it are left blank to try out:

{{< katex >}}
\begin{array}{lrcl}
\text{Let } & x & = & b^u \\ \\
\text{i.e., by definition } & \log_b (x) & = & u \\ \\
\end{array}
{{< /katex >}}

Then we proceed as follows:

{{< katex >}}
\begin{array}{lclr}
\text{LHS } & = & \log_b (x^y) & \\ \\
& = & \log_b ((b^u)^y) & \text{by substitution above}\\ \\
& = & \log_b (b^{u\cdot y}) & \text{by Laws of Indices}\\ \\
& = & u\cdot y & \text{by Basics of Logarithms}\\ \\
& = & y\cdot u & \\ \\
& = & y \cdot \log_b (x) & \text{by definition of Logarithm}\\ \\
& = & \text{RHS} \\
\end{array}
{{< /katex >}}

{{< /theorem-block >}}

The above laws made logarithms extremely valuable in the recent centuries before calculators were invented aiding engineers and everyone else of course in easily doing otherwise complex arithmetic computations. We take a look at how this was done in the next session.
