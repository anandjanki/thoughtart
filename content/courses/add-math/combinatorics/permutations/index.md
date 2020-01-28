---
title: "Permutations"
date: 2020-01-18T19:38:34+05:30
draft: false
weight: 4
---

We have had a glimpse of counting problems, and looked at two fundamental principles of counting - namely the product rule and the sum rule. We now take next steps in exploring more kinds of counting problems. This session on Permutations and the next one on Combinations are the basic kinds of counting problems commonly studied.

## Arrangements of n-items

### School Championship

Suppose you have 3 houses in your school for the Sports Championship. Let's say they are named by colors, say Purple, Orange and Green. What are the different ways in which the houses may be placed at the end of the Sports Championship?

We just enumerate out the possibilities, aiming to do so systematically:

| 1st Place | 2nd Place | 3rd Place |
|  :---:    |  :---:    |  :---:    |
| Purple    | Orange    | Green     |
| Purple    | Green     | Orange    |
| Orange    | Purple    | Green     |
| Orange    | Green     | Purple    |
| Green     | Purple    | Orange    |
| Green     | Orange    | Purple    |

As before, for ease of writing and counting, lets call the teams A, B and C. The possibilities are written out again below (we will assume ties are not allowed):

{{< columns >}}

    A    B    C
    A    C    B
    --
    B    A    C
    B    C    A
    --
    C    A    B
    C    B    A

<--->

<--->

{{< /columns >}}

We wrote it in the particular way above, so that it is also easy to read.

- Suppose team A comes first. 
  - It is possible team B may come second, and team C may be third. Or,
  - It is possible that team C may come second and team B may come third.
- Suppose team B comes first. 
  - It is possible team A comes second, and team C may be third. Or,
  - It is possible that team C may be placed second and team A may come third.
- Suppose team C comes first. 
  - second place to A, third to B, or
  - second place to B, third to A.

By applying the principles of counting without repetition we learnt earlier, and using the product rule, we can conclude that there are 3 x 2 x 1 = 6 ways in which the school results can turn out to be.

### Factorial shows up

You may have noted that the result above seemed to look like a factorial. But is that just incidental to this problem or more fundamental to counting problems of these kinds?

In order to see that, lets consider the following situation. Suppose there is a fourth house now, and we want to knwo what are the possible championship results. Do we have to work out all the possibilities from scratch like we did above? Or can we intelligently use the possibilities we found with 3 teams? It turns out that is possible.

Lets call this new team, team D. Suppose this team comes first. What are the possibilities of the end results? D is in first place, and for the ways in which the remaining 3 teams can be placed, we can reuse what we had done before with the 3 teams. This is depicted below:

{{< columns >}}

    D    A    B    C
    D    A    C    B
    D    B    A    C
    D    B    C    A
    D    C    A    B
    D    C    B    A

<--->

<--->

{{< /columns >}}

That is really cool, because we dont need to do the hard work of writing out all the possibilities for 3 teams again, and simply reuse what we had done before.

Now, it is possible team D may come last, i.e. be placed fourth. It is also possible that team D may come second, or come third. How do we account for these possibilities.

{{< columns >}}

         A    B    C
         A    C    B
         B    A    C
         B    C    A
         C    A    B
         C    B    A
      ^D   ^D   ^D   ^D

<--->

<--->

{{< /columns >}}

As shown above, we can take all the possiblities with 3 teams and come up with new possibilites when the fourth team joins the fray, by simply considering *the 4 new possibilities for each of the possibilities with 3 teams*. This is shown below compactly.

{{< columns >}}

    D  A B C
    D  A C B
    D  B A C
    D  B C A
    D  C A B
    D  C B A

<--->

    A  D  B C
    A  D  C B
    B  D  A C
    B  D  C A
    C  D  A B
    C  D  B A

<--->

    _ _  D  _
    _ _  D  _
    _ _  D  _
    _ _  D  _
    _ _  D  _
    _ _  D  _

<--->

    A B C  D
    A C B  D
    B A C  D
    B C A  D
    C A B  D
    C B A  D

{{< /columns >}}

One set of possiblities above (with team D in the third position) is left blank for you to practice.

What is happening is that the number of results possible with 4 teams is turning out to be 4 times the number of results possible with 3 teams. If we call the number of results with 4 teams as \\(R(4)\\) and the number of results with 3 teams as \\(R(3)\\), then this statement can be represented mathematically as follows:

$$ R(4) = 4\cdot R(3) $$

And we can now do a *recursive* calculation to find \\(R(4)\\).

{{< katex >}}

\begin{array}{rclcl}
R(1) & = & 1 \\
R(2) & = & 2\cdot R(1) & = & 2\cdot 1 \\
R(3) & = & 3\cdot R(2) & = & 3\cdot 2\cdot 1 \\
R(4) & = & 4\cdot R(3) & = & 4\cdot 3\cdot 2\cdot 1 \\ \\
\therefore R(4) & = & 4!
\end{array}

{{< /katex >}}

In other words, what we have found is that if there are \\(n\\) teams participating in a championship, then the number of ways in which the teams can be placed in \\(n\\) positions at the end of the championship is \\(n!\\) ways.

### Group photo

Lets look at another example. Suppose there are 6 friends. How many different ways can they pose for a photograph (standing in a straight line facing a camera)?

{{< figure src="friends-cast-v3.jpg" height="200px" class="figs" title="6 \"friends\" posing for a group photo" >}}

We know now from the previous section that this can be done in 6! ways.

Another way to go about this is the following:

- The first position (the leftmost spot) can be taken up any one of the 6 friends. And,
- Once that is done, the second position can now be taken by any of the remaining 5 friends. And,
- Once that is done, the third position can now be taken up any of the remaining 4 friends. And,
- Once that is done, the fourth position can now be taken up any of the remaining 3 friends. And,
- Once that is done, the fifth position can now be taken up any of the remaining 2 friends. And,
- Once that is done, the sixth and last position can now be taken by the remaining 1 friend.

So, the number of ways of posing for the group photograph is 6 x 5 x 4 x 3 x 2 x 1 = 6! = 720 ways.

### Queueing up

Let's take one more example. Suppose there are 20 children in your class, its lunch time, and every one is queueing up for picking up their lunch. How many different ways can the class queue up for lunch? 

Can you try out all possible ways to queue up in one lunch session?

Well, the total number of ways as we now know is 20! ways.

That is a very large number as we saw in the [last session]({{< ref "factorial/#factorials-are-large" >}}), that is - 2,432,902,008,176,640,000 - or about 2.5Quntillion ways with a small class of just 20.

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
