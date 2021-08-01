---
title: "Factorial"
date: 2020-01-25T01:26:59+05:30
draft: false
weight: 3
---

The notion of what is called the Factorial of a number, comes up often in counting problems. Before we define factorials, lets get an intuition of where this comes up.

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

From this enumeration of all the possiblities, we see that the number of ways in which the houses may be placed at the end of the school championship is 6.

We could also arrive at this number without enumerating all the possibilities. We would argue as follows:

 - The number of ways in the which the first place can be filled is 3 ways. And,
 - having filled the first place position, there are two houses left, so the second place can be filled in 2 ways. And,
 - having filled the first and second place positions, there is only one house left, so the third place can be filled in just 1 way.
 - By using the product rule, we can conclude that there are 3 x 2 x 1 = 6 ways in which the school results can end up.

### Factorial shows up

Suppose there is a fourth house now, and we want to know what are the possible championship results. Do we have to work out all the possibilities from scratch like we did above? Or can we intelligently use the possibilities we found with 3 teams? It turns out that is possible.

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
\end{array}

{{< /katex >}}

It should not be a surprise how many ways in which the championship can end up if there are 5 teams.
{{< katex >}}

\begin{array}{rclcl}
R(5) & = & 5\cdot R(4) & = & 5\cdot 4\cdot 3\cdot 2\cdot 1 \\ \\
\end{array}

{{< /katex >}}

In general, it can be seen that if there are \\(n\\) teams participating in the championship, then the number of ways in which the teams can be placed in \\(n\\) positions at the end of the championship is:
{{< katex >}}

\begin{array}{rcl}
R(n) & = & n\cdot (n - 1)\cdot \cdots 5\cdot 4\cdot 3\cdot 2\cdot 1 \\ \\
\end{array}

{{< /katex >}}

### Group photo

Lets look at another example. Suppose there are 6 friends. How many different ways can they pose for a photograph (standing in a straight line facing a camera)?

{{< figure src="images/friends-cast-v3.jpg" class="figs" title="6 \"friends\" posing for a group photo" >}}

We know now from the previous section that this can be done in 6! ways.

Another way to go about this is the following:

- The first position (the leftmost spot) can be taken up any one of the 6 friends. And,
- Once that is done, the second position can now be taken by any of the remaining 5 friends. And,
- Once that is done, the third position can now be taken up any of the remaining 4 friends. And,
- Once that is done, the fourth position can now be taken up any of the remaining 3 friends. And,
- Once that is done, the fifth position can now be taken up any of the remaining 2 friends. And,
- Once that is done, the sixth and last position can now be taken by the remaining 1 friend.

So, the number of ways of posing for the group photograph is 6 x 5 x 4 x 3 x 2 x 1 = 6! = 720 ways.

## Factorial definition

As we can see, the number that is coming up repeatedly is this number where you multiple all numbers less than equal to that number. The number 5 x 4 x 3 x 2 x 1 is called the factorial of 5 and is denoted by 5!

In general, for any natural number n, the factorial of the number is defined as follows:
{{< katex >}}
n! \equiv n \cdot (n - 1) \cdot (n - 2) \cdots 2 \cdot 1
{{< /katex >}}

### A property of factorial

It should be easy to note the following property of factorials:

{{< katex >}}

\begin{array}{rcl}
n! & \equiv & n \cdot (n - 1) \cdot (n - 2) \cdots 2 \cdot 1 \\ \\
(n - 1)! & \equiv & (n - 1) \cdot (n - 2) \cdots 2 \cdot 1 \\ \\
\therefore n! & = & n\cdot (n - 1)!
\end{array}

{{< /katex >}}

This is a very important property. What it means is that if we need to find, let's say 10!, then one way is to multiply all numbers from 10, 9, 8, ..., up to 2 and 1. But suppose we already know the value of 9!, then we can simply multiply it by 10 to get the value of 10!.

What it also means is that we can find the value of n! *recursively*. In order to find \\(n!\\), we find \\( (n - 1)! \\), in order to find that we find \\( (n - 2)! \\), and so on. At any point if we know the value of the factorial of any particular number, we backtrack the way we came. We know the value of 1! to be 1 by definition. So, we can backtrack at least from 1!.

For example, lets see how this works for 5!.

     In order to find 5!,  
     we have to find 4! and multiple by 5.  
    
         In order to find 4!,  
         we have to find 3! and multiple by 4.
        
             In order to find 3!,  
             we have to find 2! and multiple by 3.
            
                 In order to find 2!,  
                 we have to find 1! and multiple by 2.
                
                     We know that 1! is 1.
                
                 Now we can find 2!,  
                 2! is simply 2 x 1 = 2
            
             Now we can find 3!,  
             3! is simply 3 x 2 = 6
        
         Now we can find 4!,  
         4! is simply 4 x 6 = 24
    
     Finally, we can find 5!,  
     5! is simply 5 x 24 = 120

We finally arrived at the same answer for 5!, as we could have got by multiplying 5 x 4 x 3 x 2 x 1, but the nice thing about this approach is that in the process we have also found the values of 4!, 3!, and all factorials lesser than the number we start with.

### Queueing up

Let's take one more example. Suppose there are 20 children in your class, its lunch time, and every one is queueing up for picking up their lunch. How many different ways can the class queue up for lunch? 

Can you try out all possible ways to queue up in one lunch session?

Well, the total number of ways as we now know is 20! ways.

It turns out that this is a very large number. It will take many many years to try out all the possible ways to queue up. In fact, even if you are superfast and can try one way to queue up in 1sec, it will ake about 77billion years to try out all possible ways, even with a small class of just 20.

### Factorials are large

Factorials are fairly large numbers. They become large quickly, much faster than power terms (such as \\(n^2\\)) or even exponential terms (such as \\(2^n\\)). The table below compares \\(n, n^2, n^3 \\) with \\( 2^n, 3^n, 4^n \\) and \\( n! \\), for say \\( n = 1, 2, ..., 10 \\) and \\(20\\).

| n	| ---> 	| 1	| 2	| 3	| 4	| 5	| 6	| 7	| 8	| 9	| 10	| ...	| 20    |
| ---:  | ---: 	|---:  | ---:  | ---:  | ---:  | ---:  | ---:  | ---:  | ---:  | ---:  | ---:  | ---:  | ---:  |
| \\(n^2\\) |   	|1	| 4	| 9	| 16	| 25	| 36	| 49	| 64	| 81	| 100	| 	| 400 |
| \\(n^3\\) 	|   	| 1	| 8	| 27	| 64	| 125	| 216	| 343	| 512	| 729	| 1,000	| 	| 8,000 |
| \\(2^n\\) 	|  	| 2	| 4	| 8	| 16	| 32	| 64	| 128	| 256	| 512	| 1,024	| 	| 1,048,576 |
| \\(3^n\\) 	|  	| 3	| 9	| 27	| 81	| 243	| 729	| 2,187	| 6,561	| 19,683	| 59,049	| 	| 3,486,784,401 |
| \\(4^n\\) 	|  	| 4	| 16	| 64	| 256	| 1,024	| 4,096	| 16,384	| 65,536	| 262,144	| 1,048,576	| 	| 1,099,511,627,776 |
| \\(n!	\\) |  	| 1	| 2	| 6	| 24	| 120	| 720	| 5,040	| 40,320	| 362,880	| 3,628,800	| 	| 2,432,902,008,176,640,000 |



