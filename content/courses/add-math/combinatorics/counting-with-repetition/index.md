---
title: "Counting with Repetition"
date: 2020-01-24T18:05:19+05:30
draft: true
weight: 2
---

## Cracking the combination

Let's start with the total numbers that are there between 1 and 1000 (both inclusive). Even the youngest of kids would know that there are obviously 1000 numbers in this range. Let's just shift the start and the end a little and ask - how many numbers are there between 0 and 999 (both inclusive), the answer is again 1000 numbers.

Now lets consider this same counting problem in a different scenario. Let's say we have a suitcase with a 3-digit combination lock. A picture is below:

{{< figure src="briefcase-combination-v5.jpg" height="200px" class="figs" title="Briefcase with a combination lock having 3 digits" >}}

The question we are asking is how many different ways are there to set a 3-digit code for this combination lock. Yet another way to ask the question is what is the maximum number of codes one would need to try in order to crack the combination.

In order to find the answer to this question, lets start counting. 

The way to go about counting is as follows. Consider the first digit of the code. How many ways are there to set this first digit? The possible values this first digit can have is anything from 0 to 9. Thats 10 ways to set the first digit. The second digit can likewise be set in 10 different ways, and the same holds true for the last digit.

Thus the total number of ways of performing the combined action of setting the code for the combination lock is 10 x 10 x 10.

{{< katex >}}
{{< /katex >}}

That is \\(10^3\\) or 1000 different codes. And that is also the *maximum* number of codes one would need to try in order to crack the combination.

### Odd-looking codes

Now, suppose we have a 4-digit combination lock. A code is called "odd-looking" if all of the digits are odd. 1357 is an example of an odd-looking code, 7799 is another example. How many such 4-digit codes exist?

We know that there are 5 odd digits obviosuly - 1, 3, 5, 7, and 9. The first digit of the code can thus be set in 4 ways, the second digit can also be set in 5 different ways, and the same holds true for the third and the fourth digit as well. Again, applying the product rule, the total number of odd-looking codes possible is 5 x 5 x 5 x 5 i.e. \\(5^4\\) or 625 codes.

As in the case of the St Ives [kittens counting]({{< ref "basics-of-counting#kittens-galore" >}}) exercise, we can write out these odd-looking codes systematically as follows:

{{< figure src="odd-looking-combinations.png" height="400px" class="figs" title="Counting odd-looking codes" >}}

Shown in figure above are 5 codes - 1111, 1113, 1115, 1117, and 1119 and a way to systematically enumerate out all of the \\(5^4\\) or 625 codes (should someone really want to do that :).

## A new language

Suppose we were to come up with a new language using the same alphabets of the English language. Suppose, we also decide to constrain ourselves to only 5-letter words, i.e. all the words of our new language will exactly 5-letters only. What do you think, would our new language have a very small vocabulary or would it be good enough?

A few tidbits before we answer this question. The total number of words in some of the most well known and comprehensive English dictionary of today maybe around 300,000 or so. A list of a few such dictionaries is [here](https://en.wikipedia.org/wiki/Comparison_of_English_dictionaries) on Wikipedia. The number of 5-letter words would be about 30,000 or so. A sample of 5-letter words some of them starting from the letter D, and some from E can be found [here](https://www.bestwordlist.com/5letterwordspage4.htm).

Now, coming back to our task of putting together the new language consisting only of 5-letter words. What are the maximum number of words we can possible have in the vocabulary of this new language?

The way to go about counting is as follows. Consider the first letter of the word. How many ways are there to fill this first letter? There are 26 different ways in which we can set the first letter. The second letter can also be filled in 26 different ways, and the same holds true for the 3rd, 4th and 5th letter. 

Thus the total number of ways of performing the combined action of creating 5-letter words, and the number of 5-letter words themselves is \\(26^5\\). You will need a calculator to check that this number is fairly large, it is 11,881,376, which is 40 times the size of the above dictionaries!!

### Counting with repetition

We saw a few examples in this section where the answer has been an exponential. In all these cases, we did not have any uniqueness constraint between the digits of the combination code, or the letters of a word in the new language above. In the previous example, we allowed for the letters to repeat. For e.g., AABAA would be a perfectly valid word in this new language. Hence this is commonly know as counting with repetition.

## Practice Problems

As before, can you come up with a couple of problems of your own where there is counting with repetition.

Here is another problem that involves such counting.

{{< tabs "CWR-1" >}}
{{< tab "Problem" >}}

You have taken up 7 different subjects for your 10th grade exams.

In the early days, you decide to study for an hour each day of the week. At the end of the week, how many different ways in which your study calendar could have looked like?

{{< /tab >}}

{{< tab "Hint" >}}

In one particular week, you could have spent the entire week studying only Math. In another week, your calendar could have been 3 days of Biology, 3 days of Literature and 1 day of English. In other words, each day you can repeat a subject that you already did earlier in the week.

{{< /tab >}}

{{< tab "Solution" >}}

The number of ways the study calendar can look like each week is \\(7^7\\).

{{< /tab >}}

{{< /tabs >}}

A slightly different version of the same problem is below:

{{< tabs "CWR-2" >}}
{{< tab "Problem" >}}

If you had only 3 subjects and let's say only 5 days of the week, then how many different ways in which the caneldar could look like?

Is it \\(3^5\\) or \\(5^3\\)?

{{< /tab >}}

{{< tab "Hint" >}}

If you had only 1 subject, then how would your calendar look over the 5days? Will you have \\(5^1\\) ways or \\(1^5\\) ways.

{{< /tab >}}

{{< tab "Solution" >}}

With only 1 subject, there is only 1 way the calendar can look. On all 5 days of the week, it is the same subject. So the number of ways is 1 x 1 x 1 x 1 x 1 = \\(1^5\\) = 1 way only.

With 3 subjects, every day you have 3 choices for which subject you want to study. So the number of ways for the study calendar is 3 x 3 x 3 x 3 x 3 = \\(3^5\\) or 243 ways.

{{< /tab >}}

{{< /tabs >}}

