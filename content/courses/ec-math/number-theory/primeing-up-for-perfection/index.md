---
title: "1.2 PRIME-ing up, for PERFECT-ion"
date: 2020-02-06T21:32:29+05:30
draft: true
weight: 2
---

We encountered prime numbers in the previous session on GCD and took a brief look at them. Prime numbers have fascinated mathematicians for 1000s of years, almost from the very beginning. Even today, prime numbers continue to play a central role in many fields, one of the latest being cryptography. To recap the definition of prime numbers:


{{< highlight-box "Defn 1:" "none" "" "part" >}}
A natural number p > 1 is called a prime number if it has no divisors other than 1 and p itself.
{{< /highlight-box >}}

A (natural) number that is not a prime number is called composite.

Recall the game with Scrabble tiles, can we arrange 12 of them in a rectangle? 

{{< figure src="images/3x4=12.png" class="figs" title="3 x 4 = 12" >}}

{{< figure src="images/2x6=12.png" class="figs" title="2 x 6 = 12" >}}

{{< figure src="images/1x12=12.png" class="figs" title="1 x 12 = 12" >}}

Now, we simply add 1 more tile and make it 13. Suddenly, with 13 tiles, we can only form one rectangle of size 1 x 13. How did that happen? What is special about 13? Or for that matter 17 or 19? 

{{< figure src="images/1x13=13.png" class="figs" title="" >}}

Here is a nice pic (from Wikipedia) depicting the first few numbers and whether or not they can be expressed as a product of numbers different from 1 and the number itself.

{{< columns "30,40,30" >}}
<--->
{{< figure src="images/first-few-prime-composite.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Do these numbers have any special properties? How many of these numbers are there? How do we find them? What can we do with them? We will find answers to some of these questions in this session.

## Is 10007 a prime number?

First let’s figure out how to check if a number is prime or not. Recall how we went about finding divisors of a number in the session on GCD. But do we need to go through all that work? Note that we simply need to search for *one* divisor of the number, if we find even one divisor then we know that the number is *not* prime. 

So the next question is - how many numbers do we need to search for finding a divisor of a number, if one exists? Again, recall how we learnt that to search for all divisors of a number we only need to search until the square root of the number. This is stated formally here.

{{< theorem-block "Claim" "Proof" >}}
If \\( b\cdot c = a\\) and if \\( b \leq c\\) , then \\( b \leq \sqrt{a} \\).
<--->
\\( \because b \leq c \\)   
\\( \therefore b\cdot b \leq b\cdot c \\)  (for natural number b and c)   
\\( \therefore b^2 \leq a \\)  
\\( \therefore b \leq \sqrt{a} \\)  

Hence proved.
{{< /theorem-block >}}

In words, divisors of a number come in pairs. And the smaller of the pair is always less than square root of the number. So, if 1 is the only divisor of a number less than the square root of the number, then the number itself is prime.

Just to get a feel for how much effort we are saving by searching for divisors only within the square root of a number, see the picture below. See how small the range from 0 to 100 is.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/square_root_10000.png" class="figs" title="" >}}
<--->
{{< /columns >}}

If we have to find whether 10,007 is prime, we only need to search for a divisor until 100. If we don’t find a divisor, then we are done, we can say that it is a prime number. Further, it turns out that we only need to check for prime factors within 100. We will see why shortly.


