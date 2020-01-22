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

TBD.

{{< katex >}}
{{< /katex >}}

So, thats how we get \\(7^4\\) kittens in all.

## Combinatorial Principles

### Product Rule

#### How many pizzas

#### How many paths

#### How many cups, saucers and spoons

### Sum Rule

#### How many paths



