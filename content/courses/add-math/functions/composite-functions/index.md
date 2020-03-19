---
title: "Composite Functions"
date: 2020-03-14T23:21:46+05:30
draft: false
weight: 5
---

It is worth taking a little pause here to note that we started with a very basic definition of sets, just as a collection of objects and from there on started building more and more ideas purely with our imagination. Composite function is yet another such idea. First, we put one set in front of another and made the definitions of mappings and functions. Now, we put one function in front of another and ask the question what would happen.

## A practical example

It is also good to note that most of what we have been building on have practical applications too. Not that they need to, they are each beautiful in their own right. But let's look at a practical example of composite functions.

Suppose, it's start of the academic year and we need to make three teams for the sports events of the year. We obviously want to make the distribution fair, so there is healthy competition between the teams. We decide to make the groups such that no group has a height advantage over the others.

In order to do this, we of course have to first find the heights of all the students in all the classes and then we apply what is called the *modulus* function (that's just a short mathematical way to say *remainder upon division by*). We divide the height of the student by 3, and depending on the remainder sort the student in one of the three teams.

This can be depicted as follows:

{{< columns "45,10,45" >}}
{{< figure src="images/student height function.png" class="figs" title="The function, f, mapping a student to his/her height" >}}
<--->
<--->
{{< figure src="images/modulus 3 function.png" class="figs" title="The function, g, mapping of a student's height to the house team (using division by 3)" >}}
{{< /columns >}}

We have two functions:
{{< katex >}}
\begin{array}{rclcl}
f & : & S & \to & H \\ 
g & : & H & \to & T \\ 
\end{array}
{{< /katex >}}

And to find which team a student belongs to, we use the first function to get the height of the student, then use the second function *on the height* of the student to get the team of the student. In other words, we have managed to chain one function after another to create a composite effect as shown below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/composite function.png" class="figs" title="The composition of function g over function f" >}}
<--->
{{< /columns >}}

We thus have a new function from the original set S of students to the final set T of teams. This overall function is called \\( g\circ f \\) and is defined below:

## Composite functions
{{< highlight-box "Defn 1:" "none" "" "part" >}}
Given two functions \\(\displaystyle f\colon X\to Y\\) and \\(\displaystyle g\colon Y\to Z\\) such that the domain of \\(g\\) is the codomain of \\(f\\), their **composition** is the function \\(\displaystyle g\circ f\colon X\rightarrow Z\\) defined by

$$\displaystyle (g\circ f)(x)=g(f(x)) $$
{{< /highlight-box >}}

Notice that to find the composition of two functions, the co-domain of the first function should be the same as the domain of the second function as in the case of the example above. In general, composition is not a commutative operation, in fact it is possible that while \\( g\circ f\\) is valid, it may not be possible to even define \\(f\circ g\\) as in the example above.

### Another function depiction

Another way to think of functions is an operation that takes \\(x\\) as input and produces \\( f(x) \\) as the output as shown in the picture below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/Function_machine2.svg" class="figs" title="Function as taking an input and producing an output" >}}
<--->
{{< /columns >}}

A *function* in a computer programming language for example can be thought of in the above manner - no wonder they were called functions in the first place. Of course, all our functions that we talked about until now can also be thought of in the same manner as well.

### Visual depiction

With this depiction, the idea of composite functions looks even more appealing, take the functions below for example:
{{< katex >}}
\begin{array}{rclcl}
f & : & x & \mapsto & x^2 \\ 
g & : & x & \mapsto & x + 1 \\ 
\end{array}
{{< /katex >}}

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/Function_machine5.svg" class="figs" title="Composite function of g and f above for the input value of 3" >}}
<--->
{{< /columns >}}

### Algebraic manipulation

We can also start dealing with these operations algebraically. It tends to become a little mechanical once you get used to it, but it has its own advantages of speedily getting to newer findings. For the two functions above, we can find both \\( g\circ f\\) and \\(f\circ g\\) as shown below:

{{< katex >}}
\begin{array}{rcl}
f(x) & = & x^2 \\ 
g(x) & = & x + 1 \\ \\
(g\circ f)(x) & = & g(f(x)) \\
& = & g(x^2) \\ 
& = & x^2 + 1 \\ \\
(f\circ g)(x) & = & f(g(x)) \\
& = & f(x+1) \\ 
& = & (x + 1)^2 \\ 
\end{array}
{{< /katex >}}

While it may be easy to get lost in the ease of doing these algebraic manipulations, it is worth always keeping track of the each of the functions we are dealing with, their domain, co-domain, and the range, and these sets once we do a composition, all from first principles. Let's do this for the above example:

{{< table "horizontal-table" >}}
|  | \\(f(x) = x^2 \\)  | \\( g(x) = x + 1\\) | \\((g \circ f)(x) = x^2 + 1\\)  | \\( (f \circ g)(x) = (x + 1)^2 \\) |
| :-- | :-- | :-- | :-- | :-- |
| Domain |   \\( \R \\) | \\( \R \\)  | \\( \R \\) | \\( \R \\)  |
| Co-domain | \\( \R \\)   | \\( \R \\)   | \\( \R \\) | \\( \R \\)  |
| Range |  \\( \R^+ \\)  | \\( \R \\)   | \\( y \geq 1 \\) | \\( \R^+ \\)  |
{{< /table >}}

Notice how the range varies depending on the values of the function. The values that the function \\( f(x) = x^2 \\) takes is only positive real values, hence the range of the function is \\( \R^+ \\). The same holds true for the function \\( f\circ g\\), and the range is \\( \R^+ \\). On the other hand, the function \\( g\circ f = x^2 + 1\\) takes values greater than 1, hence its range is simply \\( y \geq 1 \\) or to be more precise in set terms $$ \text{Range of function } (g \circ f) = \lbrace y \| y \in \R \text{ and } y \geq 1 \rbrace $$ the set of all items y, where y is a real number and y is not less than 1.

We will look at a few different plots of functions shortly, and that should also help visualize the range of functions easily.
