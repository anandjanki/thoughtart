---
title: "Logarithm Uses"
date: 2021-08-28T12:16:58+05:30
draft: false
weight: 6
---

The three laws of logarithms that we unravelled in the last session have been tremendously useful in aiding arithmetic calculations in the centuries gone by, when calculators were not yet invented. Electronic calculators are only a few decades old, but the industrial revolution started in the 17th century and for 3-4 centuries since the 16th century logarithms have been at the heart of easing arithmetic calculations in so many fields such as engineering, astronomy, the sciences, accounting, etc.

To understand how this works, lets take an example. Suppose we have to do a tedious arithmetic calculation such as the one below, to find the value of \\(x\\).
{{< katex >}}
\begin{array}{rcl}
x & = & \displaystyle \frac{47.38 \times \sqrt{6721.25}}{929.39} \\
\end{array}
{{< /katex >}}

In today's world, this calculation would hardly take a few seconds, not more than half a minute in any case to find the value of \\(x\\) using an electronic calculator that is now ubiquitous with engineers, shopkeepers, accountants, even students in high school. But take yourself 400 yrs or so ago, how would they have done such calculations? If one has to build a bridge across a river, surely calculations of such kinds would routinely come up. That is where the laws of logarithms come in along with a very important invention called the log tables.

## Log Tables

In the early 1600s, a few people took the pains to put together what are called the log and anti-log tables. John Napier is rather well known for having put these togehter, along with a few others before and after him also independetnly worked on it. When we were in our high school in the 1990s, and for quite some time after the electronic calculator was invented in the 1970s, all calculations *had to* be one using the log tables. While students used to cringe at the sight of these tables, mainly sinc calculators had already set in, it is worth taking a few moments to understand how these tables served anyone around the world doing arithmetic calculations for several centuries.

The log table eventually took the form as shown below:

{{< columns "1,98,1" >}}
<--->
{{< figure src="images/log-table.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The table is fairly easy to read, as highlighted in the picture below, to find say \\( \log_{10} (6.316) \\), simply navigate the appropriate row, appropriate column and then add the digits from the last few columns. 
{{< columns "1,98,1" >}}
<--->
{{< figure src="images/log-table-6316.png" class="figs" title="" >}}
<--->
{{< /columns >}}

You also check using a calculator that 
{{< katex >}}
\log_{10} (6.316) = 0.8004
{{< /katex >}}

### Simplifying calculations

Now lets use the log table to do the calculation we set out with:

{{< katex >}}
\begin{array}{rclcr}
x & = & \displaystyle \frac{47.38 \times \sqrt{6721.25}}{929.39} \\ \\
\therefore \log_{10} (x) & = & \log_{10} (\displaystyle \frac{47.38 \times \sqrt{6721.25}}{929.39}) & & \text{Taking log on both sides} \\ \\
& = & \log_{10} (47.38 ) + \log_{10} (\sqrt{6721.25}) - \log_{10} (929.39) & & \text{By using the Laws of Logarithm} \\ \\
& = & \log_{10} (4.738 \times 10) + \log_{10} (6721.25)^{\frac{1}{2}} - \log_{10} (9.2939 \times 100) \\ \\
& = & \log_{10} (4.738) + \log_{10} (10) + \\ 
& & {\frac{1}{2}}\log_{10} (6.72125 \times 1000) - \\
& & \log_{10} (9.2939) - \log_{10} (100) \\ \\
& = & \log_{10} (4.738) + \log_{10} (10) + \\ 
& & {\frac{1}{2}}(\log_{10} (6.72125) + \log_{10} (1000)) - \\
& & \log_{10} (9.2939) - \log_{10} (100) \\ \\
& = & \log_{10} (4.738) + 1 + {\frac{1}{2}}(\log_{10} (6.72125) + 3) - \log_{10} (9.2939) - 2 \\ \\
& = & \log_{10} (4.738) + {\frac{1}{2}}(\log_{10} (6.72125)) - \log_{10} (9.2939) + 0.5 \\ \\
& = & 0.6756 + 0.5 \times 0.8275 - 0.9682 + 0.5 & & \text{by looking up the Log tables} \\ \\
& = & 0.62115 & & \text{doing the simpler Arithmetic manually} \\ \\
\end{array}
{{< /katex >}}

Notice that the key simplification step is that under the logarithm, multiplications get replaced by additions, and divisions get replaced by subtractions, significantly simplifying the burden of doing the arithmetic manually. It may also be noted that powers get replaced with multiplication, which can in turn be replaced with addition, but in the above example, since the power was only \\( \sqrt{} \\), under the logarithm it mean multiplying by \\( \frac{1}{2} \\), which can be easily done even mentally.

### Anti-log tables

The last bit of the puzzle was of course the anti-log tables, which were essentially tables that provided values of \\(10^x\\), which were also put together in a similar manner to the log tables. Of course, how these tables were put together is a story in itself, but that was a one time task. Just imagine the billions of calculations around the world that it subsequently eased!

The anti-log table is shown below:
{{< columns "1,98,1" >}}
<--->
{{< figure src="images/antilog-table.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Now it was a simple matter to look up the antilog table for \\( 0.6212 \\) to find the answer to the original calculation as \\( 0.418 \\).

A calculator can of course be used to confirm that all three digits of that answer are absoutely right! That right there was one of the significant inventions that powered engineering, scientific, astronomical calculation through the centuries of the Industrial Revolution resulting in the world as we know it today.

