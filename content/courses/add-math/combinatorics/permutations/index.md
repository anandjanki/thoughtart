---
title: "Permutations"
date: 2020-01-18T19:38:34+05:30
draft: false
weight: 4
---

We have had a glimpse of counting problems, and looked at two fundamental principles of counting - namely the product rule and the sum rule. Then we looked at the notion of factorials and how they come about naturally when we try to arrange n things in n places. We now take next steps in exploring more kinds of counting problems. This session on Permutations and the next one on Combinations are the basic kinds of counting problems commonly studied.

## Arranging r-items out of n

### The top 2 teams

Suppose there were 5 houses in the school, let's recap how many ways in which the houses can be placed at the end of the championship? We know now that is 5! = 5 x 4 x 3 x 2 x 1 = 120 ways.

Suppose, we were interested only in the first place and the second place teams. So, lets say the question was - with the 5 houses, what are the ways in which the championship first place and second place can be determined?

For this, consider the following 6 possibilities (out of the total of 120) for the results of the championship. In each of these 6 possibilities, team A stands first, and team B second.

{{< columns >}}

    A  B  C  D  E
    A  B  C  E  D
    A  B  D  C  E
    A  B  D  E  C
    A  B  E  C  D
    A  B  E  D  C

<--->

<---> 

{{< /columns >}}

Since we are only looking for the number of ways for the first and the second place, all these 6 possibilities can be collapsed into 1 single possibility for the first and second place - namely `A  B`. Similarly if we take some other possibility for the first and second place, say we take `E  B`, then again, amongst the 120 possibilities for all 5 teams, we will find 6 which have `E  B` in the first and second place. These are listed below:

{{< columns >}}

    E  B  A  C  D
    E  B  A  D  C
    E  B  C  A  D
    E  B  C  D  A
    E  B  D  A  C
    E  B  D  C  A

<--->

<---> 

{{< /columns >}}

The reason there are 6 of these is because, with the first and second place fixed at `E  B`, there are 3! ways in which 3 teams can show up in 3 places (the third, fourth and fifth places).

In other words, if we take all the 120 possibilities of the end result for all 5 teams, we can make separate sets such that within each set, the first and the second place is the same. The only difference is which team was placed third, fourth and fifth.

Now, lets recall the question we were answering - how many ways in which we can have the top two positions at the end of the Championship filled? Since we have separated all the 120 possiblities above, such that each set gives us one possibility of the top two positions, and since the number of possiblities within each set is 6, hence the number of ways in which the top two positions can be filled is 120 / 6 = 20. 

More generically, in a championship with 5 teams, the number of ways in which the top two positions can be filled is \\( \displaystyle \frac{5!}{3!} \\). In order to complete the calculation:

{{< katex >}}

\begin{array}{rcl}
\displaystyle \frac{5!}{3!} & = & \displaystyle \frac{5\cdot 4\cdot 3\cdot 2\cdot 1}{3\cdot 2\cdot 1} \\ \\
& = & 5\cdot 4 \\
& = & 20
\end{array}

{{< /katex >}}

Another way to arrive at this answer is as follows - there are 5 teams that can occupy the first position, once we have a team in the first position, one of the remaining 4 teams can occupy the second position. In other words, number of ways in which the first position can be filled is 5, and the number of ways in which the second position can be filled is 4. Hence, applying the product rule, the number of ways the first two positions can be filled by 5 teams is 5 x 4 = 20 ways.

### 100m dash with 10 students

Similarly, if a 100m dash had 10 students participating, and we were interested in the top three positions, the number of ways in which the top 3 positions can be filled is \\( \displaystyle \frac{10!}{7!} \\). The total number of possibilities for all 10 positions is 10!, but we are not interested in the last 7 positions, we are only interested in the top 3. For a given standing of the top-3 students (say `Student-E  Student-B  Student-F` for example), the remaining 7 students occupy the remaining 7 positions in 7! ways, but we are not interested in them. Hence the answer we got above. 

This is called \\( {^{10}}P_3 \\).

### nPr

The number of different ordered arrangements of \\( r \\) items taken from \\( n \\) distinct items is given by:
$$ {^n}P_r = \frac{n!}{(n - r)!} $$

To revisit the couple of problems above: 

The number of different ordered arrangements of 2 teams taken from 5 distinct teams (that is same as the number of ways in which the top-2 positions can be filled from amongst 5 teams) is given by:
$$ {^5}P_{2} = \frac{5!}{(5 - 2)!} = \frac{5!}{3!} = 5\cdot 4 = 20$$

The number of different ordered arrangements of 3 students taken from 10 distinct students (that is the same as the number of ways in which the top-3 positions can be filled from amongst 10 students) is given by:
$$ {^{10}}P_{3} = \frac{10!}{(10 - 3)!} = \frac{10!}{7!} = 10\cdot 9\cdot 8 = 720$$

### Power of the password

Here is another question - how many distinct 8-character passwords can you make from 26 lower case alphabets, 26 upper case ones, 10 digits, and say 10 symbols?

The total number of distinct characters is 26 + 26 + 10 + 10 = 72. The number of 8-character passwords we can make from these is:
$$ {^{72}}P_{8} = \frac{72!}{(72 - 8)!} = \frac{72!}{64!} $$
You can use a calculator or program to check that this value is approximately **500 trillion possible passwords** (the exact number is 482,590,739,030,400).

On the other hand, suppose you had only put in a 3-character password for your acccount. How many different 3-character passwords can be made? That can be calculated as:
$$ {^{72}}P_{3} = \frac{72!}{(72 - 3)!} = \frac{72!}{69!} $$
That comes out to be 357,840. A human intruder may not be able to go through so many different attempts to crack your password, but a modern day computer can easily churn through these to identify your password. 

If however, your password was 8-character long, it would take even a modern day computer days on end to figure out the password.

Now it should be clear why, longer the password, the harder it is to crack it.

{{< TODO >}}

## Practice Problems

{{< tabs "PER-1" >}}
{{< tab "Problem" >}}
TBD
{{< /tab >}}

{{< tab "Hint" >}}
TBD
{{< /tab >}}

{{< tab "Solution" >}}
TBD
{{< /tab >}}

{{< /tabs >}}

{{< /TODO >}}
