---
title: "Sets"
date: 2020-01-21T06:57:06+05:30
draft: false
weight: 1
---

In a class of 20 children, 5 of them like History, 10 of them like English and 15 of them like Math!! Do you think this is an impossible statement, or is it possible to have class of only 20 children where all the conditions above are satisfied? What if we are posed an additional question - what is the maximum number of students who may not like any of these three subjects?

Set theory can be used to answer such questions, as we will see shortly. But set theory goes way beyond this. Set theory is considered by many mathematicians as the foundations of pretty much all of mathematics, from which nearly all of mathematics can be derived! Such is the fundamental nature of set theory. For our pruposes, we will take a somewhat simplistic approach to set theory (what is called the naïve set theory or also the intuitive set theory defined using natural language rather than formal axioms) that still gives a pretty good flavor of the theory and its basic principles.

## Definition

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A **Set** is a well-defined collection of distinct objects. The objects that make up a set are known as the set's **elements** or **members**.
{{< /highlight-box >}}

### Examples

It is easy to find examples of sets, since the definition of a set is very broad and can include pretty much anything. Here are a few examples:

- The collection of all pieces of furniture in the room you are in can be called a set.
- The collection of all children in your class is another example of a set.
- The collection of books you read during the last summer vacation can be considered as a set.
- The collection of songs on your favorite playlist would be a set.

In fact, sets are so ubiquitous that it would very hard (if not impossible) to come up with non-examples of sets! Yet another e.g., the collection of all feelings you may have experienced in the last 10 minutes can also be considered a set.

### Describing a set

Sets are typically denoted using capital letters such as A, or B, or S, with subscripts as needed. Consider a set \\(S_I{}_N\\) defined as the collection of colors on the Indian national flag. The elements of this set \\(S_I{}_N\\) would be the colors - saffron, white, green and blue.

This set is depicted (using what is called the roster notation) as follows:

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/india_flag.png" class="figs" title="" >}}
\\(S_{IN}\\) = {saffron, white, green, blue}
<--->
{{< /columns >}}

Note the curly braces to enclose the elements of the set, in some ways to signify that the collection is well defined. Note also how the elements or members of the set are separated by commas. Further, the order of stating the elements of the set is not important, and a set has distinct objects, so all of the following are the same set S.

{{< columns "25,50,25" >}}
<--->
\\(S_{IN}\\) = {saffron, white, green, blue}  
\\(S_{IN}\\) = {white, saffron, green, blue}  
\\(S_{IN}\\) = {white, saffron, green, blue, blue}
<--->
{{< /columns >}}

### Depicting a set

Another way to depict the set somewhat pictorially is as follows:

{{< columns "35,30,35" >}}
<--->
{{< figure src="images/set.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Again, the circle or the oval shape signifies in some ways that the set is well defined. As before, the order of depicting the elements does not matter.
{{< columns "35,30,35" >}}
<--->
{{< figure src="images/set_2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

## Set membership

The notation used to capture the belongingness of an element (or not) to the set is as follows:

{{< katex >}}
\begin{array}{rcl}
\text{blue} & \in & S_{IN} \\
\text{red} & \notin & S_{IN} \\
\end{array}
{{< /katex >}}

The first line above in English would read - the element blue is in the set \\( S_{IN} \\), sometimes also read as - blue belongs to \\( S_{IN} \\). The second above reads - the element red is not in the set \\( S_{IN} \\), or also as - red does not blelong to \\( S_{IN}\\).

### Set equality

{{< highlight-box "Defn 2:" "none" "" "part" >}}
Two sets are said to be **equal sets** if and only if they have precisely the same elements. This is denoted simply as \\( A = B \\).
{{< /highlight-box >}}

Consider the flags shown below of Canada and Switzerland respectively. (For simplicity, we will assume that the shade of red in both the Canadian and the Swiss flags is exactly the same.)

{{< columns "60,10,30" >}}
{{< figure src="images/canada_flag.png" class="figs ba" title="" >}}
\\(S_{CN}\\) = {white, red}
<--->
<--->
{{< figure src="images/swiss_flag.png" class="figs" title="" >}}
\\(S_{SW}\\) = {red, white}
{{< /columns >}}

The two sets above are clearly equal since both the sets have exactly the same elements. Notice that the order of the elements does not matter.

{{< katex >}}
S_{CN} = S_{SW}
{{< /katex >}}

### Subsets

{{< highlight-box "Defn 3:" "none" "" "part" >}}
A set A is called a **subset** of a set B if every element of set A is also an element of set B. This is denoted as \\( A \subseteq B\\). This is same as saying set B is a **superset** of set A, and that is denoted as \\( B \supe A \\).

If A is a subset of B, but A is not equal to B i.e. there exists at least one element of B which is not an element of A, then A is a **proper subset** (or a strict subset) of B, denoted by \\(\displaystyle A\subset B\\) or equivalently B is called a **proper superset** (or a strict superset) of A.
{{< /highlight-box >}}

Consider the flags of Pakistan, Bangladesh and Maldives below (again, we will assume same shades for simplicity).

{{< columns "35,40,35" >}}
{{< figure src="images/pakistan_flag.png" class="figs ba" title="" >}}
\\(S_{PK}\\) = {white, green}
<--->
{{< figure src="images/bangladesh_flag.png" class="figs" title="" >}}
\\(S_{BD}\\) = {red, green}
<--->
{{< figure src="images/maldives_flag.png" class="figs" title="" >}}
\\(S_{MV}\\) = {red, white, green}
{{< /columns >}}

As it can be seen from the above, the set of colors in the flag of Pakistan is a subset of the set of colors in the flag of Maldives, and likewise the set of colors of the flag of Bangladesh is also a subset of the set of colors in the flag of Maldives. Written in set notation:

{{< katex >}}
S_{PK} \subset S_{MV} \\
S_{BD} \subset S_{MV}
{{< /katex >}}

Pictorially, this is depicted as shown below. 
{{< columns "30,40,30" >}}
<--->
{{< figure src="images/subset.png" class="figs" title="" >}}
<--->
{{< /columns >}}

It shows that all the elements of the set \\( S_{PK} \\) also belong to the set \\( S_M{}_V \\).

### Empty set

{{< highlight-box "Defn 4:" "none" "" "part" >}}
A set with no members is called the **empty set** (or the null set), which is denoted by the symbol \\( \varnothing \\).
{{< /highlight-box >}}

Since the empty set does not have any members, it is a *unique* set. What this means is that there aren't different sets such as an empty set of colors, different from an empty set of books, there is one and only one empty set, which does not contain any elements, no colors, no books, nothing in it.

Interestingly, the empty set is a subset of any and every set. For e.g., for the sets of colors of flags above,

{{< katex >}}
\varnothing \subset S_{PK} \subset S_{MV}
{{< /katex >}}

This can be depicted pictorially as below:
{{< columns "30,40,30" >}}
<--->
{{< figure src="images/empty set v2.png" class="figs" title="" >}}
<--->
{{< /columns >}}


### Power set

An interesting idea is that since by definition a set is a collection of objects, a set can be a collection of other sets as well. 

For e.g., consider the set \\( S_{MV} \\) consisting of 3 colors - {red, white, green}. What are *all possible* subsets of this set?

{{< highlight-box "Defn 5:" "none" "" "part" >}}
The set of all subsets of a set S is called the **power set** of S. And is typically denoted by \\( P(S) \\).
{{< /highlight-box >}}

The power set of the set \\( S_{MV} \\) is as shown below:

{{< katex >}}
P(S_{MV}) = \{\varnothing, \{\text{red}\}, \{\text{white}\}, \{\text{green}\}, \{\text{red, white}\}, \{\text{red, green}\}, \{\text{white, green}\}, S_{MV}\}
{{< /katex >}}

Note firstly that all elements of the power set above are themselves sets. In fact, by definition of the power set, they are all subsets of the original set. Also note that two special elements of the power set are the empty set and the original set itself.

### Cardinality

{{< highlight-box "Defn 6:" "none" "" "part" >}}
The number of elements of a set \\( S\\), is called the cardinality of the set and is denoted by \\( |S| \\)
{{< /highlight-box >}}

We can easily write the cardinality of soem of the sets we encountered above.
{{< katex >}}
\begin{array}{rcl}
|S_{PK}| & = & 2 \\
|S_{MV}| & = & 3 \\
|\varnothing| & = & 0 \\
\end{array}
{{< /katex >}}


{{< tabs "SET-1" >}}
{{< tab "Problem" >}}
Given a set \\( S \\) with cardinality say \\( n \\), i.e., the set \\( S\\) has \\(n\\) elements in it, what is the number of elements in the power set \\( P(S) \\) of \\( S\\)?

{{< /tab >}}
{{< tab "Hint" >}}
Is there a way to codify a subset of a set? 

Suppose a set has 3 elements, say \\( S = \lbrace a, b, c \rbrace \\)

Now consider a subset with just one element, say \\(\lbrace b \rbrace \\), can we represent that using \\( (0 1 0) \\)? 

Then how would we represent a subset, say \\( \lbrace a, b\rbrace \\)?

Now can we count the total number of subsets.

{{< /tab >}}
{{< tab "Solution" >}}

\\(2^n\\)

{{< /tab >}}
{{< /tabs >}}

## Set operations

Now that we have the basic building blocks ready, we can start playing with sets, adding them, subtracting them, etc. (imagine a kid with a new set of Lego blocks, the excitement may be similar :).

### Union of sets

We can define an operation over sets that looks somewhat like the addition operation. 

{{< highlight-box "Defn 7:" "none" "" "part" >}}
The **union** of set A and set B, denoted by \\(A \cup B\\), is the set of all objects that are members of either set A *or* set B.
{{< /highlight-box >}}

Consider the sets of colors in the flags of Pakistan and Bangladesh, what is the union of these two sets?
{{< katex >}}
\begin{array}{rcl}
S_{PK} & = & \{\text{green, white}\} \\
S_{BD} & = & \{\text{red, green}\} \\
S_{PK} \cup S_{BD} & = & \{\text{red, green, white}\} \\
\end{array}
{{< /katex >}}

Remember that the order of elements in a set does not matter. Remember also that a set contains only distinct elements. We used both these properties of a set in coming up with the union set above.

Some inferences about the union operation can be derived simply from the definition:
{{< katex >}}
\begin{array}{rcl}
A \cup A & = & A \\
A \cup \varnothing & = & A \\
\end{array}
{{< /katex >}}
In words, the first rule above says that the union of a set with itself is the same set, because by definition the union is the set of all objects that are either in A or B, in this case B is the same as A, and the set of all objects is thus the original set itself.

The second rule above should also be obvious. Since the empty set does not contain any elements, it does not *add* any newer elements when we consider its union with any set A.

We can derive more propoerties of the union operation, for e.g., the fact that the union operation is commutative and associative is captured below:

{{< katex >}}
\begin{array}{rcl}
A \cup B & = & B \cup A \\
A \cup (B \cup C) & = & (A \cup B) \cup C \\
\end{array}
{{< /katex >}}

Note that the equality relation above is set equality that we defined a little while earlier. Further note that both of the properties above hinge on just the basic definitions of sets - that they contain an *unordered* collection of *distinct* objects.

The union of two sets can also be depicted pictorially as follows:

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/set_union.svg" class="figs" title="" >}}
<--->
{{< /columns >}}

The example from above would look as follows:
{{< columns "30,40,30" >}}
{{< figure src="images/Set_S_PK.png" class="figs" title="" >}}
<--->
<--->
{{< figure src="images/Set_S_BD.png" class="figs" title="" >}}
{{< /columns >}}

And the union of both these sets would look as follows:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/Set_SPK_U_SBD.png" class="figs" title="" >}}
{{< katex >}}
\begin{array}{rcl}
S_{PK} \cup S_{BD} & = & \{\text{red, green, white}\} \\
\end{array}
{{< /katex >}}

<--->
{{< /columns >}}

Notice how the multiple sets are depicted with overlapping circles, and especially how elements common to both the sets are depicted *only once* and in the common area.

### Intersection of sets

{{< highlight-box "Defn 8:" "none" "" "part" >}}
The **intersection** of set A and set B, denoted by \\(A \cap B\\), is the set of all elements that are members of both set A *and* set B.
{{< /highlight-box >}}

Consider the sets of colors in the flags of Pakistan and Bangladesh, what is the intersection of these two sets?
{{< katex >}}
\begin{array}{rcl}
S_{PK} & = & \{\text{green, white}\} \\
S_{BD} & = & \{\text{red, green}\} \\
S_{PK} \cap S_{BD} & = & \{\text{green}\} \\
\end{array}
{{< /katex >}}

Some inferences about the intersection operation can be derived simply from the definition:
{{< katex >}}
\begin{array}{rcl}
A \cap A & = & A \\
A \cap \varnothing & = & \varnothing \\
\end{array}
{{< /katex >}}

In words, the first rule above says that the intersection of a set with itself is the same set, because by definition the intersection is the set of all objects that are both in A and B, in this case B is the same as A, and the set of all objects is thus the original set itself.

The second rule above should also be obvious. Since the empty set does not contain any elements, hence there are no elements which are in both the empy set and the set A, and hence the intersection is the empty set again.

As in the case of the union operation, we can derive more propoerties of the intersection operation, for e.g., the fact that the intersection operation is commutative and associative is captured below:

{{< katex >}}
\begin{array}{rcl}
A \cap B & = & B \cap A \\
A \cap (B \cap C) & = & (A \cap B) \cap C \\
\end{array}
{{< /katex >}}

The intersection of two sets can also be depicted pictorially as follows:

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/set_intersection.svg" class="figs" title="" >}}
<--->
{{< /columns >}}

The example from above would look as follows:
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/Set_SPK_I_SBD.png" class="figs" title="" >}}
{{< katex >}}
\begin{array}{rcl}
S_{PK} \cap S_{BD} & = & \{\text{green}\} \\
\end{array}
{{< /katex >}}

<--->
{{< /columns >}}

### Set builder notation

An extension of the roster notation is often very handy as we start performing operations with sets, and is called the set builder notation. This is best explained with an example.

Given set A and set B, the union of the two sets would be written in set builder notation as follows:
{{< katex >}}
\begin{array}{rcl}
A \cup B & = & \{x \, | \, x\in A \text{ or } x\in B\} \\
\end{array}
{{< /katex >}}

The way to read the first part of the notation \\( \lbrace x \, | \, \\) is as follows "the set of all \\(x\\) such that", and the second part of the notation following the \\( | \\) is the condition that the \\( x\\) satisfies. Taken togehter, the above notation in English would mean that \\( A \cup B \\) is the set of all elements, \\(x\\), such that \\(x\\) is in set A or \\( x\\) is in set B.

The definition for intersection can be likewise written in set builder notation as follows:
{{< katex >}}
\begin{array}{rcl}
A \cap B & = & \{x \, | \, x\in A \text{ and } x\in B\} \\
\end{array}
{{< /katex >}}


There are other set operations that can be studied, most notably, complement of a set, difference of two sets, etc. We will skip those here for they are not critical from understanding mappings and functions which we come to next. But before we go one, we will look one more set operation that will come in handy as we get into the next topics.

### Product of sets

Now that we have learnt the set-builder notation, we can succintly define the product of two sets, also called the Cartesian product.

{{< katex >}}
\begin{array}{rcl}
A \times B & = & \{(a, b) \, | \, a\in A \text{ and } b\in B\} \\
\end{array}
{{< /katex >}}

In words, The Cartesian product of two sets \\(A\\) and \\( B\\) is the set of all ordered pairs \\( (a, b) \\) such that the first element of the pair is from set \\( A \\) and the second element of the pair is from set \\( B\\). Ordered pairs \\( (a, b)\\) are also sometimes called as tuples.

A good example to understand Cartesian products of two sets is the following:
{{< katex >}}
\begin{array}{rcl}
R & = & \lbrace A, 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K \rbrace \\
S & = & \lbrace \spades, {\color{red} \hearts}, {\color{red} \diamonds}, \clubs \rbrace \\
\end{array}
{{< /katex >}}

Then the Cartesian product of the set of ranks, \\(R\\), and the set of suits, \\(S\\), is the entire deck of cards as shown below:
{{< katex >}}
\begin{array}{rcl}
R \times S & = & \lbrace (A, \spades), (2, \spades), (3, \spades), \ldots, (Q, \spades), (K, \spades), \\
& & \enspace (A, {\color{red} \hearts}), (2, {\color{red} \hearts}), (3, {\color{red} \hearts}), \ldots, (Q, {\color{red} \hearts}), (K, {\color{red} \hearts}), \\
& & \enspace (A, {\color{red} \diamonds}), (2, {\color{red} \diamonds}), (3, {\color{red} \diamonds}), \ldots, (Q, {\color{red} \diamonds}), (K, {\color{red} \diamonds}), \\
& & \enspace (A, \clubs), (2, \clubs), (3, \clubs), \ldots, (Q, \clubs), (K, \clubs) \rbrace \\
\end{array}
{{< /katex >}}

All of this can be depicted pictorially as follows:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/cross product.png" class="figs" title="" >}}
{{< katex >}}
\begin{array}{rcl}
R \times S & = & \lbrace (r, s) \, | \, r\in R \text{ and } s\in S \rbrace \\
\end{array}
{{< /katex >}}

<--->
{{< /columns >}}

It should be easy to guess the cardinality of the product of two sets:
{{< katex >}}
\begin{array}{rcl}
|A \times B| & = & |A| \cdot |B|
\end{array}
{{< /katex >}}

The cardinality of the set \\( B \times A\\) is also the same, but it is important to note that:
{{< katex >}}
\begin{array}{rcl}
\because (a, b) & \cancel{=} & (b, a) \\
\therefore A \times B & \cancel{=} & B \times A \\
\end{array}
{{< /katex >}}


