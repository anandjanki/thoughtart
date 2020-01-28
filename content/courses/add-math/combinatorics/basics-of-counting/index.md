---
title: "Basics of Counting"
date: 2020-01-18T19:38:25+05:30
draft: false
weight: 1
---

## Going to St Ives

We start with a counting riddle in the form of an English-language nursery rhyme from the 1700s. 
The poem goes as follows:

> As I was going to St Ives,   
> Upon the road I met seven wives;   
> Every wife had seven sacks,   
> Every sack had seven cats,   
> Every cat had seven kits:   
> Kits, cats, sacks, and wives,   
> How many were going to St Ives?   

There are many ways to answer this question. It was likely intended as a trick question, and not really a counting question. For, the author of the rhyme does not say where the seven wives were. They could even have been in towns or villages on the way to St Ives, or the author probably meant to say that he met them on the way, meaning that they were going in the other direction. If we follow this train of arguments, then we would conclude with an answer of just 1 - only the author was going to St Ives!

### Kittens galore

We can formulate a counting question from the poem above. Suppose we were to ask how many kittens were there in all, what would be the answer to that question?

Lets take say the first wife. This wife had seven sacks, lets take one of the sacks. This sack had 7 cats, lets take one of the cats. This cat had 7 kittens of course, but that's just one of the cats. There are 7 cats in the sack, and each of them has 7 kittens. So the total number of kittens in one of the sacks is 7 x 7 = 49. But that's just one of the sacks. There are 7 such sacks with the wife, and each sack has 49 kittens. So the total number of kittens in the 7 sacks with by the first wife - 7 x 7 x 7 = 343 kittens. Now, we can calculate the total number of kittens with all the 7 wives put together. That would be 7 x 7 x 7 x 7 = 2401 kittens. That's a lot of kittens.

It is important to notice how we counted the kittens:

    The First wife's --> First sack's --> First cat has => 7 kittens
    First wife's --> First sack --> has 7 cats with => 7x7 kittens
    First wife --> has 7 sacks with => 7x7x7 kittens
    Seven wives have => 7x7x7x7 kittens

A good way to represent this as a picture is below:

{{< figure src="StIves3.png" height="400px" class="figs" title="A picture to aid the counting of the kittens" >}}

{{< katex >}}
{{< /katex >}}

When we start counting, we may get large numbers and it is easy to lose track. It is hence of paramount importance while counting to do it very systematically. It is easy to see from the above picture, what would be the name of the 3rd cat in the 5th sack of the 2nd wife - that would be W2-S3-CAT#3, and this cat has 7 kittens.

So, thats how we get \\(7^4\\) kittens in all.

## Combinatorial Principles

Now that we have begun our foray into the world of counting, lets first get ourselves familiar with the basics. We will explore the couple of rules that will form the basic building blocks for the topics to follow, including permutations and combinations.

### Product Rule

The first rule is called the Product Rule and lets understand this with a few examples.

#### How many pizzas

Let's say we are at a pizza place and want to order a pizza. The restaurant provides a choice of 3 different bases to choose from, and 5 different cheeses to choose from. To make our own pizza, we can choose one of the 3 bases and one of the 5 cheeses to make our own custom pizza. The question is how many different unique base-cheese pairs are possible to make a pizza.

Lets call the bases B1, B2, and B3 (we could also use real names, say "Thin Crust", "Flat Bread" and say "Sicilian Base", but the counting and more importantly writing down the different possibilities gets a little cumbersome with the real names). We will of course call the cheeses C1, C2, C3, C4 and C5.

Suppose we decide to first try out base B1. Each day of the week, we can try the base B1 with a different cheese. These are listed out below:

{{< columns >}}

    B1 - C1
    B1 - C2
    B1 - C3
    B1 - C4
    B1 - C5

<--->

<--->

{{< /columns >}}

That's 5 different base-cheese pairs.

It should be easy to guess what we can do in the 2nd week and the week after.

{{< columns >}}

    B1 - C1
    B1 - C2
    B1 - C3
    B1 - C4
    B1 - C5

<--->

    B2 - C1
    B2 - C2
    B2 - C3
    B2 - C4
    B2 - C5

<--->

    B3 - C1
    B3 - C2
    B3 - C3
    B3 - C4
    B3 - C5

{{< /columns >}}

At the end of the third week, we have exhausted all possible base-cheese pairs that the restaurant has to offer. As its obvious to see, there are exactly 15 such unique base-cheese pairs possible.

This may seem a little trivial at the beginning. The answer may seem to be obviously 15, and we may wonder why go through all this trouble. But as we take on more challenging countings tasks, understanding this fundamental principle clearly will come in very handy.

The key point to note is the following - We have 3 different ways to choose the base. *Having chosen a base*, we have 5 different ways to choose the cheese. That's how we have 15 base-cheese pairs.

Stated differently - if there are 3 ways to choose a base **and** 5 ways to choose a cheese, then there are exactly **3 x 5** ways to make a base-cheese pair.

#### How many paths

Let's take another example. Suppose we board the school bus at Stop A, and the bus takes a route through Stop B to get to the school. Further suppose that there are 5 different ways to get from Stop A to Stop B, and 3 different ways to get from Stop B to the school. This is depicted in the picture below. The question we are asking is how many different ways are there to reach school from Stop A.

{{< figure src="Routes-A-B-C-v3.png" height="200px" class="figs" title="Different ways to reach school starting from Stop A, and going through Stop B" >}}

We could name the 5 routes between Stop A and Stop B as say AB1, AB2, ... AB5, and the routes between Stop B and Stop C as say BC1, BC2 and BC3. On the first day, we can take route AB1 from A to B, and route BC1 from B to C. On the second day, we could take AB1 again from A to B, but this time take route BC2 from B to C. If we do this systematically, the different possibilities will look as follows:

{{< columns >}}

    AB1 - BC1
    AB1 - BC2
    AB1 - BC3

<--->
    AB2 - BC1
    AB2 - BC2
    AB2 - BC3

<--->
    AB3 - BC1
    AB3 - BC2
    AB3 - BC3

{{< /columns >}}
{{< columns >}}
    AB4 - BC1
    AB4 - BC2
    AB4 - BC3

<--->
    AB5 - BC1
    AB5 - BC2
    AB5 - BC3

<--->

{{< /columns >}}

As before - if there are 5 ways to choose a path from A to B **and** 3 ways to choose a path from B to C, then there are exactly **5 x 3** different ways to go from A to C via B.

#### What to wear?

We can take this idea a step further. Suppose a boy's wardrobe looks like below - 5 different kinds of shirts, 3 different kinds of pants and 2 different kinds of shoes. How many different ways can he dress up to school?

{{< figure src="shirts-pants-shoes.png" height="300px" class="figs" title="Wardrobe of a boy with different choices to wear" >}}

The same rule applies - if there are 5 different ways to choose the shirt to wear **and** 3 different ways to choose a pant **and** 2 different ways to choose a shoe, then there are exactly **5 x 3 x 2** or 30 different ways to dress up to school.

As before, we can enumerate all these possibilities to check:

{{< columns >}}

    C1 - B1 - A1
    C1 - B1 - A2
    C1 - B2 - A1
    C1 - B2 - A2
    C1 - B3 - A1
    C1 - B3 - A2

<--->

    C2 - B1 - A1
    __ - B1 - A2
    __ - B2 - A1
    __ - B2 - A2
    __ - B3 - A1
    __ - B3 - A2

<--->

    C3 - B1 - A1
    __ - __ - A2
    __ - __ - A1
    __ - __ - A2
    __ - __ - A1
    __ - __ - A2

{{< /columns >}}

{{< columns >}}

    C4 - B1 - A1
    __ - __ - __
    __ - __ - __
    __ - __ - __
    __ - __ - __
    __ - __ - __

<--->

    C5 - __ - __
    __ - __ - __
    __ - __ - __
    __ - __ - __
    __ - __ - __
    __ - __ - __

<--->

{{< /columns >}}

Some of the possibilities are left blank above, and it is good to get some practice enumerating them out. As mentioned before, the the key thing to remember is to do it systematically. First choose the first shirt, then choose the first pant, having chosen the first shirt and the first pant, write out all possiblities for the shoes. Then go back to the pant choice, and choose the second pant. Having chosen the first shirt and the second pant, write out all the possibilities for the shoes again. Having exhausted all possible pant and shoe choices with the first shirt, then choose the second shirt and repeat the whole process.

#### The Product Rule

> If there are ``k`` ways of doing something, ``m`` ways of doing another thing, ``n`` ways of doing yet another thing, and so on, then there are ``k x m x n x ...`` ways of performing the combined action.

### Sum Rule

The Sum Rule goes as follows:

> If there are ``k`` ways of doing something, ``m`` ways of doing another thing, ``n`` ways of doing yet another thing and we can only do one of these, then there are ``k + m + n + ...`` ways to choose one of the actions.

#### Choice of Subject

Let's say you have picked Math and Science as your main subjects, and let's say that you have to choose any 1 additional subject from either an Arts or Sports area. Suppose your school offers 5 different Arts courses - Literature, Painting, Music, Photography and Sculpting, and 3 different Sports courses - Basketball, Swimming and Athletics. How many ways are there in which you can choose your additional subject.

Note that you can only choose 1 additional subject. You can either choose one of the 5 Arts subjects, **or** you can choose one of the 3 Sports subjects. So, the number of ways in which you can choose your additional subject is simply **5 + 3**, or 8 different ways.

As before, it may seem too obvious to make a fancy rule out of this idea. But we will see the importance of this as we take on more complex counting problems and next one below should serve as an example.

### Both rules together

What if we are faced with a situation where some of the actions have to be done together one after the other, while some of the options are alternatives to other options. An example will help clarify.

#### How many paths

Let's revisit the path counting problem, except that we have some new developments to deal with. It turns out there are other alternative ways to get to the school from Stop A. This is depicted in the picture below.

{{< figure src="Routes-A-BD-C.png" height="200px" class="figs" title="Different ways to reach school starting from Stop A, and going through Stop B or going through Stop D" >}}

We had already calculated the number of ways of reaching school through Stop B before, that is 5 x 3 ways. The presence of Stop D provide alternative routes to reach the school. The bus can either go from A to B to C, **or** it can go from A to D to C. The number of ways to reach school from A, going via D should be easy to calculate - it is 2 x 1 ways (since there are 2 ways to reach from A to D, and 1 way to reach from D to school). So, the total number of ways to reach school in this new scenario works out to be **5 x 3 + 2 x 1**, or exactly 17 ways. 

Notice how we have used multiplications and additions as appropriate in arriving at the above.

All the possible ways are enumerated below, and notice that the 2 new ways simply get added to the 15 ways that were available before.

{{< columns >}}

    AB1 - BC1
    AB1 - BC2
    AB1 - BC3

<--->
    AB2 - BC1
    AB2 - BC2
    AB2 - BC3

<--->
    AB3 - BC1
    AB3 - BC2
    AB3 - BC3

{{< /columns >}}
{{< columns >}}
    AB4 - BC1
    AB4 - BC2
    AB4 - BC3

<--->
    AB5 - BC1
    AB5 - BC2
    AB5 - BC3

<--->

    AD1 - DC1
    AD2 - DC2

{{< /columns >}}

### Practice Problems

One of the best ways to learn how these two rules work is to come up with problems of your own. Try and come up with at least one problem with needs the applicaiton of the product rule, 1 that needs application of the sum rule, and one that needs both.

Here is a problem that needs both.

{{< tabs "BOC-1" >}}
{{< tab "Problem" >}}

This family is planning a vacation for the year. 

They can either go on a summer vacation or a winter vacation but not both. There are 4 places they have shortlisted for the summer vacation, and there are 3 places they have shortlisted for the winter vacation. 

They always go on vacation along with one other family. There are 5 other friends who would be interested in joining the summer trip along with their family. There are 4 relatives who would be interested in the winter trip each along with their family.

How many different possiblities does the family have for their vacation this year?

{{< /tab >}}

{{< tab "Hint" >}}

One way is to use the sum and product rules directly.

The other way to work this out is to enumerate all the possibilities. Call the summer places S1, S2, S3, S4 and the winter places W1, W2 and W3. Call the summer travel companions as F1, F2, F3, F4, F5 and the winter companions as R1, R2, R3 and R4. Now what are the different possibilities? Start with summer option S1, the family can go to S1 along with one of F1, F2, ..., F5. And enumerate it all.

Do try to do this in both ways. First apply sum and product rules to arrive at the answer. Then verify it by enumerating all the possibilities.

{{< /tab >}}

{{< tab "Solution" >}}

The family can either take a summer vacation or a winter vacation, not both.

- For the places to visit in summer, the family has 4 choices, and for travel companions they have 5 choices. So, there are 4 x 5 ways in which they can take their summer vacation.
- For places to visit in winter, the family has 3 choices, and travel companions they have 4 choices. So, there are 3 x 4 ways in which they can take their winter vacation.

Thus, the total number of ways in which they can take a vacation is then 4 x 5 + 3 x 4 = 32 ways.

Since the numbers involved are not too large, we can enumerate out the ways and verify as below:

{{< columns >}}
    S1 - F1
    S1 - F2
    S1 - F3
    S1 - F4
    S1 - F5

<--->
    S2 - F1
    S2 - F2
    S2 - F3
    S2 - F4
    S2 - F5

<--->
    S3 - F1
    S3 - F2
    S3 - F3
    S3 - F4
    S3 - F5
{{< /columns >}}

{{< columns >}}
    S4 - F1
    S4 - F2
    S4 - F3
    S4 - F4
    S4 - F5
<--->

<--->

{{< /columns >}}

{{< columns >}}
    W1 - R1
    W1 - R2
    W1 - R3
    W1 - R4

<--->
    W2 - R1
    W2 - R2
    W2 - R3
    W2 - R4

<--->
    W3 - R1
    W3 - R2
    W3 - R3
    W3 - R4

{{< /columns >}}

{{< /tab >}}
{{< /tabs >}}

