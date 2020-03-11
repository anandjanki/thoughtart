---
title: "Functions"
date: 2020-01-21T06:57:15+05:30
draft: false
weight: 3
---

We have now covered all the background needed to delve into one of the most fundamental topics of Mathematics - we are now ready to understand what functions are. Almost every other session we do in the course of Additional Mathematics will build on this topic, so it is essential that you go through all the background we covered so far (that on [Sets]({{< ref "Sets" >}}) and [Mappings]({{< ref "mappings" >}}) and carefully understand the concept of functions described in great detail here.

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A **Function** is simply a mapping in which each element of the first set is mapped to one element of the second set.
{{< /highlight-box >}}

You may wonder if that's all the definition, and entire branches of Mathematics are built on such a simple definition. Indeed it is so as we will start seeing shortly.

## Valid mapping types

It should be immediately clear from the definition of functions that only certain kinds of mappings can qualify to be functions. 

A 1-to-many mapping cannot be a function. This should be clear because in a 1-to-many mapping, we can expect some elements of the first set to map to multiple elements of the second set. But by definition, in a function each element of the first set can map to only one element of the second set. For the same reason, many-to-many mappings cannot be functions either, because they can contain some connections which map an element of the first set to many elements of the second set.

On the other hand a 1-to-1 mapping can be a function. A many-to-1 mapping can also be a function. But a word of caution, not all 1-to-1 mappings can be functions. Recall that mappings allowed some elements of the first set to not be mapped at all. That is not allowed with function. Likewise for many-to-1 mappings, if there is any element of the first set in a many-to-1 mapping that is not mapped to an element of the second set, then it cannot be called a function.

> **A side note** - Just to say the above in a slightly more complicated way - the set of all functions between two sets is a subset of the union of all 1-to-1 mappings and many-to-1 mappings between the two sets each of which in turn is a subset of the set of all mappings between the two sets. 
>
> Well that is a mouthful, but it is nice to try and read it slowly. It is some of these concepts that make sets and functions the basics of all or most of Mathematics. The other idea that we visited earlier was that of sets being elements of other sets in turn.

## Examples of functions

Lets take a few examples to understand functions better.

### Remainder function

Consider a set X of all numbers from 1 to 100. Consider another set Y with all numbers from 0 to 9. Each number in set X is mapped to its remainder upon division by 10. Lets depict this pictorially as we have been doing so far.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/remainder function.png" class="figs" title="A mapping of a number to its remainder upon division by 10" >}}
<--->
{{< /columns >}}

Is this mapping a function?

The way to determine this is simple, just follow the definition of a function and check if the definition is fully met:

- There is a first set S, and a second set Y, and a rule connecting elements of set X to elements of set Y. So, its definitely a mapping.
- Further, each element of set X is mapped to some element of set Y. We can easily check that there is no element that is not mapped, since every element when divided by 10 will have a remainder between 0 and 9, and all of these numbers are in set Y.
- Finally, each element of set X is mapped to only one element in set Y, which should also be obvious, because when we divide a number by 10 we get a single unique remainder between 0 and 9, never can we get two or more remainders.

Thus this mapping satisfies all the conditions needed for it to be a function. Also note that this is a many-to-one function.

### Division function

Lets consider the same sets as above - set X of all numbers from 1 to 100 and set Y with all numbers from 0 to 9. Each number in set X is mapped to the result of dividing the number by 10. Is this mapping a function?

Lets depict this pictorially again as we have been doing so far.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/division function.png" class="figs" title="A mapping of a number to the result of dividing the number by 10" >}}
<--->
{{< /columns >}}

The way to determine this is simple, we again follow the definition of a function and check if the definition is fully met:

- There is a first set S, and a second set Y, and a rule connecting elements of set X to elements of set Y. So, its definitely a mapping.
- Next, we notice all the multiples of 10 in set X, such as 10, 20, ..., 90 are correspondingly mapped to 1, 2, ... 9.
- Note however that the result of dividing 100 by 10 is 10 which is not an element in set Y. So we are unable to map 100. While that may be OK for a mapping, it is NOT OK for a function. Recall that for a mapping to be a function, *each* element of set X should be mapped.
- Likewise, several other numbers that are not multiples cannot be mapped. For eg 2 / 10 is 0.2 which is not an element of set Y.

Hence this mapping is NOT a function.

### Divisors function

Lets consider one more examples with the same sets as above - set X of all numbers from 1 to 100 and set Y with all numbers from 0 to 9. Each number in set X is mapped to its divisors in set Y. Is this mapping a function?

Lets depict this pictorially again as we have been doing so far.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/divisors function.png" class="figs" title="A mapping of a number to the result of dividing the number by 10" >}}
<--->
{{< /columns >}}

The way to determine this is simple, we again follow the definition of a function and check if the definition is fully met:

- There is a first set S, and a second set Y, and a rule connecting elements of set X to elements of set Y. So, its definitely a mapping.
- Notice that for each number in set X, some or all of its divisors are present in set Y. 
 - For the number 2, its divisors are 1 and 2, and both these numbers are present in set Y, so the number 2 in set X can be mapped. 
 - For the number 100, some of its divisors such as 1, 2, and 5 are present in set Y, but some of its other divisors such as 10, 20, 25, and 50 are not present in set Y. Does this prevent this mapping from being called a function? NO! We are still able to map 100 to some of its divisors. To be precise, we are able to map 100. And we are able to map all other elements of set X likewise.
- However, the issue is that all of these numbers in set X map to more than one element in set Y. That goes against the definition of a function. A function requires that each element of set X is mapped to one element in set Y. 

Multiple elements in set X can map to the same element in set Y, like in the case of the remainder function above. But an element in set X *cannot* map to multiple elements in set Y.

Hence this mapping is NOT a function.

### Square function

Finally, lets consider a set X of all numbers from 1 to 10. Consider another set Y with all numbers from 1 to 100. Each number in set X is mapped to its square in set Y. Is this mapping a function?

Lets depict this pictorially again as we have been doing so far.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/square function.png" class="figs" title="A mapping of a number to its square" >}}
<--->
{{< /columns >}}

Is this mapping a function?

The way to determine this is simple, just follow the definition of a function and check if the definition is fully met:

- There is a first set S, and a second set Y, and a rule connecting elements of set X to elements of set Y. So, its definitely a mapping.
- Further, each element of set X is mapped to some element of set Y. We can easily check that there is no element that is not mapped, 1 maps to 1 (this is a short way to say - the element 1 in set X maps to the element 1 in the set Y), 2 maps to 4, and so on, 10 maps to 100. In other words all elements can be mapped.
- Finally, each element of set X is mapped to only one element in set Y, which should also be obvious, because when we square a number we get a unique number.
- There are many elements in set Y that are not mapped into, but that does not bother us. If there had been any element in the first set, set X, that cannot be *mapped from*, then that would have been reason to reject the mapping as a function. However that is not the case here.

Thus this mapping satisfies all the conditions needed for it to be a function. Also note that this is a 1-to-1 function.

## Types of function

### Domain, co-domain and range

A little bit of nomenclature is in order here. We will use the square function above, depicted again here to go over these:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/domain codomain range.png" class="figs" title="The square function with the range of the function within the co-domain" >}}
<--->
{{< /columns >}}

And now for the definitions:

- The set X is called the domain of the function.
- The set Y is called the co-domain of the function.
- The subset of the co-domain which contains only elements of set Y that have been mapped from set X via the function is called the range of the function. 

For the square function depicted above, the range is the set of all square numbers between 1 and 100. The rest of the numbers  in set Y are still part of the co-domain, but not in the *range of the function*. They are "outside the range". In words, the function can be thought of as a way to reach set Y from set X, imagine roads or bridges from elements in set X to some of the elements in set Y, but it may not be possible to reach all elements of set Y, wherever the function is able to reach is called the range of the function.

### Injective function

A function that is a 1-to-1 function is called an *injective function*. The square function depicted above is an injective function. 

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/domain codomain range.png" class="figs" title="The square function is an injective function" >}}
<--->
{{< /columns >}}

For an injective function, every element in the domain should map to a unique element in the co-domain. Note that it is OK if there are elements in the co-domain that are not mapped from any element in the domain, that is fine, it is still an injective function.

### Surjective function

A function where every element of the co-domain is mapped from some element of the domain is called a surjective function (it is also often called an *onto function*).

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/remainder function.png" class="figs" title="The remainder upon division by 10 is a surjective function" >}}
<--->
{{< /columns >}}

Note how every member of the co-domain is mapped from some element of the domain. There is no member of the co-domain that is not mapped. This called an onto function or a surjective function. For a surjective function the range and the co-domain are the same.

### Bijective function

A bijective function is simply a function that is both injective and surjective.

Lets first look at examples of functions that are NOT bijective:

{{< columns >}}
{{< figure src="images/injective.png" class="figs" title="An injective function (but not a surjective function)" >}}
<--->
{{< figure src="images/surjective.png" class="figs" title="A surjective function (but not an injective function)" >}}
<--->
{{< figure src="images/non-injective non-surjective.png" class="figs" title="A non-injective non-surjective function" >}}
{{< /columns >}}

In contrast, a bijective function is a function that is both injective and surjective, also called as a 1-to-1 onto function, shown below:

{{< columns "30,30,30" >}}
<--->
{{< figure src="images/bijective.png" class="figs" title="A bijective function (both injective and surjective)" >}}
<--->
{{< /columns >}}

The function depicted above is 1-to-1 (or injective) because each element in the domain maps to a unique element in the co-domain, and the function is onto (or surjective) because for every element in the co-domain there is at least one element from the domain that is mapped to it.

So far, so good. Now, lets take things one level further, but first a little detour.

## A little detour

### Infinite sets

In the sessions on Sets and Mappings, we dealt largely with sets of objects in daily life like teams and their members, zones in a field, teachers, students, colors in flags, etc. We will now start exploring with sets of numbers. We already started doing that in this session on functions, and we started using sets of numbers in the function examples above.

What if we consider a large set, say the set of all natural numbers, or the set of all integers? The key change is that these sets have "infinite" number of elements. But pretty much every concept we covered in the session on sets still holds true. (Every concept except the ones on cardinality, and set equality - we will not need to deal with cardinality of these sets to work with functions, so we will keep that aside, but everything else still works.) We can consider unions and intersections of these sets, we can consider mappings between these sets, and most interestingly we can consider functions between these sets as we will see shortly.

Before that, take a moment to reflect some of the concepts we covered on sets, and see if they all hold true even with these sets with infinite elements. Note that "infinite" is bit of a loose term, not an exactly mathematically correct term to use here, but it will be OK for our purposes.

Lets take an example to see what we mean. Consider any two numbers, say 45 and 60, and consider the set of divisors of both of these numbers as well as multiples of both of these numbers.

If we were to write out these sets in the set-builder notation, it would look as follows:
$$ D_{45} = \lbrace d : d \in \N \text { and } d \,|\, 45 \rbrace $$

Some of this notation may be unfamiliar, but in words, we are just saying that the set \\( D_{45} \\) is the set of all \\( d \\) such that (represented by the colon character \\(:\\)) \\( d \\) belongs to the set of natural numbers (represented by the notation \\( \N \\)) and \\( d \\) divides 45 (represented by the notation \\( d \,|\, 45 \\)).

Likewise, the set of all multiples of 45 would be written as follows:
$$ M_{45} = \lbrace 45\cdot k : k \in \N \rbrace $$

You can ignore this crytic notation if it is hard to follow. Lets depict the sets pictorially as we have always done. But before that, lets write out some of the elements of these sets:

{{< katex >}}
\begin{array}{rcl}
D_{45} & = & \lbrace 1, 3, 5, 9, 15, 45 \rbrace \\
D_{60} & = & \lbrace 1, 2, 3, 4, 5, 6, 10, 12, 15, 20, 30, 60 \rbrace \\
M_{45} & = & \lbrace 45, 90, 135, 180, \ldots \rbrace \\
M_{60} & = & \lbrace 60, 120, 180, 240, 300, \ldots \rbrace \\
\end{array}
{{< /katex >}}

The key thing to note is that the set of divisors are finite sets, that is they have a finite number of elements. However the set of multiple is "inifite", i.e. it is impossible to write out all the elements of this set, it goes on endlessly (and that is represented by the notation \\( \ldots \\)).

That however does not limit us to draw up a picture of these sets together along with their intersecting elements as shown below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/divisors and multiples.png" class="figs" title="The sets of the divisors and multiples of 45 and 60" >}}
<--->
{{< /columns >}}

That's a busy picture, looks like a lot going on, but it should not be too hard to see the following:

- The sets \\( D_4{}_5 \\) and \\( D_6{}_0 \\) have a finite number of elements as already noted.
- The intersection of these two sets also has a finite number of elements. In fact, this intersection, if you think carefully is really the set of common divisors of both 45 and 60. Further the largest number in the intersection set is 45, which is the Greatest Common Divisor (GCD) of the two numbers.
- In contrast the sets \\( M_4{}_5\\) and \\( M_6{}_0 \\) have an infinite number of elements in them.
- The intersection of these two sets also has an infinite number of elements. In fact, this intersection, if you think carefully is really the set of common multiples of both 45 and 60. Since this is an infinite set, without any upper limit, it is not possible to find the largest number of this set. But we can see that the smallest number in the intersection set is 180, which is the Least Common Multiple (LCM) of the two numbers.
- It is also possible to find the intersection of a finite set with an infinite set. For e.g., the intersection of the sets \\( D_4{}_5 \\) and \\( M_4{}_5\\), i.e. of the set of divisors and multiples of 45, is a set that contains only the original number 45.

All of that was a little bit of digression, but it shows a glimpse of the fascinating world of sets and how it becomes even more interesting as we look at sets containing numbers, and especially ones that contain infinite number of elements.

We come back to our topic of functions, and move on noting that as we explore mappings of such infinite sets, more particularly sets of real numbers, the field literally explodes. We come across functions such as polynomials, trigonometric functions, explonential and logarithmic functions, all of which are abundant in natural phenomena around us. From there, we go into the beautiful world of calculus that has completely revolutinalized the way we look at nature and analyze its underpinings.

Without much ado, lets march ahead.

### Number sets

We take one more little detour before we go ahead. Most functions we encounter will be functions of real numbers. So, its good to know what real numbers are before going forward.

This picture depicts the relation between the different sets of numbers, each inner set as we know from the session on sets is a subset of the outer sets.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/number sets.png" class="figs" title="Different kinds of numbers depicted as sets" >}}
<--->
{{< /columns >}}

The notation for natural numbers, \\( \N \\), may be familiar from above when we used it to define the set of divisors and multiples. 

This picture is borrowed from the thinkzone website by Keith Envoldsen. Do take a few minutes to also carefully read the description of each of these sets from the link [here](https://thinkzone.wlonk.com/Numbers/NumberSets.htm).

We can proceed further to explore functions of real numbers without worrying too much about all the kinds of numbers described above, though it is good to read up what these are.

## Function of real numbers

Consider set X as the set of all real numbers \\( \R \\), and set Y also as \\( \R \\). Lets define a function that for each number in set X, maps it to twice the number in set Y.

Lets first check and confirm that this mapping is a function. Each element in set X is mapped, because given any real nuumber we can multiple it by 2 and the result will be another real number. Each element in set X obviously maps to one element in set Y. Hence, this is a function. In fact, it is a 1-to-1 function.

### Depicting the function - take 1

We can try and represent this function pictorially as we have done in the past. It would look somewhat like below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/twice function.png" class="figs" title="Function that maps each number in X to twice its value in Y" >}}
<--->
{{< /columns >}}

While this is perfectly OK, and in fact it shows that the function is a 1-to-1 function, it is still limited in its representation power. One key limitation is that since the sets X and Y are infinite, it is hard to draw all the mapping arrows. When we were dealing with a finite set of objects such as colors or zones in a field, it was easy to depict the mapping for all the members. But as we already started noticing earlier on in this session, as the number of elements in the sets become large, it becomes difficult to depict all the connections between the sets and we resort to \\( \ldots \\) and \\( \vdots \\) to fill the gaps. The reader of the picture is then left to imagine what these gaps might be. 

Second, and more importantly, even though sets dont have any order in them the sets of numbers that we are dealing with have an inherent order. The definition of a set does not need to have ordering between its elements, but we have an additional nice property with sets of numbers that we can potentially use to depict functions between them.

### The number line

One idea that we are familiar with from early on in our Math classes is that the natural numbers, integers, and even rational and irrational numbers can all be represented as points on an infinite number line. This is shown in the picture below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/number line.png" class="figs" title="Real numbers can be thought of as points on an infinitely long number line" >}}
<--->
{{< /columns >}}

The number line above depicts some natural numbers such as 1, 2, 3, etc, it also depicts integers including -1, -2, -3, etc, and rational numbers such as -1.6, 0.5, etc and it also depicts irrational numbers such as \\( \sqrt{2} \\), \\(\pi\\), etc.

### Depicting the function - take 2

Armed with this depiction of the set of real numbers on a number line, we can now come up with an alternate representation of functions.

We will replace the ovals that we have been using so far to depict sets, and when the set is a set of numbers, such as real numbers we will use the number line to depict the two sets. The function can then be depicted as before with arrows from the first set X to the second set Y. This is shown pictorially below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/twice function number line take2.png" class="figs" title="Representing functions between real numbers using the number line" >}}
<--->
{{< /columns >}}

### Cartesian coordinates

The genius of the philosopher and mathematician René Descartes gave us the Cartesian coordinate system in the 17th century. Cartesian co-ordinate system essentially was a way to pin down the location of a point in space, any point, relative to a fixed point called the origin. Until the Cartesian co-ordinate system was invented, Geometry and Algebra were two different areas of Mathematics, but the co-ordinate system allowed the ability to describe a circle in 2-dimensional space or say a cylinder in 3-dimensional space in the form of an algebraic equation. More importantly, it laid the seeds for many vast areas of Mathematics, Calculus being the most noteworthy of them all.

{{< columns "60,40" >}}
René Descartes is known for more than just the coordinate system. As mentioned, he was a philosopher first and a mathematician later.

{{< hint info >}}
**I think, therefore I am**  
{{< /hint >}}

Or in Latin:
{{< hint info >}}
**Cogito, ergo sum**  
{{< /hint >}}

This one philosophical proposition that René Descartes came up with is so profound that it has become the fundamental element of Western philosophy.

In respect for his profound contribution and in line with the name of this [website]({{< ref "about" >}}), we devote a photograph in his memory.

<--->
{{< figure src="images/Rene_Descartes.jpg" class="figs" title="I think, therefore I am" >}}
{{< /columns >}}

### Depicting the function - take 3

Our third and final take on depicting real functions banks on the principles of the Cartesian coordinate system.

It is not clear if René Descrtes himself came up with this idea of depicting functions or if it was someone who built on the idea of Cartesian coordinates subsequently. But the idea is now ubiquitous with the depiction of functions everywhere in Mathematics. 

The idea is as follows:

- Recall that we are trying to depict a real function, i.e. a function that maps elements of set X of \\( \R \\) numbers to elements of set Y also of \\( \R \\) numbers.
- We realized that depicting these sets as ovals or circles was limiting, and that depicting each set using the number line provides better visualization.
- The next two steps are the key:
 - First, instead of depicting the sets X and Y as number lines parallel to each other, we place them perpendicular to each other! The convention has been to depict the set X as a horizontal number line, and the set Y as a vertical number line. Further we call the point of intersection of these lines as the origin and give it the coordinates \\( (0, 0) \\). This is really similar to setting up the Cartesian coordinate system.
 - Second, and this is the significant leap. As in take 2 above, we could have drawn lines connecting points on the numberline for set X with the points that they map to on the numberline for set Y. That would have been messy. Instead, we do the following:

> If there is an \\(x \\) in set X that maps to a certain \\( y\\) in set Y, then we mark the point \\( (x, y) \\) in the Cartesian coordinate system that we have set up.
>
> For e.g., if the element 3 in set X maps to the element 6 in the set Y, then we mark a point at the coordinates \\( (3, 6) \\).
>
> And we do this for all the points in set X. Practically, we will see that it is sufficient to do this for a few points to get a very good idea of the function.

For the doubling function above, we have a picture that looks as follows:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/Graph of a function v1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Once we have reached so far, the next step should be fairly obvious. We simply connect up the points we have plotted to have a picture of the function \\(f\\).

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/Graph of a function v2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

This idea must be familiar from high school, or probably also from middle school. This is really the entire history of what the **graph of a function** really means. 

If a point \\( (x, y) \\) lies on the graph of a function, it tells us that the function maps the real number \\( x\\) to the real number \\( y\\). The graph of a function is simply the collection of all points \\( (x, f(x)) \\) on the Cartesian coordinate system.

The significance of this idea is simply profound. When we do Calculus, we will learn that the derivative of a function can be interpreted as the slope of this graph, and the integral of a function can be looked at as the area under this graph. When we learn trigonometric functions or exponential functions, we will plot the graph of the function to visualize it easily. When we find roots of a polynomial, we will see that we are really looking at points where this graph cuts the x-axis. When we solve simultaneous equations, we are rally looking at two functions and finding where the graphs of the functions intersect. The idea just comes up again and again in many areas in Mathematics. 

## Function notations

We are now all ready to explore the vast and beautiful world of functions. But before we do that, we quickly look at a couple of additioanl notations for describing a function.

The above function can be very succintly described using the following notation:
$$ f(x) = 2\cdot x $$
This captures a lot of information in a very compact manner:

- Firstly, the name of the function is \\( f\\).
- By virtue of the use of \\( x\\), it is understood that the domain of this function is \\( \R \\).
- It is also understood that the co-domain of this function is \\( \R \\).
- It does not tell us anything about the range though, and different functions may have different ranges. In this case, of course, the range happens to be same as the co-domain, which is \\(\R\\).
- The notation \\( f(\bullet\) \\) conveys the idea that the function \\( f\\) *operates* on what is within the brackets, in this case \\( x\\) and maps it to something.
- The term on the right side of the \\( = \\) provides an algebraic expression for how the function operates on the elements on the domain.

When we say, \\( f(3) = 6 \\), it means that the function maps the element 3 of set X to the element 6 of set Y.

Occassionally, the function is also denoted as follows:
$$ f : x \mapsto 2\cdot x $$

This is a more set-like notation, in words it reads, \\(f\\) is a function that maps \\( x\\) to twice its value, and again captures all of the information described above.

Finally, when depicting the function as a graph, the following notation is commonly used:
$$ y = 2\cdot x $$

This can be read in two ways:

- In set terms, it says for a given \\( x\in X \\), the corresponding \\( y \in Y\\) that it maps to is given by the above expression.
- In graph terms, it says that if you know the x-coordinate of any point and you want to find the y-coordinate of the point on this graph, it is given by the above expression.

With that we stop this session on functions here, all geared for an adventurous exploration of the vast fields of Mathematics that have suddenly opened up for us.
