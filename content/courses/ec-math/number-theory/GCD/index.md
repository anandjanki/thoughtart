---
title: "1.1 Greatest Common Divisor"
date: 2020-02-03T19:40:47+05:30
draft: false
weight: 1
custom_css: ["css/foo.css"]
---

## Multiplication

Let’s start with the basics first. We have learnt since childhood that multiplication is simply repeated addition. For eg, 3 x 4 is really the “shorthand notation” for saying 3 + 3 + 3 + 3.

Where does multiplication show up practically, in real life? Suppose you have a room that is 3m wide and 4m long. How many 1m square tiles are needed to cover the room?

If the room were 3m x 1m, then it needs 3 tiles obviously. Now, if you repeat that 4 times, then you can find out how many tiles are needed. This is shown in the picture below.

{{< columns >}}
{{< figure src="images/3x1=3.png" class="figs" title="3 x 1 = 3" >}}
<--->
{{< figure src="images/3x4=12.png" class="figs" title="3 x 4 = 12" >}}
{{< /columns >}}

Let’s do some quick mental multiplication problems. Each time, visualize the room with the dimensions of the two numbers being multiplied and feel the total number of tiles in the room.

{{< columns >}}

    4 x 6 = 
    6 x 7 = 
    7 x 9 = 
    8 x 4 = 
    9 x 6 = 
    7 x 8 = 

<--->

    3 x 10 = 
    8 x 10 = 
    10 x 6 = 
    6 x 0 = 
    0 x 3 = 
    0 x 0 = 

<--->

    3 x 3 = 
    6 x 6 = 
    8 x 8 = 
    8 x 1 = 
    1 x 1 = 
    12 x 15 = 

{{< /columns >}}

{{< highlight-box "QTP-1" >}}
Did you find it easy to do multiplications with the number 10? Why?
{{< /highlight-box >}}
<br/>
{{< highlight-box "QTP-2" >}}
How about this multiplication below? Is there a way to calculate the number of tiles needed without resorting to a calculator or even rough work area - simply mentally?

{{< columns >}}

<--->

             2 0 4 1 5
             x 8 2 3 1
    \-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-
                       ?
    \-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-

<--->

{{< /columns >}}

{{< /highlight-box >}}

We will revisit these questions when we do Polynomials in Algebra.

### The Largest Tile Size

Now, imagine a room that is 6m wide and 9m long. The answer to how many 1m square tiles are needed to fill this room is simple - we need `_____` tiles. But lets ask a different question. We want to tile the room with larger size square tiles. What is the largest sized tile that we can use?

{{< figure src="images/1x1-tiling.png" class="figs" title="" >}}
{{< figure src="images/2x2-tiling.png" class="figs" title="" >}}
{{< figure src="images/4x4-tiling.png" class="figs" title="" >}}

But what about 3m square tiles? 

As you can see from the picture below, 3m square tiles beautifully cover the complete room, just like 1m square tiles had covered it. 

{{< figure src="images/3x3-tiling.png" width="85%" class="figs" title="" >}}

Now, remember the question we are asking - what is largest sized square tile that can be used to cover the room completely? Is the answer 3m square tiles? Turns out that is correct. We can check 5m and 6m square tiles to verify. Note that 7m square tiles or any size above that won’t work, simply because one side of the room is only 6m. 

This number, 3, is called the Greatest Common Divisor (GCD) of 6 and 9.

Let’s take a few more examples:

{{< columns >}}

{{< table "horizontal-table" >}}
| Room Size | Largest size square tile? |
|-----------|---------------------------|
| 6m x 6m   |                           |
| 9m x 9m   |                           |
| 1m x 8m   |                           |
| 7m x 1m   |                           |
{{< /table >}}

<--->

{{< table "horizontal-table" >}}
| Room Size | Largest size square tile? |
|-----------|---------------------------|
| 5m x 10m   |                           |
| 15m x 5m   |                           |
| 8m x 9m   |                           |
| 13m x 14m   |                           |
{{< /table >}}

{{< /columns >}}

In the rest of this session, we will explore the GCD of two numbers in more detail.

## Divisors

When we multiply two numbers, we get a result that is a fixed number. We always get the same result, right, no matter how we do the multiplication. We can do it on a calculator, on a computer, or in our mind, it does not matter. We can do it using some long method, short method, or any other method, it does not matter.

But what about the reverse?

Given a number, if we try to find some two numbers whose multiplication will yield that original number - is it always fixed? Will we always get the same two numbers? Lets try.

Suppose the given number is 12. Find two numbers which when multiplied will yield 12? What is the answer? 3 and 4? If we ask someone else the same question, will we get the same answer? Someone else may say 2 and 6. Yet another person may say 1 and 12. So, there can be many answers to the question - find two numbers when multiplied yield 12.

We can play this game with tiles as well. Lets take 12 scrabble pieces and form rectangles.

{{< figure src="images/12-scrabble-tiles.png" class="figs" title="" >}}

{{< highlight-box "QTP-3" >}}
Will there always be many rectangles? If you are given a number, will there always be many different ways in which you can multiply two numbers and get that number?
{{< /highlight-box >}}

There is only one answer to that question :) and we will find out soon.

Now, lets take slightly larger numbers and see.

{{< columns >}}

    _______ x _______

    _______ x _______
                       =  24
    _______ x _______

    _______ x _______

<--->

    _______ x _______

    _______ x _______
                       =  30
    _______ x _______

    _______ x _______

{{< /columns >}}

{{< columns >}}

    _______ x _______
                       =  49
    _______ x _______

<--->

    _______ x _______

    _______ x _______

    _______ x _______  =  36
                      
    _______ x _______

    _______ x _______

{{< /columns >}}

These are called the factors of a number. They are also called divisors.

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A number \\(b\\) is said to be a divisor of a number \\(a\\) if there exists a number \\(q\\) such that:

$$ a = q\cdot b $$
\\(b\\) is said to divide \\(a\\), and that is written as:
$$ b \| a $$
That is the same as saying:

- \\(a\\) is divisible by \\(b\\), or 
- \\(a\\) is a multiple of \\(b\\), or
- \\(b\\) is a factor of \\(a\\), or 
- \\(b\\) is a divisor of \\(a\\).

{{< /highlight-box >}}

From the above examples we tried, we can say 12 divides 24, or more succinctly, 12 | 24.

{{< highlight-box "HDMT-1" "color-content" >}}
Mathematicians love symbols and use them to express their ideas succinctly.
{{< /highlight-box >}}


### A brief historical note

What do you feel when you see a Math textbook full of symbols of different kinds? 

{{< columns >}}

{{< figure src="images/math-blackboard.png" class="figs" title="" >}}

<--->

Or a blackboard from a typical Math class?

What are all these symbols, how do we read what’s written?

Are these symbols from some divine language?

{{< /columns >}}

Well, when it started, Math was written as prose and poetry, there were no symbols. 

Old Greek mathematics was a collection of prose.

{{< figure src="images/greek-for-multiplication.png" class="figs" title="" >}}

Vedic mathematics was a collection of sutras.

{{< figure src="images/vedic-sutras.png" class="figs" title="" >}}

{{< columns >}}

Mathematical lunacy: for a short time the symbol for positive and negative was a moon. The equation above is -4 + 6 = 2

<--->

{{< figure src="images/positive-negative-sign.png" class="figs mt0" title="" >}}

{{< /columns >}}


{{< columns >}}

And the first time that a symbol was used for “equals to” was as late as 1500s. The + and - signs were introduced in 1300 and 1400, while the x sign came about in 1600s.

<--->

{{< figure src="images/equals-sign.png" class="figs mt0" title="" >}}

{{< /columns >}}

All these symbols were invented by humans like us, to simply make the task of communicating their ideas easier. 

When we see a math symbol, all that we need to do is to look up the definition of the symbol, and then we know what it means. Never fear, and we can even come up with new ones of our own!!

### Finding Divisors of a number

How do we find ALL the divisors of a number? Systematically? It’s simple. We keep asking this question:

- Is 1 a divisor?
- Is 2 a divisor?
- ... ...

Until we are sure we can stop asking!

Is it possible to stop asking the question after some time? Or will we have to keep asking endlessly?

Suppose we are trying to find the divisors of 120. Do we need to ask the question - is 121 a divisor? Do we need to ask - is 122 a divisor? Clearly no. Why? Because no divisor of a number can be greater than the number itself. If b were greater than a, then it is impossible to find a number q such that `a = q . b`. Remember, multiplication is repeated addition, and it is impossible to repeatedly add the number b and get a, if b > a. 

If d is a divisor of 120, then this is written as:
$$ 1 \leq d \leq 120 $$
In words, d is greater than or equal to 1 and less than or equal to 120. 

So, we can stop asking at 120 because the answer to all questions that follow is NO.

Now, how do we answer one particular question, say, is 20 a divisor of 120? Straight from the definition. If we can find a number q, such that `120 = q . 20`, then it is. Can we?

Shall we do that. Let’s mark all the divisors of 120 in the table below.

{{< table "normal-table" >}}
| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 |
| --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: | --: |
| 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 |
| 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 | 49 | 50 | 51 | 52 | 53 | 54 | 55 | 56 | 57 | 58 | 59 | 60 |
| 61 | 62 | 63 | 64 | 65 | 66 | 67 | 68 | 69 | 70 | 71 | 72 | 73 | 74 | 75 | 76 | 77 | 78 | 79 | 80 |
| 81 | 82 | 83 | 84 | 85 | 86 | 87 | 88 | 89 | 90 | 91 | 92 | 93 | 94 | 95 | 96 | 97 | 98 | 99 | 100 |
| 101 | 102 | 103 | 104 | 105 | 106 | 107 | 108 | 109 | 110 | 111 | 112 | 113 | 114 | 115 | 116 | 117 | 118 | 119 | 120 |
{{< /table >}}

### Finding divisors faster

Did it take a lot of work? What if we had to do the same for a bigger number, say 500? Can we do it faster? 

{{< highlight-box "HDMT-2" "color-content" >}}
Mathematicians like to discover faster and better ways to solve problems.
{{< /highlight-box >}}

It turns out that we can do this much faster than we first did. We don’t need to check all 120 numbers. We can finish by simply checking some 10 or 11 numbers !!

{{< table "normal-table" >}}
| Is 1 a divisor of 120? | YES | 1 x 120 = 120 | 1, 120 |
| :-- | :-- | --: | --: |
| Is 2 a divisor of 120? | YES | 2 x 60 = 120 | 2, 60 |
| Is 3 a divisor of 120? | YES | 3 x 40 = 120 | 3, 40 |
| Is 4 a divisor of 120? | YES | 4 x 30 = 120 | 4, 30 |
| Is 5 a divisor of 120? | YES | 5 x 24 = 120 | 5, 24 |
| Is 6 a divisor of 120? | YES | 6 x 20 = 120 | 6, 20 |
| Is 7 a divisor of 120? | <span style="color:red;">NO</span> |  |  |
| Is 8 a divisor of 120? | YES | 8 x 15 = 120 | 8, 15 |
| Is 9 a divisor of 120? | <span style="color:red;">NO</span> |  |  |
| Is 10 a divisor of 120? | YES | 10 x 12 = 120 | 10, 12 |
| Is 11 a divisor of 120? | <span style="color:red;">NO</span> |  |  |
| Is 12 a divisor of 120? | YES | 12 x 10 = 120 | Already DONE !!! |
{{< /table >}}

As we can see from the above table, once we cross 11, we find that we already know that 12 is a divisor because `10 x 12 = 12 x 10 = 120`. 

That’s great. But, should we check if 13 is a divisor? What about 14? Or can we confidently say that 15 is the next divisor after 12?

If 14 were a divisor of 120, then we have to find a number q such that 120 = q . 14. If there were such a q, what is our guess? Would it be less than 14 or more than 14?

Let’s do this with an example. We have 36 Scrabble tiles and have arranged it in a square as shown in the left below. 6 x 6 = 36. Suppose we move the tiles around and try to create a rectangle where one side has greater than 6 tiles, say it is 9 tiles long. Then what will be the size of the other side of the rectangle? Will it be less than 6 or greater than 6? Clearly, less than 6, because if both sides were greater than 6, then we will need more than 36 tiles.

{{< figure src="images/6x6-9x4-tiles.png" class="figs" title="" >}}

The question we are asking is this:

If `a.a = b` and `c.d = b`, suppose `c <= a`, then can we say that `d >= a`.

We will encounter a lot of such problems, where we have a few facts given, and we have to uncover new facts based on that. This is how the field of Mathematics (and in general, Science) has evolved.

We will not try to prove this one now, and leave it as a QTP.

{{< highlight-box "QTP-4" >}}
If `a.a = b` and `c.d = b`, and suppose `c ≤ a`, then prove that `d ≥ a`.
{{< /highlight-box >}}

Now going back to our original problem, while 120 is not a perfect square like b above, we can still apply similar techniques. 100 is a perfect square and `10.10 = 100`, and suppose we are trying to find the divisors of 100, then we can stop at 10. Why? Because if we find any divisor, say c, such that `c > 10` and `c.d = 100`, then we can be sure that `d < 10`. But since we have already covered all numbers less than 10, we would have already found c.

The next square after 100 is `121 = 11.11`. Since we are trying to find the divisors for 120, we can stop searching at 10. Isn’t that a big relief, instead of checking all 120 numbers!?

Find the divisors of these numbers below:

{{< columns >}}

{{< table "horizontal-table" >}}
| N | List of divisors  |
| :-- | :-- |
| 64 | 1, 64, 2, 32, 4, 16, 8 |
| 72 |   |
| 500 |   |
| 420 |   |
| 37 |   |
| 97 |   |
{{< /table >}}

<--->

{{< /columns >}}

How many numbers need to be checked for finding the divisors of 97 above? Do we need to check all numbers up to 97? Or can we stop checking much earlier, say at 9, since 100 is the nearest square? If we check only until 9, and we do not find any divisors, can we stop checking and claim that there are no divisors other than 1 and 97 itself? Or do we feel worried we may have missed something? What if there is some divisor between 10 and 96?

If there were some divisor in that range, say a, then what do we know about the other number, say b, that when multiplied by a may yield 97. 

If \\(a\cdot b = 97\\) and if \\(a > 9\\), then \\(b \leq 9 \\)

### Prime Numbers

What is special about 37 and 97 above? The only divisors that these numbers have are 1 and the number itself. These numbers, as we may be familiar, are called prime numbers.

A number P is said to be a prime number if P has no divisors expect 1 and P itself. All other numbers are called composite numbers. The only exception is 1. 1 is considered neither prime, nor composite.

Can we now attempt QTP 3?

Prime numbers are very special and we will spend a lot of time with them in a subsequent session.

### Properties of Divisors

Since we have spent a fair bit of time understanding what divisors are, we should explore a little more about them. We already saw one of them earlier (that the divisor of a number has to be less than or equal to the number).

- If \\(b | a\\), then \\(1 ≤ b ≤ a\\)
- If \\(a | b\\) and \\(b | c\\), then \\(a | c\\)
- If \\(a | b\\), then \\(a | kb\\) for any number \\(k\\)
- \\(a | b\\) if and only if \\(na | nb\\) for any \\(n > 0\\)

Do take a minute to go over each of these properties and speak them out in English. That will help in translating seemlessly between math symbols and the meaning they convey.

Each of the above properties need to be proved. We do not need to commit these to memory, but we need to understand each of these properties well. Do they all follow from the basic definition of a divisor, if so how. This is how the field evolves, someone discovers properties such as the ones above, proves them, and they become facts. Then someone else comes along uses all the facts discovered so far and then discovers a newer fact. It is almost like a living organism that is constantly growing! The original seed was just a simple definition.

## Greatest Common Divisor

Now we are all set to dive into the topic of this session - GCD. 

We now know how to find the divisors of a number. Some mathematician along the way decided (s)he wanted to have more fun and asked the question - what if we have two numbers and look at the divisors of both the numbers, are there divisors in common?

{{< highlight-box "Defn 2:" "no-colors" "" "part-borders" >}}
If a number \\(c\\) divides two numbers \\(a\\) and \\(b\\), i.e.

\\(c | a\\), and \\(c | b\\)

then \\(c\\) is called a common divisor of \\(a\\) and \\(b\\).

{{< /highlight-box >}}

Let’s start with a few examples.

{{< columns >}}

{{< table "horizontal-table" >}}
| N | Divisors  |
| :-- | :-- |
| 100 |   |
| 120 |   |
| Common <br/> Divisors |   |
{{< /table >}}

<--->

{{< /columns >}}

We can also depict this as a Venn Diagram:

{{< figure src="images/venn-divisors-100-120.png" class="figs" title="" >}}

What about 37 and 97. What are the common divisor(s) of 37 and 97? __________

Now, the definition of Greatest Common Divisor should be straightforward. The greatest of the common divisors is called the GCD. More formally:

{{< highlight-box "Defn 3:" "no-colors" "" "part-borders" >}}
A number \\(g\\) is said to be the greatest common divisor of \\(a\\) and \\(b\\) if it satisfies the following:

- \\(g | a\\) and \\(g | b\\), 
- If \\(c | a\\) and\\(c | b\\), then\\(c ≤ g\\). 

The GCD of two numbers\\(a\\) and \\(b\\) is represented as \\((a, b)\\)
{{< /highlight-box >}}

Lets see how to compute the GCD. We have already seen how to compute all divisors of a number quickly. Given two numbers, we can simply compute the divisors of both the numbers, then find the common divisors, and finally find the greatest of them.

{{< columns >}}

{{< table "horizontal-table" >}}
| N | Divisors  |
| :-- | :-- |
| 100 |   |
| 120 |   |
| Common <br/> Divisors |   |
| GCD |   |
{{< /table >}}

<--->

{{< /columns >}}

### Finding the GCD fast
But, is there a faster way to find the GCD? Remember HDMT 2 - Mathematicians like to discover faster and better ways to solve problems. If we have to find the GCD of 3645 and 2115, it seems quite tedious finding all the divisors and then proceeding to find the common divisors followed by finding the GCD.

To find a simpler way, let’s go back to the largest tile problem. Let’s take the 6m x 9m room that we had talked about. 

The first thing to note is that any square tile that completely fills the room is a common divisor of both 6 and 9. Why? Because it divides the 6m side into some equal parts and it also divides the 9m side into some different number of equal parts.

Recall that 2 is NOT a common divisor as shown in the picture below. It divides the 6m side into 3 parts, but it fails to divide the 9m side.

{{< figure src="images/2x2-tiling.png" class="figs" title="" >}}

We had found that 3m square tiles are the largest tiles that cover this room as shown below.

{{< figure src="images/3x3-tiling.png" width="85%" class="figs" title="" >}}

The key thing to note in order to discover a faster way is that the 3m square tiles completely tile the 6m x 9m room, therefore they would also tile a 6m x 6m room, and hence crucially they would also tile a 6m x 3m room! In other words, we can ignore the 6m x 6m room and focus on the *smaller* 6m x 3m room to find out the largest size tile! 

{{< figure src="images/ignore-6x6.png" class="figs" title="" >}}

If the room size was 4m x 9m, then we can ignore two 4m x 4m parts and focus only on the 4m x 1m part of the room to find the largest tile size.

{{< figure src="images/ignore-4x8.png" class="figs" title="" >}}

The next crucial thing to note is that we can do this process repeatedly (or “recursively”).

To find the largest tile that covers say a 9m x 15m room:

1. First ignore the 9m x 9m part of the room. Then, the leftover part is 9m x 6m. 
1. In this part, ignore the 6m x 6m part. Then, the leftover part is 3m x 6m. 
1. Finally ignore the 3m x 3m part. Then, the leftover part is 3m x 3m. 
1. And that is largest size tile.

{{< figure src="images/ignore-9x9-6x6-3x3.png" class="figs" title="" >}}

We can work backwards to check that the 3m square tile can indeed tile the 3m x 6m room, and in turn tile the 9m x 6m room, and finally also tile the 9m x 15m room.

To find the GCD of 100 and 120, we just need to do:
$$ (120, 100) = (100, 20) = 20 $$

Doesn’t that look magical? Sometimes mathematics looks like magic, simply enthralling. But the magician always knows how the trick works. So does a mathematician!!

Now, lets understand how this magic works. We will need to get behind the curtains and take one step at a time to unravel this mystery. We’ll start with properties of GCD.

## PROPERTIES of GCD

First, a few properties of divisors in general:

1. \\(1 \| a\\) \\(\forall a\\)
1. \\(a \| a\\) \\(\forall a \neq 0\\)
1. \\(a \| 0\\) \\(\forall a \neq 0\\)

(\\( \forall \\) is the symbol for "for all")

Can we accept that these are correct? How do we do that? By asking for proof!

{{< highlight-box "HDMT-3" "color-content" >}}
Mathematicians do not accept anything blindly. They always ask for proof.
{{< /highlight-box >}}

So, what are these proofs? Proofs are logical step-by-step arguments made using previously proven claims. They usually start from a definition to logically prove a few claims. Once a claim is proven, it becomes a fact. With these facts, more claims can be proven using the original definition and all the facts that we know so far.

Its a bit like constructing a building. You have to start with the foundation, then construct the ground floor and then the first floor and so on. The terrace on the topmost floor comes last and stands on every single brick that has been laid before it. If any floor is weak, all the floors above will come crashing.

The proofs for some claims are very simple, take only a line or two. But some proofs can be extremely long. And hard. One such example is Fermat’s last theorem. Fermat wrote the theorem in the margin of his book, but it took 358 years before it was proved!! Its proof took about 129 pages. Most proofs though take only a few lines, say half a page or so. 

Lets take the first property - \\(1 \| a\\) \\(\forall a\\)

In words, what it claims is that 1 is a divisor of all numbers. But we know that, dont we. Well, HDMT 3 - it has to be proved. What do we know to prove this? So far, only the definition of a divisor.

So, to prove that 1 is a divisor of any number a, we have to simply find q given any number a. Is that easy? Yes.

{{< theorem-block "Claim" "Proof" >}}

\\(1 | a\\) \\(\forall a\\)

<--->

\\(\forall a\\), \\(a = a\cdot 1\\)

\\(\therefore 1 \| a\\)

Hence proved.

{{< /theorem-block >}}

(\\(\therefore \\) is the symbol for therefore)

In words, we know that for all a, a multiplied by 1 is a itself. Therefore, given any a, the search for a number q such that q multiplied by 1 is equal to a is very easy. The q is a itself. Since we have found the number q, we can can therefore say that 1 divides a.

The other two properties can also be proved in the same fashion.

Lets look at a fourth property that needs a slightly longer proof.

{{< theorem-block "Claim" "Proof" >}}

If \\(a | b\\) and \\(b | c \\), then \\(a | c\\)

<--->

\\(\because a | b\\), \\(\exists q_1\\) such that \\(b = q_1\cdot a\\)  
\\(\because b | c\\), \\(\exists q_2\\) such that \\(c = q_2\cdot b\\)

Now, \\( c = q_2\cdot b \\)
\\( = q_2\cdot q_1\cdot a \\)
\\( = q\cdot a \\)   
where \\( q = q_1\cdot q_2\\)

\\( \therefore a | c \\)

Hence proved.

{{< /theorem-block >}}

(\\(\because \\) is the symbol for since or because)   
(\\(\exists \\) is the symbol for there exists)

Claims are often called Theorems in Mathematics, and we will see them a lot going forward.

Here is another property of divisors, a really interesting one. The proof itself is fairly simple, but this property is quite insightful, and we will look at it carefully.

{{< theorem-block "Theorem" "Proof" >}}

If \\(a | b\\) and \\(a | c \\), then \\(a | (b\cdot x + c\cdot y) \\) for any numbers \\(x\\) and \\(y\\)

<--->

\\(\because a | b\\), \\(\exists q_1\\) such that \\(b = q_1\cdot a\\)  
\\(\because b | c\\), \\(\exists q_2\\) such that \\(c = q_2\cdot b\\)

Now,

{{< katex >}}
\begin{array}{rcl}
b\cdot x + c\cdot y & = & q_1\cdot a\cdot x + q_2\cdot a\cdot y \\
& = & (q_1\cdot x + q_2\cdot y)\cdot a \\
& = & q\cdot a
\end{array}
{{< /katex >}}
where \\( q = q_1\cdot x + q_2\cdot y\\)

\\( \therefore a | (b\cdot x + c\cdot y) \\)

Hence proved.

{{< /theorem-block >}}

Lets take some sticks and see what the above means. Lets say we have one stick of length b and another stick of length c. Both these sticks are divisible by sticks of length a. That means we can take some number of sticks of length a and stick them together (no pun intended :) to form the stick of length b. We can take a (possibly) different number of these smaller sticks of length a to form the stick of length c.

{{< figure src="images/sticks-b-and-c.png" class="figs" title="" >}}

If we join the two sticks to make a long stick of length b + c, that long stick will also be divisible by a. In other words, we can take a number of small sticks of length a and join them together and it will be possible to make a stick of length b + c. If say 5 sticks of length a are needed to make b, and say 8 sticks of length a are needed to make c, then with 13 sticks of length a, we can make the longer stick of length b + c. Child’s play, right?

{{< figure src="images/sticks-b+c.png" class="figs" title="" >}}

In fact, you can x sticks of length b and y sticks of length c and this (very long) stick of length \\(b\cdot x + c\cdot y\\) is also divisible by a.

Of special mention is the fact that you can take x sticks of length b and 0 sticks of length c, and this long stick of length b.x is divisible by a. That means if a divides b, then a also divides all multiples of b. Is that a simple property to prove? Well, we have already proved it. Remember we say that a divides b.x + c.y for any numbers x and y. That includes the case where y is 0. Or for that matter x is zero, i.e., a divides all multiples of c.

Now for the interesting part. 

It turns out that if you take the stick of length c, and break away length b from it, to be left with a stick of length c - b, then that stick is also divisible by a.

{{< figure src="images/sticks-c-b.png" class="figs" title="" >}}

Why is this interesting? Because, it helps us reduce the complexity of the problem we are solving. 

What we proved in the theorem above is that if we know a is a divisor of b and a is a divisor of c, then a is a divisor of \\(b\cdot x + c\cdot y\\), in particular, a is a divisor of \\(c - b\\) (which is \\(b\cdot -1 + c\cdot 1\\)). 

Imagine two sticks of length 200 and say 1017. Finding the factors of 200 we have seen does take some time. Finding factors of 1017 might take longer (What are the factors?). But from the previous discussion we know that if we put 5 of the 200-length sticks together we will get a 1000-length stick and then subtracting from 1017 will give us a 17-length stick. Now we can say that if we find a common divisor of 200 and 17, then we would have also found a common divisor for 200 and 1017. That is how it helps us reduce the complexity of the problem. (What are the common divisors of 200 and 17?)

### Linear combinations of a & b

Let’s consider the set of all linear combinations of a and b. We will go over sets in more detail when we do Combinatorics and when we do Functions in Algebra. For now, a set is simply a collection of things, in this case a collection of numbers that satisfy a particular criteria. We are given a fixed value of a, say 100 and a fixed value of b, say 120. Now, let’s try to find all numbers which can be expressed as a linear combination of 100 and 120. This means let’s take any value for x and any value for y and calculate \\(100\cdot x + 120\cdot y\\). Add this new number to the set of linear combinations.

It is good to do this systematically, as systematically as we can.

{{< table "header-bold-table" >}}
| x | y | 100.x + 120.y |
| :-- | :-- | :-- |
| 1, 2, 3, ... | 0 | 100, 200, 300, ... |
| 1, 2, 3, ... | 1 | 220, 320, 420, ... |
| 1, 2, 3, ... | 2 | 340, 440, 540, ... |
| 1, 2, 3, ... | -1 | -20, 80, 180, ... |
| 1, 2, 3, ... | -2 | -140, -40, 60, ... |
| 0 | 1, 2, 3, ... | 120, 240, 360, ... |
| 1 | 1, 2, 3, ... | 220, 340, 460, ... |
| -1 | 1, 2, 3, ... | 20, 120, 220, ... |
| ... | ... | ... |
{{< /table >}}

Note that there are infinitely many values we can assign to x and y and in the process, and each time we can a new value for \\(a\cdot x + b\cdot y\\). In other words, the set of linear combinations of a and b has infinitely many numbers.

### Divisors, Multiples and Linear combinations

Lets look at these sets as a Venn diagram more carefully, say for the numbers 45 and 60.

The divisors of 45 are listed below, note that this is a finite set with exactly 6 numbers in it.

{{< table "compact-table" "bg-light-red-1" >}}
| Divisors of 45 | 1 | 3 | 5 | 9 | 15 | 45 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
{{< /table >}}

The set of multiples of 45 are shown below, i.e. numbers of the form 45.n, where n ≥ 1. Note that this is an infinite set. 

{{< table "compact-table" "bg-light-blue-1" >}}
| Multiples of 45 | 45 | 90 | 135 | 180 | 225 | 270 | 315 | 360 | ... | ... |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
{{< /table >}}

Notice that the only common element between these sets is the original number itself, 45.
{{< table "compact-table" "bg-light-blue-1" "bg-light-red-1">}}
|  |  |  |  |  |  | 45 | 90 | 135 | 180 | 225 | 270 | 315 | 360 | ... | ... | Multiples of 45 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| Divisors of 45 | 1 | 3 | 5 | 9 | 15 | 45 |  |  |  |  |  |  |  |  |  |  |
{{< /table >}}

We can repeat the same process as above for the number 60, to get the following:
{{< table "compact-table" "bg-light-red-2" >}}
| Divisors of 60 | 1 | 2 | 3 | 4 | 5 | 6 | 10 | 12 | 15 | 20 | 30 | 60 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
{{< /table >}}

The finite set of divisors above, the infinite set of multiples below,
{{< table "compact-table" "bg-light-blue-2" >}}
| Multiples of 60 | 60 | 120 | 180 | 240 | 300 | 360 | ... | ... |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
{{< /table >}}

and the intersection of these two sets being the original number, 60.
{{< table "compact-table" "bg-light-blue-2" "bg-light-red-2" >}}
|  |  |  |  |  |  |  |  |  |  |  |  | 60 | 120 | 180 | 240 | 300 | 360 | ... | ... | Multiples of 60 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| Divisors of 60 | 1 | 2 | 3 | 4 | 5 | 6 | 10 | 12 | 15 | 20 | 30 | 60 |  |  |  |  |  |  |  |  |
{{< /table >}}

Next, lets look at common divisors of 45 and 60, just like we did for 100 and 120 earlier.

{{< table "compact-table" "bg-light-red-1" "bg-light-red-2" >}}
| Divisors of 45 | 1 |  | 3 |  | 5 |  | 9 |  |  | 15 |  |  | 45 |  |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| <span class="bg-light-yellow-1">Common Divisors of 45 and 60</span> | <span class="bg-light-yellow-1">1</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">3</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">5</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1 ba pa2">15</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">.</span> | <span class="bg-light-yellow-1">.</span> |
| Divisors of 60 | 1 | 2 | 3 | 4 | 5 | 6 |  | 10 | 12 | 15 | 20 | 30 |  | 60 |
{{< /table >}}

The greatest of the common divisors, or the GCD as we know well, is highlighted above.

The Venn diagrams for the common multiples of 45 and 60 can be similarly done.
{{< table "compact-table" "bg-light-blue-1" "bg-light-blue-2" >}}
| Multiples of 45 | 45 |  | 90 |  | 135 | 180 | 225 |  | 270 |  | 315 | 360 | ... | ... |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| <span class="bg-light-green-2">Common multiples of 45 and 60</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2 ba pa2">180</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">360</span> | <span class="bg-light-green-2">.</span> | <span class="bg-light-green-2">...</span> |
| Multiples of 60 |  | 60 |  | 120 |  | 180 |  | 240 |  | 300 |  | 360 | ... | ... |
{{< /table >}}

And the least of the common multiples, or the LCM that may be already familiar but will encounter more in the next sessions, is highlighted above.

Finally, lets look at the set of linear combinations of 45 and 60, i.e. all numbers of the form \\(45\cdot x + 60\cdot y\\). We can restrict ourselves to positive numbers alone, x or y can either be negative but we will only consider the combination number, \\(45\cdot x + 60\cdot y\\), when it is positive (the picture for negative numbers is just a mirror image, and we can ignore that for now). 

Lets notice the interesting properties of this set and its elements:

- Firstly, the set is an infinite set, i.e. it has an infinite number of elements.
- The set includes *all* multiples of 45, got by putting y = 0 in the linear combination.
- The set likewise includes *all* multiples of 60, by putting x = 0.
- It also includes additional numbers such as say 150:
  - which is neither a multiple of 45, nor a multiple of 60,
  - but is a linear combination, \\( 150 = 270 - 120 = 45.6 + 60.(-2) \\)
- Interestingly, it also includes a select few divisors of 45 and of 60:
  - For eg, it includes 30, which is a linear combination of 45 and 60,
  - it can be written as, \\(30 = 90 - 60 = 45.2 + 60.(-1)\\),
  - or even as, \\(30 = -90 + 120 = 45.(-2) + 60.2\\).
- Crucially though, and most interestingly, the set of linear combinations of 45 and 60 also includes one of the common divisors of 45 and 60, *exactly one common divisor*, and no points for guessing even though it is a most startling revelation, it includes the greatest of the common divisors, the GCD. 
  - \\(15 = -45 + 60, or\\)
  - \\(15 = 45.3 + 60.(-2)\\)

These different sets are depicted below (a little squashed up, but hopefully still clear from the colors), note that the linear combinations set is repeated at the top and bottom just for clarity of comparing the sets.

{{< figure src="images/45-60-divisors-multiples-comaprison.png" class="figs" title="A picture to aid the counting of the kittens" >}}

We already know that the GCD of a and b is a divisor of a and a divisor of b, by definition. What we are seeing is that the GCD is the only common divisor which can also be expressed as a linear combination of a and b. The GCD is also the smallest positive element in the set of linear combinations of a and b. In fact, all linear combinations of a and b are multiples of the GCD and vice versa, any multiple of the GCD can be written as a linear combination of a and b. We also find that all the common divisors of a and b divide the GCD. 

All of these are very interesting results, and do take some time to mull over these, say with examples.

This Venn diagram is depicted below, and we have found something almost magical - the GCD is at the very center of this gorgeous 😎 Venn Diagram!!

{{< figure src="images/Divisors-Multiples-and-Linear-Combinations.png" class="figs" title="" >}}

Take a moment to take all of that in. We can draw similar Venn diagrams for other pairs of numbers. Try for eg, 80 and 180.

### Division Algorithm

We are now well on our way to unraveling how the simple approach to finding the largest tile that we encountered earlier works. Before we do that, we need to add one more theorem or algorithm to our understanding. We must know this from our childhood, and we will not prove this one right now. But it is important to note what the claim is.

{{< theorem-block "Theorem" "Proof" >}}
Given two integers \\(a\\) and \\(b\\), \\(\exists \\) unique integers \\(q\\) and \\(r\\), such that   
\\( a = q\cdot b + r\\) and \\(0 \leq r < b\\)
<--->
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

Hence proved.

{{< /theorem-block >}}

We will leave the space here to come back to the proof later. The main thing to prove is that if r is smaller than b, then q and r are both unique. This is fundamental. But we have known this from childhood, we may not have known that q and r are unique, we probably always knew that r was smaller than b, but we do know that we call q the quotient and r the remainder. Further, if r is 0, then b divides a, and vice versa, if r is not zero, then b does not divide a.

### Unique property of GCD

{{< theorem-block "Theorem" "Proof" >}}
The least positive integer of the set of linear combinations of a and b is the GCD of a and b.
<--->

Suppose m is the least positive integer in the set of linear combinations of a and b. Recall that all linear combinations are of the form \\(a\cdot x + b\cdot y\\). Since m is also a linear combination of a and b
$$ m = a\cdot x_0 + b\cdot y_0, \text{ for some } x_0 \text{ and } y_0$$

We are now going to show that \\(m | a\\) and \\(m | b\\). Suppose \\(m \cancel{|} a\\).  
Then, by Division algorithm, \\( \exists q\\) and \\(r\\) s/t  

{{< katex >}}
\begin{array}{rcl}
a & = & m\cdot q + r \text{ and } 0 < r < m \\
r & = & a - m\cdot q \\
  & = & a - (a\cdot x_0 + b\cdot y_0)\cdot q \\
  & = & a - a\cdot x_0\cdot q - b\cdot y_0\cdot q \\
  & = & a\cdot (1 - x_0\cdot q) + b\cdot (-y_0\cdot q) \\
  & = & a\cdot x_1 + b\cdot y_1
\end{array}
{{< /katex >}}

But that means that \\(r\\) is also a linear combination of \\(a\\) and \\(b\\). However \\(r < m\\), but we started saying \\(m\\) is the smallest linear combination. So, our assumption that \\(m  \cancel{|} a\\) must be wrong. Hence \\(m | a\\). Similarly, we can prove that \\(m | b\\). So, \\(m\\) is a common divisor of \\(a\\) and \\(b\\).

We already know that all divisors of \\(a\\) and \\(b\\) also divide \\(a\cdot x + b\cdot y\\) and therefore in particular also divide \\(m\\), i.e.
{{< katex >}}
\text{If } c | a \text{ and } c | b, \text{ then } c | m
{{< /katex >}}

So, \\( c \leq m\\), \\(\forall c\\)

Thus we have that m is a common divisor of a and b and is also the greatest common divisor.

Hence proved.

{{< /theorem-block >}}

The method of this proof is called proof by contradiction. We start with an assumption, arrive at a contradiction and hence infer that the assumption has to be wrong.

### Back to the tiles

Let’s go back to the tiling exercise and see how all of this relates to what we were originally doing - finding the largest size tile that fits the room.

If we observe carefully, we will notice that the process of finding the largest tile for the room is the same as the process of searching for the smallest positive integer in the set of linear combinations!!

{{< figure src="images/tiles-and-linear-combinations.png" class="figs" title="" >}}

In the above picture:

1. We start with 3645 and 2115. 
1. In discarding the square of size 2115 x 2115, we are making the first linear combination that is 1.3645 - 1.2115 = 1530
1. In discarding the next square of 1530 x 1530 from the 2115 x 1530 part of the room, we are again making a linear combination 1.2115 - 1.1530 = 1.2115 - 1.(1.3645 - 1.2115) = -1.3645 + 2.2115 = 585
1. And so on.

It should be clear from the above that we are searching the set of linear combinations for small numbers. But we have to prove that it converges to the smallest number, the GCD.

## Euclid's Algorithm for GCD

This is the famous Euclid’s algorithm for finding the GCD of two numbers a and b. We will assume \\(a \geq b > 0\\).

We first divide \\(a\\) by \\(b\\) yielding remainder \\(r_1\\).

{{< columns >}}

<--->

{{< katex >}}
\begin{array}{rcl}
a & = & q_1\cdot b + r_1 \\
\end{array}
{{< /katex >}}

<--->

{{< katex >}}
\begin{array}{l}
0 < r_1 < b \\
\end{array}
{{< /katex >}}

{{< /columns >}}

If \\(r_1\\) is \\(0\\), then the GCD is \\(b\\). But suppose \\(r_1\\) is not zero, then we divide \\(b\\) by \\(r_1\\) to yield \\(r_2\\), and then \\(r_1\\) by \\(r_2\\) and so on, until we get a zero remainder.

{{< columns >}}

<--->

{{< katex >}}
\begin{array}{rcl}
b & = & q_2\cdot r_1 + r_2 \\
r_1 & = & q_3\cdot r_2 + r_3 \\
\vdots \\
r_{n - 2} & = & q_n\cdot r_{n - 1} + r_n \\
r_{n - 1} & = & q_{n + 1}\cdot r_n + 0 \\
\end{array}
{{< /katex >}}

<--->

{{< katex >}}
\begin{array}{l}
0 < r_2 < r_1 \\
0 < r_3 < r_2 \\
\vdots \\
0 < r_n < r_{n - 1} \\
\end{array}
{{< /katex >}}

{{< /columns >}}

Note that we are guaranteed to get a remainder of 0 after some number of steps, because at each step the remainder is strictly decreasing, i.e. \\( b > r1 > r2 > r3 > \cdots \geq 0\\).

{{< theorem-block "Theorem" "Proof" >}}

\\(r_n\\) above is the GCD of \\(a\\) and \\(b\\).
<--->

First lets prove the following:  
If \\(a = q\cdot b + r\\), then \\((a, b) = (b, r)\\)  

Suppose \\(g = (a, b) \\)  
\\( \therefore g | a \\) and \\( g | b \\)  
\\( \therefore g | (a\cdot x + b\cdot y) \\)  
In particular, \\( g | (a\cdot 1 + b\cdot (-q)) \\), i.e. \\( g | (a - q\cdot b) \\)  
\\( \therefore g | r \\)  

Now suppose \\( c | b \\) and \\( c | r \\)
\\( \therefore c | (b\cdot x + r\cdot y) \\)  
In particular, \\( c | (b\cdot q + r\cdot 1) \\), i.e. \\( c | (q\cdot b + r) \\)  
\\( \therefore c | a \\)  
\\( \therefore c \leq g \\)  

\\( \therefore g = (a, b) = (b, r) \\)  

{{< katex >}} \therefore (a, b) = (b, r_1) = (r_1, r_2) = \cdots = (r_{n-1}, r_n) = (r_n, 0) = r_n {{< /katex >}}

Hence proved.

{{< /theorem-block >}}

And that completes our magic trick!! 😎😎😎

