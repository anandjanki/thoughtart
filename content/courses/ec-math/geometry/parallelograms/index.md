---
title: "2.3 About Parallelograms"
date: 2020-03-25T14:40:48+05:30
draft: false
weight: 3
---

As we expand from triangles into the world of quadrilaterals, one of the first few we encounter are of course the square and the rectangle. Parallelograms are not far behind, and hold many secrets, some of which we explore in this session.

## Quadrilaterals

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A **quadrilateral** is a planar figure with 4 sides (edges) and 4 corners (vertices).
{{< /highlight-box >}}

Based on this definition, we can draw a few different kinds of quadrilaterals shown below:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/quadrilateral-types.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The difference between simple quadrilaterals and complex quadrilaterals should be easy to note, it is whether we allow the edge crossings in the quadrilateral or not.

Within simple quadrilaterals, the difference between convex quadrilaterals and concave quadrilaterals may take a little effort to note, essentially, all of the angles in a convex quadrilateral are less than \\(180\degree \\). In a concave quadrilateral, we allow for any one of its angle to be greater than \\( 180\degree \\). 

Another nice way to differentiate between convex and concave quadrilaterals is the following - in a convex quadrilateral, every line between any two points inside the quadrilateral also falls within the quadrilateral. In a concave quadrilateral, that need not be the case, we can find points which line within the quadrilateral, but the line joining the points may not entirely lie within.

### Convex Quadrilateral

We will limit our discussions mostly to convex quadrilaterals for now. And note the following well known property about the angles of the quadrilateral:

{{< theorem-block "Theorem" "Proof" >}}
The interior angles of a convex quadrilateral add up to \\( 360\degree \\)

$$ \angle A + \angle B + \angle C + \angle D = 360\degree $$
<--->

.   
.   
.   
.   
.   
.   
.   
.   
.   
Hence proved.

{{< /theorem-block >}}

We can also check if this property holds true for the other kinds of quadrilaterals - concave ones, and what about complex ones?

### Convex Quadrilaterals Types

A few different types of convex quadrilaterals are shown in the picture below:
{{< columns "10,80,10" >}}
<--->
{{< figure src="images/convex-quadrilateral-types.svg" class="figs" title="" >}}
<--->
{{< /columns >}}

The angles / sides in a quadrilateral depicted in the same color have the same measure, and the definitions of the different kinds of quadrilaterals above should be self evident.

It is an interesting exercise to draw a nice Venn Diagram to illustrate the relationship between the different kinds of quadrilaterals. For e.g., All rectangles are parallelograms; all squares are rectangles; the set of parallelograms includes the set of rhombi and the set of rectangles; etc.

## Parallelograms

### Definition

There are many alternate ways to define a parallelogram. The simplest is of course the following:

{{< highlight-box "Defn 2:" "none" "" "part" >}}
A **parallelogram** is a quadrilateral with two pairs of oppposite sides parallel.
{{< /highlight-box >}}

As it turns out, this definition is equivalent to many other properties. Some of these are listed below:

- Two pairs of opposite sides are equal in length.
- Two pairs of opposite angles are equal in measure.
- The diagonals bisect each other.
- One pair of opposite sides is parallel and equal in length.
- Adjacent angles are supplementary.

It is usually a fun exercise to start with any of the properties and arrive at another. Here is one example.

{{< theorem-block "Theorem" "Proof" >}}
If two pairs of opposite sides of a quadrilateral are equal in length, prove that the two pairs are also parallel and hence the quadrilateral is a parallelogram.
<--->

{{< columns >}}
The key is to make a construction, in this case, to draw the diagonal BD. And then use the tools of the trade, in this case, a congruence test.
.   
.   
.   
.   
.   
.   
<--->
{{< figure src="images/parallelogram-proof.png" class="figs" title="" >}}
{{< /columns >}}

Hence proved.

{{< /theorem-block >}}

### Parallelogram law

A very interesting property of parallelograms pertains to the relationship length of the sides of the parallelogram with its diagonals. It is especially interesting because it can be thought of as an extension of the famous Pythagoras theorem.

{{< theorem-block "Theorem" "Proof" >}}
{{< columns >}}
In a parallelogram,
$$ 2\cdot(AB)^2 + 2\cdot(BC)^2 = (AC)^2 + (BD)^2 $$
<--->
{{< figure src="images/parallelogram-law-theorem.png" class="figs" title="" >}}
{{< /columns >}}

<--->

{{< columns >}}
The key is to make a construction, in this case, to draw a perpendicular \\(DM\\) such that \\( AM = x\\).

And to also draw \\( CN \perp AB \\). 
<--->
{{< figure src="images/parallelogram-law-proof.png" class="figs" title="" >}}
{{< /columns >}}

Now, we can apply Pythagoras theorem in the triangles \\( \triangle DAM\\) and \\( \triangle DBM \\), and write out the side \\( (DM)^2 \\) in terms of the other sides. That will give us what \\(x\\) is in terms of \\( a\\), \\(b\\) and \\(d\\).   
.   
.   
.   
.   
.   
.   
Next, we can apply Pythagoras theorem in the triangles \\( \triangle CAN\\) and \\( \triangle CBN \\), and write out the side \\( (CN)^2 \\) in terms of the other sides. That will give us what \\(x\\) is in terms of \\( a\\), \\(b\\) and \\(c\\).   
.   
.   
.   
.   
.   
.   
Finally, substitute the value of \\( x \\) from the first step above into the second step above to get a relation between \\(a\\), \\(b\\), \\(c\\), and \\(d\\).
 
.   
.   
.   
.   
.   
.   
Hence proved.

{{< /theorem-block >}}

In the case of a rectangle where the diagonals are equal in length, the parallelogram law becomes the same as Pythagoras theorem.

What is even more interesting is the version of the parallelogram law for generic quadrilaterals. This is left as an open exercise to try out separately.

### Area of a parallelogram

If the base side of the parallelogram is known and its height, then the area of the parallelogram is well known to be simply \\( A = b\times h\\).
{{< columns "30,40,30" >}}
<--->
{{< figure src="images/parallelogram-area.png" class="figs" title="" >}}
<--->
{{< /columns >}}

If the two sides are known and the angle formed by the sides is known, then the area is given simply by \\( A = a\times b\times \sin \alpha \\).

An interesting property pertaining the area of the parallelogram, that is fairly easy to prove, is that *any line* passing through the point of intersection of the diagonals of the parallelogram, divides the parallelogram into two parts with equal area. Draw a picture, and check it out yourself.

A more interesting property pertaining areas in the parallelogram is the following, attributed to Euclid.
{{< theorem-block "Theorem" "Proof" >}}
{{< columns >}}
If lines parallel to the sides are drawn through any point on a diagonal of a parallelogram, then the parallelograms not containing segments of that diagonal are equal in area, \\( A_1=A_2 \\).
<--->
{{< figure src="images/parallelogram-part-areas.png" class="figs" title="" >}}
{{< /columns >}}
<--->

{{< columns >}}
The first step is to write out \\( A_1\\) and \\( A_2\\) in terms of the quantities marked in the figure.   

\\( A_1 = (a - x)\cdot y\cdot \sin \alpha \\)   
\\( A_2 = (b - y)\cdot x\cdot \sin \alpha \\)   
<--->
{{< figure src="images/parallelogram-part-areas-proof-p1.png" class="figs" title="" >}}
{{< /columns >}}

The next step and the key step is to note the presence of similar triangles with the parallel lines that have been drawn. Two such similar triangles are marked in red in the pic below.

{{< columns >}}
{{< figure src="images/parallelogram-part-areas-proof-p2.png" class="figs" title="" >}}

<--->

The sides of these triangles are in proportion, yielding:  

\\( \displaystyle \frac{x}{a} = \displaystyle \frac{y}{b} \\), or   
\\( b\cdot x = a\cdot y \\)

{{< /columns >}}

Substituting this in the above formulae for \\(A_1\\) and \\(A_2\\) yields the desired result.

Hence proved.

{{< /theorem-block >}}

## Squares on the Parallelogram

Another interesting finding, also dating back to Euclid's time is the following - you draw squares on the sides of the parallelogram, and if you connect the centers of those squares, like magic, it turns out to be a square. Proving this turns out to be reasonably simple, but as always needs creativity in carefully choosing the right set of triangles to draw one's focus to.

{{< theorem-block "Theorem" "Proof" >}}
{{< columns >}}
\\( \square PQRS \\) is a square.
<--->
{{< figure src="images/squares-on-parallelogram.png" class="figs" title="" >}}
{{< /columns >}}
<--->

{{< columns >}}
The first step is to focus attention on \\( \triangle PAQ \\) and \\( \triangle PDS \\).

With a few observations, we can prove that   
.   
.   
.   
.   
.   
.   
.   
.   
\\( \triangle PAQ \cong \triangle PDS \\)

<--->
{{< figure src="images/squares-on-parallelogram-proof.png" class="figs" title="" >}}
{{< /columns >}}

Next, since \\( \angle APQ = \angle DPS \\), and since \\( \angle APD = 90\degree \\),   
\\( \therefore \angle QPS = 90\degree \\).

We have just shown that \\( PQ \\) and \\( SP \\) are equal and form a right angle. We can prove the same about each pair of adjacent sides of the \\( \square PQRS \\), making it a square.

Hence proved.

{{< /theorem-block >}}

It turns out that the squares can be drawn on the inner side of the sides of the parallelogram and the above property still holds true. Do try to draw this picture and try and prove it.

## Varignon parallelogram

A Varignon parallelogram is a parallelogram that gets formed when you connect the midpoints of all four sides of a quadrilateral. It is named after a French mathematician Pierre Varignon in the 1600s.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/varignon-parallelogram-convex-quadrilateral.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Interestingly it turns out this is true with any concave quadrilateral, as well as complex quadrilaterals.

{{< columns >}}
{{< figure src="images/varignon-parallelogram-concave-quadrilateral.png" class="figs" title="" >}}
<--->
{{< figure src="images/varignon-parallelogram-complex-quadrilateral.png" class="figs" title="" >}}
{{< /columns >}}

It should be fairly easy to prove this, using similar triangles to find equal angles and hence parallel lines.

A few simple properties can be proven for the Varignon parallelogram:

- The area of the Varignon parallelogram is half the area of the original quadrilateral.
- The perimeter of the Varignon parallelogram is equal to the sum of the diagonals of the original quadrilateral.

## Wittenbauer Parallelogram

A parallelogram shown up in surprising places, one more such is depicted below. Consider any general quadrilaterial, and trisect each of the sides of the quadrilaterial. Now, if we join the adjacent points on adjacent sides by lines, these lines togehter form a parallelogram. this is shown in the pic below.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/parallelogram-by-trisecting-quadrilateral-sides.png" class="figs" title="" >}}
<--->
{{< /columns >}}

\\( \square PQRS \\) in the above figure turns out to be a parallelogram. Similar to the Varignon parallelogram, it should be fairly easy to prove this, using similar triangles to find equal angles and hence parallel lines. Do try it out.

