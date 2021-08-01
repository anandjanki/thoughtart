---
title: "Combinations"
date: 2020-01-18T19:38:40+05:30
draft: false
weight: 5
---

In this session, we are interested in a slightly different class of counting problems, where the order of the items does not matter. 

## Choosing without order

### Student Volunteers

Suppose, we have 5 students with us, and we want 2 volunteers from these 5 students in order to do something. How many ways in which we can have 2 volunteers from these 5 students?

Note the key difference compared to the other kind of problem we have looked at - suppose 5 students were running a race, and we were interested in how many was can the top-2 positions be filled? In this case, the order of the top-2 arrangement matters. But if we only want 2 volunteers, then *the order of the students doesnt matter*. We are only interested in the group of 2 volunteers.

The number of ways for the top-2 positions to be filled by 5 students is 5 x 4 = 20 ways. One of these ways would be `A  B`, with `A` in the first place and `B` in the second. A different way would be `B  A`, with `B` in the firsst place and `A` in the second. 

But if we were taking 2 student volunteers, then `A  B` and `B  A` are the same. Hence the number of ways of having 2 volunteers from 5 students is 20 / 2 = 10 ways.

### Quick Recap

Let's once recap the different kinds of counting problems we have looked at so far.

**Q1.** A combination lock has a 3-digit code, each digit can be set using one of the 10 digits from 0 - 10, digits can be repeated. How many different codes are possible?

**Ans.** The number of ways in which a 3-digit code can be set is 10 x 10 x 10 = \\( 10^3 \\) or 1,000 ways.

---

**Q2.** There are 10 students in a class, and they are queuing up for lunch. How many different ways in which the queue can be formed?

**Ans.** The number of ways in which the queue can be formed is \\( 10! \\) ways. That is 3,628,800 ways. 

---

**Q3.** 10 students are running the 100m dash. How many ways are there for the top-3 standings from the race?

**Ans.** The number of ways in which the top-3 positions can be won by 10 students is \\( {^{10}}P_{3} \\) = 10 x 9 x 8 = 720 ways.

---

**Q4.** 10 students are available, and we need 3 volunteers out of these. How many ways can we have a 3-member volunteer group from 10 students?

**Ans.** The number of ways in which 3 volunteers can be chosen from 10 students is \\( {^{10}}C_{3} \\) = 10 x 9 x 8 / 6 = 120 ways.

---

The reason we divided by 6 in the answer to the last question above is because within the 3 students, order does not matter. So the 3! ways in which 3 students can be arranged within themselves can all be considered as a single group of volunteers.

### nCr

The number of ways of choosing \\( r \\) items from a set of \\( n \\) distinct items, where the order of the selection does not matter, is given by:
$$ {^n}C_{r} = \frac{{^n}P_r}{r!} $$

nCr is often read as n-choose-r and also denoted by this alternate symbol below and expanded using the formula for nPr:
$$ {n\choose r} = \frac{n!}{r!\cdot (n - r)!} $$

## More Examples

### Making a fruit salad

Suppose there are 10 kinds of fruits at a shop, how many ways are there to buy 4 kinds of fruits to make a fruit salad?

The answer is simply \\( {^{10}}C_4 \\), but lets also do the calculation below to arrive at the final answer:

{{< katex >}}
\begin{array}{rcl}
\displaystyle {10\choose 4} & = & \displaystyle \frac{10!}{4!\cdot 6!} \\ \\
& = & \displaystyle \frac{10\cdot 9\cdot \cancel{8}\cdot 7\cdot \cancel{6!}}{{\cancel{4}\cdot 3\cdot \cancel{2}\cdot 1}\cdot \cancel{6!}} \\ \\
& = & 10\cdot 3\cdot 7 \\
& = & 210
\end{array}
{{< /katex >}}

Note that the order of selection of 4 kinds of fruits does not matter.

### Hands with 5 cards

From a 52-card deck, we pick 5 cards. How many such hands are possible?

The total number of hands is \\( \displaystyle {52\choose 5} = \displaystyle \frac{52!}{5!\cdot 47!} \\). This number turns out to be 2,598,960 hands or about two-and-a-half Million hands in all.

Note again that the order of cards in the hand does not matter.

### Choosing friends

It is always hard if one has to choose from between friends, but suppose you have only 5 tickets for a movie. How many ways are there to choose 5 friends from your class of say 20 friends?

The number of ways to choose 5 friends from amongst 20 friends is:

{{< katex >}}
\begin{array}{rcl}
\displaystyle {20\choose 5} & = & \displaystyle \frac{20!}{5!\cdot 15!} \\ \\
& = & \displaystyle \frac{\cancel{20}\cdot 19\cdot 18\cdot 17\cdot 16\cdot \cancel{15!}}{{\cancel{5}\cdot \cancel{4}\cdot 3\cdot 2\cdot 1}\cdot \cancel{15!}} \\ \\
& = & 19\cdot 3\cdot 17\cdot 16 \\
& = & 15,504
\end{array}
{{< /katex >}}

Now suppose, there was only 1 ticket, how many ways are there for you to choose from your 20 friends for the movie? This can be done in 
$$ \displaystyle {20\choose 1} = \displaystyle \frac{20!}{1!\cdot 19!} $$ 
or 20 ways. That should be obvious, if you had only 1 ticket to take a friend, then you can choose one of your 20 friends, there are 20 ways to do that. 

Now suppose, you had 19 tickets. How many ways are there for you to choose 19 friends from among your 20 friends for the movie? This can be done in
$$ \displaystyle {20\choose 19} = \displaystyle \frac{20!}{19!\cdot 1!} $$ 
or 20 ways only. Is that intuitive, or did you expect a much bigger number? If we think about this a little, we can see that if we have to choose 19 friends from amongst 20 to give the tickets to, that is the same as choosing 1 friend amongst 20 to *not* give the ticket to. We have already seen that choosing 1 friend from 20 friends can be done in \\( {^{20}}C_1 = 20 \\) ways, so choosing 19 friends from 20 friends can also be done in 20 ways.

### Make your own

Combination problems also come up all the time in our daily life. Here are a few:

- You are about to color a picture, say a mandala, and want to choose 3 colors from a set of 12 crayons. How many ways are there to do this?
- You are answering a question paper with 12 questions, out of which 2 are optional, so you need to choose any 10 questions out of the 12. How many ways are there to do this?
Can you think of a few instances where it may have come up for you.


## Some nCr properties

- Symmetry -
As we saw in the previous example, and as it should be obvious from the formula, there is a nice symmetry property to nCr:
$$ {n\choose r} = {n\choose n-r} $$

- n-choose-1 - 
Again, as seen previously:
$$ {n\choose 1} = {n\choose n-1} = n $$

- n-choose-n -
How many ways are there to choose n items from n items? Clearly, there is only 1 way. Given that, we would also like to say that there is 1 way to choose 0 items from n items. So:
$$ {n\choose 0} = {n\choose n} = 1 $$

- 0! - 
For the sake of convenience, for eg, to ensure that the formula for nCn also evaluates to 1, we define:
$$ 0! \equiv 1 $$

{{< TODO >}}

## Practice Problems

{{< tabs "COM-1" >}}
{{< tab "Problem" >}}
TBD - Combinations with sum rule
{{< /tab >}}

{{< tab "Hint" >}}
TBD
{{< /tab >}}

{{< tab "Solution" >}}
TBD
{{< /tab >}}

{{< /tabs >}}


{{< tabs "COM-2" >}}
{{< tab "Problem" >}}
TBD - Combinations with product rule
{{< /tab >}}

{{< tab "Hint" >}}
TBD
{{< /tab >}}

{{< tab "Solution" >}}
TBD
{{< /tab >}}

{{< /tabs >}}



{{< tabs "COM-3" >}}
{{< tab "Problem" >}}
TBD - Combinations with both sum and product rule
{{< /tab >}}

{{< tab "Hint" >}}
TBD
{{< /tab >}}

{{< tab "Solution" >}}
TBD
{{< /tab >}}

{{< /tabs >}}

{{< /TODO >}}

