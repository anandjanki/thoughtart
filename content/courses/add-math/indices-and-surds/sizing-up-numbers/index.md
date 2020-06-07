---
title: "Sizing Up Numbers"
date: 2020-06-07T11:08:03+05:30
draft: false
weight: 1
---

## Big Numbers

In a previous session we encountered this puzzle of an author on the way to St Ives, when he sees 7 wives on the way, each carrying 7 sacks, each with 7 cats, each with 7 kittens. And we found that the total number of kittens were 7 x 7 x 7 x 7 = 2401 kittens. Those many kittens would be hard to manage, but the number itself easily manageable.

But imagine we had to write a science fiction novel, where our hero is on a journey across the Milky Way galaxy and needs to reach the Andromeda Galaxy. Our story may look somewhat like this:

> Reoh's spacecraft had just travelled 151,810,000 kms from Earth. But not to worry, he wasn't going to crash into the Sun, for he was headed in a different direction, his first stop was Alpha Centauri which was 40,000,000,000,000 kms away from Earth. The very thought of the distance gave him the shivers. But this was just the beginning of his journey, and Alpha Centauri was only the first star he was going to pass. 

> Cutting across the Milky Way galaxy, he would have to pass through several several of the estimated 250,000,000,000 stars in our galaxy. From Earth, the 250,000,000,000 stars of the Galaxy looked like a cloud of smoke cutting across the night sky. From where he was now, this cloud of 250,000,000,000 stars was like a smattering of sparkles. He needed a vantage point from where he would be able to see all the 250,000,000,000 stars in all its glittering glory. Maybe that would happen once he leaves the Mily Way, and somewhere on the way to Andromeda.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/galaxies-NGC4302-NGC4298-Hubble.gif" class="figs" title="A picture released by Hubble Telescope on its 27th birthday." >}}
<--->
{{< /columns >}}

This animation zooms through the Virgo Cluster of nearly 2,000 galaxies into tight Hubble Space Telescope images of spiral galaxies NGC 4302 (left) and NGC 4298 (right) in visible and infrared light. Located approximately 55 million light-years away, the starry pair offers a glimpse of what our Milky Way galaxy would look like to an outside observer[^1].

[^1]: NASA link [here](https://www.nasa.gov/feature/goddard/2017/a-new-angle-on-two-spiral-galaxies-for-hubbles-27th-birthday). Credits: NASA, ESA, and G. Bacon, J. DePasquale, and Z. Levay (STScI) Acknowledgment: A. Fujii; Digitized Sky Survey (DSS), STScI/AURA, Palomar/Caltech, and UKSTU/AAO; B. Franke (Focal Point Observatory); and M. Mutchler (STScI). 

As you can imagine, carrying big numbers around like that is not easy and we have come up with ways to handle these. One way we have come up with is to give names to some of the large numbers. Thus, we would say Alpha Centauri is about 40 trillion kms away, and is only 1 of the 250 billion stars in our galaxy.

But then we do not need to go so far to encounter big numbers. You may be surprised to know what we ourselves are made of. Imagine this little story:

> Reoh's last few days before his departure from Earth were full of fun and frolic. His entire family had gathered together for a grand week long party at his farmhouse. As he and his brother were walking through the backyard recounting several childhood stories joyously, he missed noticing the slippery ground from the watering of the plants. And in one misstep he found himself flat on the floor.

> His entire body made up of 37,200,000,000,000 cells came crashing against the hard floor. Most of these cells were each carrying about 12,000,000,000 nucleotide molecules tightly woven at the core of the cell's nucleus making up his genetic material. A nasty jolt for the 446,400,000,000,000,000,000,000 nucleotide molecules in his body. Imagine them, all of them together, hurlting through the 1m fall. Would they get disintegrated by the jolt, he wondered, or were the bonds strong enough to keep them intact? 


We can manage prose like above by introducing names to large numbers such as million, billion, crore, etc. But as you can imagine, the key point is that as the numbers become bigger, we need better tools to handle them. Even the simple operation of multiplying such large numbers above soon gets unwieldy if we have keep writing out such large numbers in every step. 

Lets ask ourselves a question first - How do such large numbers come about?

One instance where we encountered such large numbers was in counting problems, we found that the factorial of a number becomes [very large very quickly]({{< ref "factorial#factorials-are-large" >}}). In the same context, we also encountered another way by which we get large numbers. 

By repetition. 

By repeated application of an operation such as addition or multiplication.

### Repeated addition
We know well from childhood how multiplication is simply repeated addition.

{{< columns >}}
{{< figure src="images/3x1=3.png" class="figs" title="3 x 1 = 3" >}}
<--->
{{< figure src="images/3x4=12.png" class="figs" title="3 x 4 = 3 + 3 + 3 + 3 = 12" >}}
{{< /columns >}}

Imagine having to carry around "3 + 3 + 3 + 3" everywhere through your calculations. That would be very cumbersome. What we needed was a notation and a definition, and that is how multiplication came about. We introduced for ourselves a notation called "x" and defined it as follows:

{{< highlight-box "Defn 1:" "none" "" "part" >}}
**Multiplication** is simply repeated application of addition. Given a number \\(a\\) and a positive integer \\(m\\), we define \\(a \times m\\) (pronounced "a times m") simply as:

$$ a\times m = \underbrace{a + a + a + \cdots + a}_{m\text{ times}} $$
{{< /highlight-box >}}

For now, we can stick to positive integer values of \\(m\\), but we of course know that multiplication can be defined between any two arbitrary numbers as well.

### Repeated multiplication

In the same way, we can imagine what would happen if we decide to repeat the multiplication operation. Very quickly we can get some very large numbers. In the St Ives riddle, we encountered the calculation "7 x 7 x 7 x 7" in order to count the number of kittens. Imagine "4 x 4 x 4 x 4 x 4 x 4 x 4", i.e. 4 repeated multipled 7 times, or say 4 repeatedly multiplied 20 times:

{{< katex >}}
\begin{array}{rcl}
7 \times 7 \times 7 \times 7 & = & 2,401 \\
4 \times 4 \times 4 \times 4 \times 4 \times 4 \times 4 & = & 16,384 \\
\underbrace{4 \times 4 \times 4 \times \cdots \cdots \cdots \cdots \cdots \cdots \cdots \times 4}_{20\text{ times}} & = & 1,099,511,627,776 \\
\end{array}
{{< /katex >}}

As you can see these numbers become big pretty quickly. 

Now imagine having to carry around \\(\underbrace{4 \times 4 \times 4 \times \cdots \cdots \cdots \cdots \cdots \cdots \cdots \times 4}_{20\text{ times}}\\) everywhere in a calculation. Or even if we carried the result of this repeated multiplication, the number \\( 1,099,511,627,776 \\), evrywhere in our calculations. That would be a little hard too. We encountered this problem in the stories above. And it is not possible to name this number either. We can give names to some numbers like a million, a billion, etc. But how do we name a number such as \\( 1,099,511,627,776 \\)?

Clearly, what we need is a new notation and a definition, and that is how exponentiation came about. People came up with different notations, but the one that has stuck is the notation \\( 4^{20} \\) to mean take 4 and repeatedly multiply it 20 times. Sometimes when it is not easy to use the superscript notation, where we have to type plain text, like say on a Slack channel, the other notation that is also used often is \\(4\\) ^ \\(20\\). And this is called exponentiation.

{{< highlight-box "Defn 2:" "none" "" "part" >}}
**Exponentiation** is simply repeated application of multiplication. Given a postive number \\(a\\) and a positive integer \\(m\\), we define \\(a^m\\) (pronounced "a power m") simply as:

$$ a^m = \underbrace{a \times a \times a \times \cdots \times a}_{m\text{ times}} $$
{{< /highlight-box >}}

Note that for now, we make the above definition for positive integer values of \\(a\\) as well as positive integer \\(m\\), but we will not hesitate in trying to expand the definition beyond these kinds of numbers.

With this notation, we can now rewrite the above calculations much more succinctly as follows:

{{< katex >}}
\begin{array}{rcl}
7^4 & = & 2,401 \\
4^7 & = & 16,384 \\
4^{20} & = & 1,099,511,627,776 \\
\end{array}
{{< /katex >}}

## Small numbers

What is amazing is that this notation of exponentiation comes in handy in handling very small numbers as well. 

You may ask where do small numbers come up. And for that, lets continue Reoh's story from his fall.

> As Reoh was wondering if his fall would have been a nasty jolt for the 446,400,000,000,000,000,000,000 nucleotide molecules, his thoughts started wandering deeper inside the molecules. Each nucleotide molecule would have about 15 or so atoms within them, atoms of Carbon, Nitrogen, Oxygen and Hydrogen bound together in very particular fashions. Each of these atoms would in turn have a nucleus at their core. 

> This is an atom's nucleus and we have come deep inside the cell's nucleus now. The size of each of nucleus with each cell (each of the 37,200,000,000,000 cells that came crashing against the hard floor) would be about 0.000006 meters. But this cell nucleus has about 12,000,000,000 nucleotide molecules packed inside of it, and each of those molecules have maybe 15 or so atoms. The size of each of these atoms is about 0.00000000009 m, and the size of the nuclues within the atom is much much smaller, about 35,000 times smaller, and would be about 0.0000000000000027 m. Packed inside that nucleus are the protons and the neutrons, 12 each for a Carbon atom. 

> Is it possible at all that Reoh's fall may have disloged some of the protons from even one of the atoms in his body? The thought was profound, but at that time Reoh was woken up by his brother frantically checking if he was all OK.

You would notice that just like large numebrs, carrying around these small numbers are also equally hard. And numbers can get rapidly small.

A small diversion here, check out this image released recently using a technique called unique molecular identifiers (or UMIs), touted as a DNA microscope to reveal a cell's hidden structures[^2].

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/DNA-microscope.jpg" class="figs" title="Individual RNA molecules (coloured dots) in a cell culture, by analysing the products of a chemical reaction and identifying their relative position." >}}
<--->
{{< /columns >}}

[^2]: nature.com link [here](https://www.nature.com/articles/d41586-019-01940-x). Credit: Joshua Weinstein/Broad Institute

We can also intuitively guess how small numbers come about. Again by repetition!

### Repeated subtraction

We will not attempt to write out definitions here, but we know well from our childhood days how division works.

If we have a 100 chocolates with us, and 20 children in the class, we can take 20 chocolates out of the 100 and give 1 chocolate to each of the childen, and then do this repeatedly until we are left with no chololates. How many chocolates would each child have? That is obvious, and that is what division is all about:

{{< katex >}}
\begin{array}{rcl}
100 - 20 - 20 - 20 - 20 - 20 & = & 0 \\
100 \div 20 & = & 5 \\
\end{array}
{{< /katex >}}

Notice the shorthand notation that we introduced \\( \div \\) to succinctly represent what would have otherwise been a very long piece of text to carry around everywhere.

### Repeated division

Finally, what if we imagine doing repeated division of one number by another?

What if we get a branch from an old dry tree, a branch that measures say 1m. And we break it into two halves, the size of each half is of course 0.5m. Then, we take the first half and break it further into two halves, and we keep doing this say 20 times. What is the size of the smallest piece of the branch that we would have?

{{< katex >}}
\begin{array}{rcl}
1 \underbrace{\div 2 \div 2 \cdots \div 2}_{20\text{ times}} & = & 0.00000095367431640625 \\
\end{array}
{{< /katex >}}

In this session, we will see how we can deal with small numbers also quite neatly using the notation of exponentiation and the laws of indices which we venture into next.
