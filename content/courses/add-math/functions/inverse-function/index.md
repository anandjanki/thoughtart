---
title: "Inverse Function"
date: 2020-03-20T00:12:05+05:30
draft: false
weight: 6
---

In very simple terms, the inverse of a function is one that reverses what the function does. For e.g., if the function maps 2.3 to say 41, then the inverse should map 41 to 2.3.

{{< columns "40,20,40" >}}
{{< figure src="images/f.png" class="figs" title="An example function f" >}}
<--->
<--->
{{< figure src="images/f_inv.png" class="figs" title="And its inverse function" >}}
{{< /columns >}}

For a function to have an inverse it should be bijective, which means it should be both injective and surjective:

- If the function is not surjective, i.e., if the function is not onto, then it means there are some elements of the co-domain that are not mapped. When we consider the inverse of this function, the co-domain becomes the domain, and it will mean that there are some elements in the domain which are not mapped. That is not allowed for the definition of a function.
- If a function is not injective, i.e., if the function is not 1-to-1, then it would mean that there are few elements of the domain map to the same element in the co-domain. When we consider the inverse of this function, the co-domain becomes the domain and it will mean that there are some elements in the domain that have a 1-to-many mapping. That is not allowed for the definition of a function.

Hence only bijective functions can have inverses.

## Inverse Definition

One way to define the inverse function is as follows:

{{< highlight-box "Defn 1:" "none" "" "part" >}}
Let \\(f\\) be a function whose domain is the set X, and whose range is the set Y. Then \\(f\\) is invertible if there exists a function \\(g\\) with domain Y and image X, with the property:

$$ \displaystyle f(x)=y\,\,\Leftrightarrow \,\,g(y)=x $$
{{< /highlight-box >}}

### Finding inverse - algebraically

Suppose we are given a function of real numbers as follows:
$$ f(x) = 2\cdot x + 3 $$

How do we find the inverse of this function? To see that, let's take a few values of \\(x\\) and see what happens:

For e.g., when \\(x = 1 \\), the value of the function is \\( 5\\), i.e.:
$$ 5 = 2\cdot 1 + 3 $$
When \\(x = 2.5 \\), the value of the function is \\( 8\\), i.e.:
$$ 8 = 2\cdot 2.5 + 3 $$

What we are seeking is a function \\( g(x)\\) which will do the reverse, i.e., give the output 1, when the input i 8, or give the output 2.5 when the input given is 8. In other words, we are seeking a function that will do the following:
{{< katex >}}
\begin{array}{rcl}
x & = & 2\cdot g(x) + 3 \\ \\
\therefore g(x) & = & \displaystyle \frac{x-3}{2} \\
\end{array}
{{< /katex >}}

### Finding inverse - graphically

We can also plot the graph of the above function and see how we can find the inverse graphically.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/inverse_graph.png" class="figs" title="The graph of a function and its inverse" >}}
<--->
{{< /columns >}}

We notice that the point \\( (1, 5) \\) lies on \\(f(x)\\) and the point \\( (5, 1) \\) lies on the inverse function \\( f^{-1}(x) \\). And likewise for every point on the original function and its inverse. 

In other words, almost magically, the graph of the inverse function is a reflection of the graph of the original function on the \\( y = x\\) line.

### Inverse of square function

The function above \\( y = 2\cdot x + 3 \\) was a simple bijective function. What if we have a function which is not bijective, consider the following function:

$$ f : \R \to \R \text{ such that } f(x) = x^2 $$

Note that the co-domain of the function is \\( \R \\), but the range of the function would only be positive real numbers \\( \R^{+} \\). This function is not injective, it is a many-to-1 function. The function is also not surjective, the range \\( \R^{+} \\) is not all of the co-domain \\( \R \\).

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/x_squared.png" class="figs" title="The graph of the square function" >}}
<--->
{{< /columns >}}

Clearly given this definition, the function does not have an inverse.

One way around is to construct a new function, with a slightly different domain and co-domain, but with the same definition as the original squared function, such that the new function can have an inverse. This can be done as follows:

$$ g : \R^{+} \to \R^{+} \text{ such that } g(x) = x^2 $$

Note that both the domain and the co-domain have been restricted to \\( \R^{+} \\) making the function a 1-to-1 and onto function, in other words a bijective function.

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/x_squared_modified.png" class="figs" title="The graph of the square function with a modified domain and co-domain" >}}
<--->
{{< /columns >}}

And now, we can find the inverse of this function as shown below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/x_squared_modified_inverse.png" class="figs" title="The graph of the modified square function along with its inverse" >}}
<--->
{{< /columns >}}

Thus, 

$$ g^{-1}(x) = \sqrt{x} $$

## Another definition

A more succinct way  to define the inverse based on the idea of composite functions we learnt earlier is as follows:

{{< highlight-box "Defn 2:" "none" "" "part" >}}
A function \\(g\\) is called the inverse of a function \\(f \\) if and only if:

$$ (g\circ f)(x) = (f\circ g)(x) = x $$
{{< /highlight-box >}}

