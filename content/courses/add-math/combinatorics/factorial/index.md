---
title: "Factorial"
date: 2020-01-25T01:26:59+05:30
draft: false
weight: 3
---

## St Ives revisted

Here is a new version of the St Ives poem:

> As I was going to St Ives,   
> Upon the road I met 2 wives;   
> Every wife had 3 sacks,   
> Every sack had 4 cats,   
> Every cat had 5 kits,    
> I am not playing any tricks,    
> Just count and tell me the number of kits.  

Counting the number of kittens is similar to before except that the numbers involved here are a little different. The pictorial depiction for counting all the kittens is shown below.

{{< figure src="StIves-factorial.png" class="figs" title="A picture to aid the counting of the kittens" >}}

And the counting can be done as follows:

    The First wife's --> First sack's --> First cat has => 5 kittens
    First wife's --> First sack --> has 4 cats with => 4x5 kittens
    First wife --> has 3 sacks with => 3x4x5 kittens
    2 wives have => 2x3x4x5 kittens

Thus the total number of kittens is 120.

## Factorial definition

The number 5 x 4 x 3 x 2 x 1 is called the factorial of 5 and is denoted by 5!

In general, for any natural number n, the factorial of the number is defined as follows:
{{< katex >}}
n! \equiv n \cdot (n - 1) \cdot (n - 2) \cdots 2 \cdot 1
{{< /katex >}}

It is important to note that in the above counting problem, the occurence of the factorial is purely incidental. The author could have seen 3 wives, each carrying say 2 sacks, each with say 20 cats and so on. In that case, the answer will not be a factorial of any number.

But in the next topic of permutations, we will see that the factorial of a number shows up naturally in many kinds of counting problems.

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



