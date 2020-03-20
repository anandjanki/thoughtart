---
title: "Exploring Graphs"
date: 2020-03-20T20:04:09+05:30
draft: false
weight: 7
---

In this session, we will explore graphs of functions in more detail. It usually helps to visualize the graph of a function, how it looks in the Cartesian co-ordinate system along with the algebraic definition of the function.

## Linear Function

Lets's first start with a very simple linear function, given as follows:
$$ f : \R \to \R \text{ such that } f(x) = 2x $$

The graph of this function is shown below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = 2x.png" class="figs" title="The graph of a linear function passing through the origin" >}}
<--->
{{< /columns >}}

The part of the function in the interval of the domain \\( [-1, 2] \\) is depicted as a solid line and the rest of the graph is shown with dotted lines just for ease of visualization and to avoid congestion.

### Translation along y-axis

A translation of the graph of this function along the y-axis would yield the following functions, depicted further below:
{{< katex >}}
\begin{array}{rcl}
f_{0,+5}(x) - 5 & = & 2\cdot x \\
f_{0,-5}(x) + 5 & = & 2\cdot x \\
\end{array}
{{< /katex >}}

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y_translate = 2x.png" class="figs" title="The graph of a linear function translated along the y-axis" >}}
<--->
{{< /columns >}}

### Translation along x-axis

A translation of the graph of this function along the x-axis would yield the following functions, depicted further below:
{{< katex >}}
\begin{array}{rcl}
f_{+5,0}(x) & = & 2\cdot (x - 5) \\
f_{-5,0}(x) & = & 2\cdot (x + 5) \\
\end{array}
{{< /katex >}}

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = 2 * x_translate.png" class="figs" title="The graph of a linear function translated along the x-axis" >}}
<--->
{{< /columns >}}

### Translation along both axes

A translation of the graph of this function along the both axes would yield the following functions, depicted further below:
{{< katex >}}
\begin{array}{rcl}
f_{+5,+5}(x) - 5 & = & 2\cdot (x - 5) \\
f_{-5,+5}(x) - 5 & = & 2\cdot (x + 5) \\
f_{+5,-5}(x) + 5 & = & 2\cdot (x - 5) \\
f_{-5,-5}(x) + 5 & = & 2\cdot (x + 5) \\
\end{array}
{{< /katex >}}

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y_translate = 2 * x_translate.png" class="figs" title="The graph of a linear function translated along both axes" >}}
<--->
{{< /columns >}}

### All Translations

All of the above translations of the graph of \\( y = 2x \\) are depicted together below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/all translations of y = 2x.png" class="figs" title="The graph of a linear function and some of its translations" >}}
<--->
{{< /columns >}}

### Scaling the function

We can also scale the linear function and visualize the graph of the scaled functions further below:
$$ f_{0,0,k}(x) = k\cdot 2x $$

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = kx.png" class="figs" title="The graph of a linear function and some of its scaled versions" >}}
<--->
{{< /columns >}}

### Scaling and translation

Finally, we can of course look at scaling and translation together to yield a series of functions:
$$ f_{a,b,k}(x) - b = k\cdot 2\cdot (x - a) $$

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/scale_and_translate.png" class="figs" title="The graph of a linear function with both scaling and translation" >}}
<--->
{{< /columns >}}

## Quadratic function

Every time we encounter a new function, we can visualize the graph of the function and also its translations and scaling. That helps build a pictorial memory of what the function looks like.

For e.g., let's explore a quadratic function in the same way as the linear function above.

$$ f : \R \to \R^{+} \text{ such that } f(x) = x^2 $$

The graph of this function is shown below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = x_squared.png" class="figs" title="The graph of a quadratic function passing through the origin" >}}
<--->
{{< /columns >}}

The part of the function in the interval of the domain \\( [-1, 2] \\) is depicted as a solid curve and the rest of the graph is shown with dotted lines just for ease of visualization and to avoid congestion.

### Translating the quadratic

A translation of the graph of \\( y = x^2 \\), with an x-translation of 5 and y-ranslation also of 5 is depicted below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = x_squared v2.png" class="figs" title="The graph of a quadratic function with one of its translations" >}}
<--->
{{< /columns >}}

### Translation and Scaling

A translation of the graph of \\( y = x^2 \\), with an x-translation of 5 and y-ranslation also of 5, along with a scaling at \\( k = 4 \\) and \\( k = 0.4 \\) are depicted below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = x_squared v4.png" class="figs" title="The graph of a quadratic function with translation and scaling" >}}
<--->
{{< /columns >}}

Notice how drawing the graph also helps easily visualize the range of these functions. For e.g., 
{{< columns "20,60,20" >}}
<--->
{{< table "horizontal-table" >}}
|  | Range |
| :-- | :-- |
| \\( y = x^2 \\) |   \\( \R^{+} \\) |
| \\( y - 5 = (x - 5)^2 \\) |   \\( y \geq 5 \\) |
| \\( y - 5 = 0.4\cdot (x - 5)^2 \\) |   \\( y \geq 5 \\) |
| \\( y - 5 = 4\cdot (x - 5)^2 \\) |   \\( y \geq 5 \\) |
{{< /table >}}
<--->
{{< /columns >}}

### Roots of the quadratic

Consider a translation of the quadratic shown below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = x_squared roots.png" class="figs" title="The graph of a quadratic function showing its roots" >}}
<--->
{{< /columns >}}

This graph cuts the x-axis at two points, \\( x = -2 \\) and \\( x = 2\\). These are called the roots of the function. More formally,
{{< highlight-box "Defn 1:" "none" "" "part" >}}
\\(x_0\\) is called a **root** of a function if and only if

$$ f(x_0) = 0 $$
{{< /highlight-box >}}

Note that we would have also learnt solving the quadratic equation above algebraically to find its roots:
{{< katex >}}
\begin{array}{rcl}
x^2 - 4 & = & 0 \\
\therefore (x - 2)\cdot(x + 2) & = & 0 \\
\therefore x = 2 & OR & x = -2
\end{array}
{{< /katex >}}

Note also in the same vein that a quadratic equation (with real coefficients) can have either 0 (real) roots, 1 (real) root, or 2 (real) roots.
{{< columns "20,60,20" >}}
<--->
{{< table "horizontal-table" >}}
|  | Roots |
| :-- | :-- |
| \\( y = x^2 - 4 \\) |  Has 2 roots, \\( x = -2\\) and \\( x = 2\\)|
| \\( y = x^2 \\) |  Has exactly 1 root, \\( x = 0\\) |
| \\( y = x^2 + 4 \\) |  Has no real roots |
{{< /table >}}
<--->
{{< /columns >}}

This is depicted graphically below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = x_squared roots v3.png" class="figs" title="The graph of different quadratic function showing their real roots" >}}
<--->
{{< /columns >}}

Finally, the roots of the corresponding inverted quadratic functions are depicted below:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/y = x_squared roots v4.png" class="figs" title="The graph of different quadratic function showing their real roots" >}}
<--->
{{< /columns >}}

