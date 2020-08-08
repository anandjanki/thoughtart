---
title: "Exponential Growth"
date: 2020-08-01T19:40:20+05:30
draft: false
weight: 1
---

We explored the Laws of Indices and Surds in a previous session. Lets take that one step further by exploring exponentials before venturing into Logarithms.

You may have heard this puzzle in your childhood - there is a pond with a lotus plant growing. On the first day, one lotus flower blooms from the plant. On the second day, there are two flowers. On the third day, there are four flowers and so on. In other words, the number of lotus flowers doubles every day. On the 20th day, the entire water tank is filled with lotus flowers. When was the tank half full?

Well, if you are not a little careful, the tendency is to halve 20 and blurt out the answer 10. But if you spend a few extra seconds thinking carefully, you realize that the correct answer is that the pond would have to be half full on the 19th day for it to be completely full on the 20th day.

While we are on this topic, take a few mins to check out this lake in Thailand where the lotus blooms something like this[^redlotus]:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/red-lotus-sea.jpg" class="figs" title="" >}}
<--->
{{< /columns >}}

[^redlotus]: Photo details [here](https://in.pinterest.com/pin/394205773627036784/) / Credit : Tara Greene / No licensing details

This is so vast that it is sometimes referred to as the Red Lotus Sea, you can read a travelog about the lake [here](https://www.tielandtothailand.com/red-lotus-sea-udon-thani/).

## Growth of Bacteria

While lotuses do not really exhibit such growth patterns, the growth of bacteria is indeed of this nature! Shown below is a false color time-lapse video of an E.coli colony growing on microscope slide[^ecoli]. E.coli is a common bacteria found in the intestines of many animals including humans.

[^ecoli]: Photo details [here](https://commons.wikimedia.org/wiki/File:E.coli-colony-growth.gif) / CC BY-SA 4.0

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/Ecoli-colony.gif" class="figs" title="" >}}
<--->
{{< /columns >}}

Notice the timescales in the video. For the first 100mins or so, there are hardly any bacteria, only a handful of them that you can literally count. Around 150mins or so, you see that the growth seems to accelerate and by 300mins, the entire slide is filled with the bacteria.

## Human Population

What's interesting (and in some ways scary too) is that humans have also exhibited similar growth patterns over our history on this planet. 

{{< iframe width="100%" height="600px" src="https://www.worldometers.info/world-population/#pastfuture" >}}

As can be noted from the graph above - whereas it had taken all of human history until around 1800 for world population to reach one billion, the second billion was achieved in only 130 years (1930), the third billion in 30 years (1960), the fourth billion in 15 years (1974), and the fifth billion in only 13 years (1987). More details can be found by scrolling within the picture above, or by visiting the website [here](https://www.worldometers.info/world-population/#pastfuture).

Fortunately, the growth rate has been dropping recently and we can witness that in the last part of the graph that is showing signs of slowing down. The last part of the graph is not exactly exponential, it is called a logistic curve. But we can ignore that detail for now.

## Compound Interest

The idea of compound interest is based on exponential growth, which is why if you have a little money and you can save it in a bank or such, you should always prefer compounding returns as opposed to simple.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/compound-interest-diagram.jpg" class="figs" title="" >}}
<--->
{{< /columns >}}

The formula for the final Amount, \\( A \\) in terms of the original Principal, \\( P \\), the Rate of Interest, \\( R\\) and crucially the Number of years, \\( N\\) is as well known in both cases:

{{< katex >}}
\begin{array}{rcl}
A_{SI} & = & P\cdot (1 + \displaystyle \frac{NR}{100}) \\ \\
A_{CI} & = & P\cdot (1 + \displaystyle \frac{R}{100})^N \\ \\
\end{array}
{{< /katex >}}

Notice the small change in the placement of the variable \\( N\\) in both the formulae, that makes all the difference. In words, in the case of Simple Interest, once the original principal yields some interest in the first year, that interest is withdrawn, and the next year the *same* original principal yields an interest. But in the case of compound interest, the interest from the first year itself contributes to *additional* interest in the second year, and in the long run that makes all the difference. We will look more carefully into this idea in a later session.

## The Chess reward

By now it should be clear that exponential growth quickly gets to be very very large. Another story that you may have heard is the reward the inventor of the game of chess asked from a king. While the story itself is likely cooked up, it brings out the how large exponentials can quickly grow to.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/chessboard.jpeg" class="figs" title="" >}}
<--->
{{< /columns >}}

The 5th row above already has 512 billion grains of rice! And if we keep going to the end of the board, in order to fill just the last square, we will have to plant the entire land area of earth with rice, not just once but four times over!!

## Virus spread

The scare associated with the spread of the Coronavirus (SARS-Cov-v2) is similar, it exhibits exponential growth. The infection can keep spreading from the first person who got the infection, and also from every new person who gets the infection. that is what causes the exponential growth.

The number of cases in India over the last 5 months (Feb-2020 to Jul-2020) is shown below[^coronajhu]:

[^coronajhu]: Snapshot from JHU COVID-19 dashboard [here](https://coronavirus.jhu.edu/map.html).

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/corona-india.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Italy, and other European countries which were soaring with cases earlier on, have managed to successfully curb the spread using extensive testing, effective containment and other such strategies to have a graph as shown below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/corona-italy.png" class="figs" title="" >}}
<--->
{{< /columns >}}

On that note, lets explore exponentials and logartihms.
