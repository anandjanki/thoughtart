---
title: "Comparing Growth Rates"
date: 2020-08-02T09:24:30+05:30
draft: false
weight: 2
---

To understand the different kinds of growth rates, lets put them next to each other and compare. 

## Graphs of functions

### Linear Functions

You have learnt about linear functions in earlier Math classes and they take the following form:
$$ f(x) = a\cdot x + b $$
Or the more popular form of \\( y = mx + c \\). For the sake of the comparison, lets make the constant term 0, and plot linear functions for different values of the slope \\( m\\).

This is depicted in the picture below:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/linear-functions-v2.png" class="figs" title="Graph of y = kx for different positive values of k" >}}
<--->
{{< /columns >}}

Notice how the function "grows" with increasing value of \\(x\\). For e.g., if we look at the graph of \\( y = 2\cdot x\\):

 * at \\( x = 1 \\), the function has a value of \\( y = 2 \\), 
 * at \\( x = 2 \\), the function has a value of \\( y = 4 \\), 
 * at \\( x = 3 \\), the function has a value of \\( y = 6 \\), and
 * at \\( x = 10 \\), the function has a value of \\( y = 20 \\).

This is called linear growth. The growth between \\( x = 1 \\) and \\( x = 2 \\) is the same as the growth between \\( x = 2\\) and \\( x = 3\\).

### Power Functions

Next, we learnt about Polynomial functions in an [earlier session]({{< ref "basics#definition" >}}). Linear functions can also be considered as polynomial functions, specifically polynomial functions of degree 1, but the graphs of polynomial functions of degree 2 and more look very similar and somewhat different from the linear functions. So, we look at them separately in this section.

Again for simplicity of drawing a graph, we will drop the many terms of a typical polynomial, and look at polynomial functions of the following form:
$$ f(x) = x^k $$
for different positive values of \\( k \\). These polynomial functions are more commonly called Power functions.

This is depicted in the picture below:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/power-functions-v2.png" class="figs" title="Graph of y = x^k for different positive values of k" >}}
<--->
{{< /columns >}}

Notice how the function "grows" with increasing value of \\(x\\). For e.g., if we look at the graph of \\( y = x^2 \\):

 * at \\( x = 1 \\), the function has a value of \\( y = 1 \\), 
 * at \\( x = 2 \\), the function has a value of \\( y = 4 \\), 
 * at \\( x = 3 \\), the function has a value of \\( y = 9 \\), and
 * at \\( x = 10 \\), the function has a value of \\( y = 100 \\).

The growth between \\( x = 1 \\) and \\( x = 2 \\) is less than the growth between \\( x = 2\\) and \\( x = 3\\).

### Exponential Functions

Finally, we looked at exponentials in great detail and the Laws of Indices in an [earlier session]({{< ref "laws-of-indices" >}}). We looked at how positive integer exponents yield [very large numbers]({{< ref "exponents-at-work#very-large-numbers" >}}), how many fractional exponents and other combinations yield [irrational numbers]({{< ref "exponents-at-work#irrational-numbers" >}}) and surds. But we largely dealt with numbers involving a base and an exponent.

Now, we are in a position to define an exponent function in the following manner:
$$ f(x) = k^x $$
where \\( k\\) is a positive number and \\( x\\) takes real values.

These are called exponential functions, and are depicted below for a few different values of \\( k \\):
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/exponential-functions.png" class="figs" title="Graph of y = x^k for different positive values of k" >}}
<--->
{{< /columns >}}

At first glance these functions may look similar to the power functions, but we will see very shortly that they are actually very different. A glimpse of it may be visible if you compare the graph of \\( x^2 \\) and the graph of \\( 2^x \\), the \\( x^2 \\) function has a value of \\( 100\\) only at \\( x = 10 \\), whereas the \\( 2^x \\) function has already crossed the value of \\( 100 \\) at \\( x = 7\\) where its value is \\( y = 2^7 = 128 \\).

Notice how the function "grows" with increasing value of \\(x\\). For e.g., if we look at the graph of \\( y = 2^x \\), it starts a little slow:

 * at \\( x = 1 \\), the function has a value of \\( y = 2 \\), 
 * at \\( x = 2 \\), the function has a value of \\( y = 4 \\), 
 * at \\( x = 3 \\), the function has a value of \\( y = 8 \\), and
 * at \\( x = 10 \\), the function has a value of \\( y = 1024 \\).

But by the time \\( x = 10 \\), it looks like the growth of the function is galloping away.

### Comparing the graphs

To compare these functions and how they grow with \\( x \\), we can draw all of them together in a single graph. Lets pick one value of \\(k\\), say \\( k = 2 \\), and look at the graph of all three functions together \\( y = 2\cdot x\\), \\( y = x^2 \\), and \\( y = 2^x\\). This is depicted below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/linear-power-exponential-v2.png" class="figs" title="Graph of linear, power and exponential functions together" >}}
<--->
{{< /columns >}}

As mentioned before, notice how at \\( x = 10 \\), the linear function \\( y = 2\cdot x\\) has a value of \\( y = 20 \\), and the power function \\( y = x^2 \\) has a value of \\( y = 100 \\), but the value of the exponential function is already outside the range shown in this graph. 

We have to zoom out quite a bit to see where the exponential function \\( 2^x \\) has reached at \\( x = 10 \\) and then we can see the comparison of the rates of these three kinds of functions very clearly as depicted below:

{{< figure src="images/linear-power-exponential-v3.png" class="figs" title="Graph of linear, power and exponential functions together" >}}

We can also note that at \\( x=25 \\) at the far end of the x-interval shown here, the linear function has a value of \\( y = 2\cdot 25 = 50 \\), the power function has a value of \\( y = 25^2 = 625 \\), whereas the exponential function is nowhere to be seen, for it has a value of \\( y = 2^{25} \\) which is approximately equal to 32million!!

## Turtle Island

This idea is also explained in the following video:

{{< youtube "9Bu0Hkxw88g" >}}
