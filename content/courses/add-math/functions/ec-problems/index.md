---
title: "EC Problems"
date: 2020-03-11T20:50:42+05:30
draft: true
weight: 4
---

EC problems may not always be easy problems. They are actually *extra-curricular* problems.. :) They usually add some interesting facets to the topic under discussion, some fascinating discoveries, etc. But they are usually not from the board syllabus for the topic. (As always, once you read a problem, take some time to attempt it yourself, if you need help, take a peek at the "Hint" section, then again attempt to solve it yourself, feel free to check the "Answer" section if you want to check the answer you found, or even just get a feel for the magnitude of the answer.)

## Thinking complements
We briefly encountered this in the topic on choosing friends. Lets look at one more example.

**Q.** How many 6-digit numbers have at least one even digit in them?

{{< expand "Hint" >}}
One way to do this is to of course list out all the possibilities for even digits, and count the number of 6-digit numbers with exactly 1 even digit, the number of 6-digit numbers with exactly 2 even digits, and so on. 

Do take a moment to try one of these, for example, what is the total number of 6-digit numbers with exactly 1 even digit. This may be OK, but if you also try to do the next one and try to find the total number of 6-digit numbers with exactly 2 even digits, you may find that a little hard to do. You may soon realize that it is quite cumbersome and lengthy to calculate all the possibilities like that and add all of them up.

The alternative intelligent way is to calculate the number of ways of the complement happening. Find out how many 6-digit numbers are there without any even digits. Then subtract this from the total number of 6-digit numbers. Those are all the numbers with at least one even digit.
{{< /expand >}}

{{< expand "Solution" "..." >}}

The number of 6-digit numbers *without* any even digits can be easily found. 

There are 5 odd-digits, namely 1, 3, 5, 7, and 9. There are 6 places to fill and repetition is allowed. The number of such numbers is simply \\( 5^6 \\).

The total number of 6-digit numbers are \\( 9\cdot 10^5 \\) or 900,000 in all (these are all the numbers from 100,000 to 999,999).

Hence, the number of 6-digit numbers with at least one even digit is \\( 9\cdot 10^5 - 5^6 \\) or 884,375 in all.

{{< /expand >}}

{{< expand "Answer" >}}
884,375
{{< /expand >}}

## Sitting around and dining

We earlier calculated the number of ways in which 6 people can stand in a straight line and pose for a photograph. That is similar to sitting at a long straight dining table. The question we now ask is:

**Q.** How many ways are there for 6 people to sit around a circular dining table (where there is no special chair, all the seats are the same)?

{{< expand "Hint" >}}
Circular arrangements have a little peculiarity as compared to straight line arrangements. Consider two possible straight line arrangements of 6-people in 6-places - for eg, `A B C D E F` and `F A B C D E`. While these are two different straight line arrangements, on a circular table these are exactly the same.

Note that around a circular table, two arrangements are the same if for each of the members at the table, the left neighbor and the right neigbor are the same.

So, the trick is to calculate the number of straight-table arrangements, and then see how many of them collapse into a single round-table arrangement.

{{< /expand >}}

{{< expand "Solution" "..." >}}
We already know that the total number of straight-table arrangement of 6-people in 6-places is \\( 6!\\) or 720 ways.

Consider one such arrangement - say `A B C D E F`. This same arrangement on a round table will be indistinguishable from five other arrangements since there is no special seat at the table. These 6 arrangements are shown below:

    A B C D E F
    F A B C D E
    E F A B C D
    D E F A B C
    C D E F A B
    B C D E F A

These are each obtained by shifting the original arrangement by one to the right (or the left) each time. In other words, we need to divide the number of straight-line arrangements by 6.

Hence, the number of ways are there for 6 people to sit around a circular dining table is \\( \displaystyle \frac{6!}{6} \\)
{{< /expand >}}

{{< expand "Answer" >}}
120
{{< /expand >}}

## Fruits from the shop

We encountered a very simple problem in the session on Combinations. A fruit shop has say 6-kinds of fruits, and you want to buy 4-kinds for making a fruit salad, how many ways to do that? The question we now ask is different:

**Q.** The fruit show still has 6-kinds of fruits, and we have to buy a total of 10 fruits from the shop. How many ways to do this? 

In general, if there are \\( n\\)  kinds of fruits at the shop, we have to buy \\(r\\) fruits in all, where \\( r\\) can be less than, greater than or even equal to \\(n\\), how many different ways are there to do this?

{{< expand "Hint-#1" >}}
This may sound as a trivial problem, but actually needs some creative problem solving. There are various ways to be misled here. 

For example, it is possible to think that there are 10 places and 6 kinds of fruits, each place can be filled in one of 6 ways, hence the total number of ways is \\(6^{10}\\). But that is wrong. That approach works if you have say 6-digits and 10 places to make a number using the 6-digits where repetition is allowed. This is when the order of the digits is important.

The other peculiarity of this problem is that we have not been told how many fruits are there of each kind. If the problem were - there are 10 apples, 20 oranges, 30 bananas, etc, and find the number of ways to make a bag with 3 apples, 5 oranges, etc. that would have been easy, that would be \\( {^{10}}C_{3}\cdot {^{20}}C_5\cdot \cdot \\). But this problem is different.
{{< /expand >}}

{{< expand "Hint-#2" >}}
You should work out the case of 2-kinds of fruits (instead of 6-kinds) and bag of 10-fruits to be filled in all, this one should be fairly easy to do. You can also try to work out the case of 3-kinds of fruits to get a good feel for exactly what we are trying to do here.

Essentially, we are trying to find the number of ways to add up 6 numbers to make 10, one or more of the 6 numbers can be 0, and in this case of fruits, `1 + 1 + 1 + 1 + 2 + 4 = 10` is different from `1 + 1 + 1 + 1 + 4 + 2 = 10`. Suppose the fifth and the sixth fruits were mango and guava, then 2mangoes+4guavas is definitely different from 4mangoes+2guavas.
{{< /expand >}}

{{< expand "Hint-#3" >}}
Try to rephrase the problem in a different manner. 

For the scenario with 3-kinds of fruits, say the furits are apples, oranges and bananas. Suppose we make 12-balls with numbers 1 to 12 written on them. We put them into a bag, close our eyes and then draw 2-balls from the bag. We check the numbers on the balls. Suppose the numbers that come out are 2 and 8, then we take 1 apple, 5 oranges and 4 bananas from the fruit shop. Suppose the numbers that come out are 4 and 5, then we take 3 apples, 0 oranges, and 7 bananas.

See if you can try to work out the case of 6-kinds of fruits similarly. What are the number of ways? And then try to generalize it to n-kinds of fruits and r-fruits to buy. What are the number of ways?
{{< /expand >}}

{{< expand "Solution" "..." >}}
For 6 kinds of fruits to choose 10 fruits from, we make 15 balls with number 1 to 15 written on them, and find the number of ways to choose 5 balls from these 15 balls. Any choice of 5 balls results in a corresponding choice of fruits of 6-kinds such that the total number of fruits is 10.

For the general case, we make \\( (r + n - 1) \\) balls numbered from 1 onwards and choose \\( (n - 1) \\) balls out of these.

{{< TODO >}}
TBD - need to make a picture for this.
{{< /TODO >}}

{{< /expand >}}

{{< expand "Answer" >}}

\\( {^{15}}C_{5} \\)

\\( {^{r + n - 1}}C_{n - 1} \\)

{{< /expand >}}

## Can't correct my own paper

**Q.** Suppose we have 5 students in the class writing an exam, how many ways are there to hand out the papers back to the students for correction, so that no student gets his/her own paper?

{{< expand "Hint" >}}
Suppose the students are `A, B, C, D and E`, and the papers are `PA, PB, PC, PD, and PE`. If we hand back the papers in the order `PB PA PC PD PE` that is not OK, because `C, D and E` have got their own papers. On the other hand, the order `PE PA PB PC PD` is OK, because no one has got their own paper. For simplicity, you may want to say that `B A C D E` is an invalid ordering, and `E A B C D` is a valid ordering for our problem.

So, the problem translates to finding the arrangements where no one gets their own paper from amongst all possible arrangements. These are called *derangements*. 

Can you work out which are valid derangements for 3 students. Then try to work out the valid derangements for 4 students. And try to see a pattern.

{{< /expand >}}

{{< expand "Solution" "..." >}}
The solution for this problem involves arriving at the derangements of 5 students based on the derangements already found for 3 students and 4 students.

Lets take the 5 students `A B C D E`, and lets say we hand the paper of `A`, i.e. `PA` to `B`. Now, we have two choices - either `A` gets `PB` or `A` does not get `PB`:

- We can give the paper of `B`, i.e. `PB` to `A`, and then look at a derangement of the remaining 3 students. In fact, for every possible derangement of 3 students we have a new derangement of 5 students by simply swapping the papers of `A` and `B`. We can repeat this process by swapping the papers of `A` and `C`, then `A` and `D`, and finally `A` and `E`. The number of ways of doing this is `4 x number of derangements of 3 students`.
- The second choice we have is that we take `A, C, D, E` and make a derangement of these 4 students such that A does not get `PB`. The number of ways in which this can be done is equal to the number of derangements of 4 students, because the problem we are solving is the following - 4 students `A C D E` have papers `PB PC PD PE`, and we need to make a derangement such that C, D and E should of course not get their own papers and A should not get `PB`.  Again, we can repeat this process by taking `A` and `C` next, then `A` and `D`, and finally `A` and `E`. The number of ways of doing this is `4 x number of derangements of 4 students`.

These two choices above result in the following *recursive* formula for the number of derangements for 5 students.
$$ D(5) = 4\cdot D(3) + 4\cdot D(4) $$

Or more generally, for any value of `n`, the number of derangements is given by:
$$ D(n) = (n - 1)\cdot (D(n-1) + D(n - 2)) $$

Starting from 0 and 1, we can find the value of \\(D(5)\\):

{{< katex >}}

\begin{array}{rclcl}
D(1) & = & 0 \\
D(2) & = & 1 \\
D(3) & = & (3 - 1)\cdot (D(2) + D(1)) = 2\cdot (1 + 0) = 2 \\
D(4) & = & (4 - 1)\cdot (D(3) + D(2)) = 3\cdot (2 + 1) = 9 \\
\therefore D(5) & = & (5 - 1)\cdot (D(4) + D(3)) = 4\cdot (9 + 2) = 44 \\
\end{array}

{{< /katex >}}


{{< /expand >}}

{{< expand "Answer" >}}
44
{{< /expand >}}


{{< TODO >}}
### Sub-Factorial
### e Magic
{{< /TODO >}}


{{< TODO >}}

{{< expand "Hint" >}}
{{< /expand >}}
{{< expand "Solution" "..." >}}
{{< /expand >}}
{{< expand "Answer" >}}
{{< /expand >}}

{{< /TODO >}}

