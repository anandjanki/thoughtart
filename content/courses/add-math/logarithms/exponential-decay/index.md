---
title: "Exponential Decay"
date: 2020-08-08T09:12:38+05:30
draft: false
weight: 3
---

We have looked at exponentials to see how they aid the handling of large numbers. In that same session we also saw how exponentials aid in the study of [very small numbers]({{< ref "exponents-at-work#very-small-numbers" >}}). Similarly, just like we saw exponential growth functions taking on very large values, we now look at exponential decay functions.

## Coffee gets cold

Ever wondered how your favorite hot drink gets cold? Imagine you made yourself a hot cup of coffee or a hot chocolate and got back to your desk to read up your mails while sipping on your drink. But then you see a mail that draws all your attention to it, you respond to it, someone else also responds, a discussion ensues, you start searchign the internet for information to justify your stance, and so on and so forth. In all of this of course, the hot coffee has been lying on the desk untouched. A small pause in the flurry of activity and the coffee comes back into your attention. You take one sip of it and let out a groan, it has obviously become cold by this time.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/coffee-mug.png" class="figs" title="" >}}
<--->
{{< /columns >}}

What most people would do is maybe curse the coffee or the mail or something else, reheat the coffee or make a new one and then forget about the whole incident.

Newton of course was different. He asked the crucial question
$$ \text{WHY?} $$
Why did the coffee go cold? So he stuck a thermometer into the coffee to start measuring and understanding unearthing what is happening, why is it happening, and discovered the law of cooling that now carries his name.

It could have been anyone. All that it needed was a thermometer.. :) Well, and a LOT of inquisitiveness to go with it. You could do this at home too, but beware the medical thermometer WILL NOT work for this purpose, they typically have a range between \\( 35 \text{ \textdegree C} \\) and \\( 40 \text{ \textdegree C} \\) or so, whereas a boiling cup of coffee would be almost at a \\( 100 \text{ \textdegree C}\\). Check the range of your thermometer before you try it, else you may have the sorrow of a broken thermometer rather than the joy of rediscovering the cooling law.

There are a few more facts that we know that may help us discover the law of cooling. If you have been on vacation up in the mountains in a very cold climate, you may have noticed that your coffee gets colder much faster. One doesnt need to go into the mountains to see this, even at home if you turn on the fan then the hot drink becomes cold faster. 

Put differently, if the coffee were to start at \\( 100 \text{ \textdegree C}\\), then the amount of time it takes to reach say \\( 50 \text{ \textdegree C}\\) varies depending on the surrounding temperature itself. If the temperature of the place is pretty high at \\( 45 \text{ \textdegree C}\\), then we expect it to take longer to reach \\( 50 \text{ \textdegree C}\\), and if the atmospheric temperature is say a low of \\( 25 \text{ \textdegree C}\\), then the coffee would cool much faster, and so reach the same temperature of \\( 50 \text{ \textdegree C}\\).

It will take some effort to start from here and work out the function that behaves in the above manner. So, we will go with the answer for now. 

### Negative exponentials

It turns out to be an exponential function again, but this time the exponent is negative. Such a function would look like follows:
$$ f(x) = k^{-x} $$
Note that this is the same as:
$$ f(x) = \displaystyle \frac{1}{k^x} $$

Lets take a couple of values of \\( k\\), say \\( k = 2\\) and \\( k = 10 \\) and see how the graph of these functions look along with the corresponding positive exponential. This is depicted in the picture below.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/positive-negative-exponentials.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We can tabulate the values of the function for different values of \\( x \\) and see the pattern:

{{< table "horizontal-table" >}}
| \\(x\\) | \\(10^x \\) | \\(10^{-x} \\) | \\(2^x \\) | \\(2^{-x} \\) |
| :-- | :-- | :-- | :-- | :-- |
| 4 | 10000 | 0.0001 | 16 | 1/16 |
| 3 | 1000 | 0.001 | 8 | 1/8 |
| 2 | 100 | 0.01 | 4 | 1/4 |
| 1 | 10 | 0.1 | 2 | 1/2 |
| 0 | 1 | 1 | 1 | 1 |
| -1 | 0.1 | 10 | 1/2 | 2 |
| -2 | 0.01 | 100 | 1/4 | 4 |
| -3 | 0.001 | 1000 | 1/8 | 8 |
| -4 | 0.0001 | 10000 | 1/16 | 16 |
{{< /table >}}

We have already looked at the graph of the positive exponentials, the function \\( y = 2^x\\). The graph of the negative exponential function \\( y = 2^{-x} \\) is just a reflection on the y-axis.

As before, here is a picture with the negative exponential depicted for a few different values of \\(k\\) to get a sense of the relative rate of "decay".
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/negative-exponentials-1.png" class="figs" title="Exponential decay for different values of k" >}}
<--->
{{< /columns >}}

Often the region of the graph for \\(x \geq 0 \\) is of interest. A zoomed in version of the graphs of these functions in this domain is depicted below:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/negative-exponentials-2.png" class="figs" title="Exponential decay for different values of k for x >= 0" >}}
<--->
{{< /columns >}}
Notice that at \\( x = 0\\), all these functions have a value of \\(1\\) and as \\( x \to \infty \\) all the functions \\( \to 0 \\).

### Newton's Law of Cooling

We can now picture what Newton discovered about how hot liquids cool down. The graph of the temperature of the liquid with the passage of time would look somewhat like below:

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/newtons-law-of-cooling.png" class="figs" title="Newton's law of cooling" >}}
<--->
{{< /columns >}}

You can ignore the algebraic expression of the function and focus on the nature of its graph instead. What it says is that at time \\( t = 0\\), suppose the liquid has a temperature of \\( 100 \text{ \textdegree C} \\), and suppose the room temperature is \\( 25 \text{ \textdegree C} \\), then the temperature of the liquid will keep falling in an exponential manner and in about 7 or 8 minutes (we will assume that is the unit of time on the x-axis), the temperature of the liquid will have fallen to close to \\( 25 \text{ \textdegree C} \\). As time progresses, the temperature will tend \\( \to 25 \text{ \textdegree C} \\), but will never go below that value, assuming the room temperature remains constant at that value.

This may be one of Newton's lesser known discoveries, his laws of motion are of course way more path breaking in our understanding of how nature works. But all that it takes is relentlessly asking why, why, why, ... and not stopping until the answer is found.

## Dinosaurs are old

Lets look at one more story where exponential decay shows up. Its in the study of paleontology or of fossils. Here is a brief video describing this field and how it helps uncover the past history of our planet.

{{< youtube "bRuSmxJo_iA" >}}

The most natural question that comes to mind when you discover a fossil is how old is it. How do we know how long ago did plant/animal that we are looking at live?

### Carbon Dating

One of the most brilliant discoveries in our times is that of Carbon Dating, a method developed by Williad Libby from the University of Chicago, and deservedly won the Nobel Prize in Chemistry for this work. It is based on the principle called the half-life of an element which is a process that exhibits exponential decay. This brief video explains how:

{{< youtube "phZeE7Att_s" >}}


