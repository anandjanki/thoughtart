---
title: "2.1 Triangle Secrets"
date: 2020-02-08T19:38:45+05:30
draft: false
---

## Geometry Sessions

Geometry is a standard subject in regular high school Mathematics unlike Number Theory which is usually not covered in regular school curriculums. So, what we will do in these EC Math (Extra-curricular Math) sessions in Geometry will draw upon standard topics we learn in school and go beyond to find some very interesting results and discoveries.

Geometry is also one of the oldest fields of Mathematics, the other being the study of numbers or Arithmetic and Number Theory. We encountered a lot of Euclid in the previous sessions on Number Theory - Euclid’s neat algorithm for finding GCDs, Euclid’s theorem on the existence of infinite prime numbers and his fantastic discoveries of perfect numbers. It turns out that Euclid is actually more famous for his works in Geometry! 

{{< columns "80,20">}}
Discoveries in Geometry pre-date Euclid (300BC) and even Pythagoras (500BC). In fact, we now know that the Pythagoras theorem of right angled triangles was well known even to Indians in the Vedic period (1000BC) and even before that to the Babylonians (before 1600BC). This clay tablet discovered in 1945 is believed to be from 1600BC and depicts the calculation of the diagonal of a unit square whose value we now know is √2.

<--->
{{< figure src="images/greek-tablet.png" class="figs" title="" >}}
{{< /columns >}}

It is no wonder that theories in Geometry are fairly well studied and many proofs have emerged for geometric theories over the centuries. Yet, the discoveries don’t stop there as we will find out in this session. Every geometric shape has many many secrets, several of them already discovered by mankind, and several more waiting to be uncovered. All that we need to do is to keep our eyes and ears open, let the mind free to imagine and we may just stumble on something new and interesting. Let’s get started.

## What is Interesting?

Let’s first spend some time to understand what we would consider as an interesting phenomenon in geometry. Recall how we found it interesting that prime numbers can generate all other numbers, it was so interesting that it is called fundamental theorem of arithmetic. When would we consider some points interesting, or some lines interesting?

### Interesting Points

Usually a point by itself may not be that interesting. But two points are interesting in that one can draw a line connecting the two points. This was one of the very first axioms that Euclid laid out in Geometry.

{{< highlight-box "Axiom:" "none" "" "part" >}}
Any two points can be joined by a straight line.
{{< /highlight-box >}}

A lot of Geometry is built on this axiom. If someone comes along and shows us two points that cannot be joined by a straight line then the entire field of Geometry would come collapsing! Note that this is an axiom, not a theorem in that we cannot prove this. We simply assume that this is true and then build new discoveries based on that. What is also interesting is that we can draw one and only one line that connects two given points. We can try as hard as we want, but if we are given two distinct points on a plane surface, then we can only draw one line connecting them, not zero, not two, not more, one and only one. But we are not studying axioms here, so let’s move on.

When will we consider 3 points as interesting? For this, let’s do a little experiment. Let’s first form groups of 3. Then let’s take a blank piece of paper, one per group. All three of us will close our eyes, and ask the first person in the group to mark a random point on the paper. Then we pass the paper to the second person, who marks a second point randomly on the paper, eyes closed. Then we pass the paper to the third person who marks a third point on the paper, again eyes closed all the time. Now all 3 of us open our eyes and can look at the 3 points on the paper. Our goal now is to try and draw a single line that connects these 3 points. Is it possible? Is it impossible? Is it sometimes possible? 

What do we find?

{{< columns >}}
{{< figure src="images/3-points-line-1.png" class="figs" title="" >}}
{{< figure src="images/3-points-line-3.png" class="figs" title="" >}}
<--->
{{< figure src="images/3-points-line-2.png" class="figs" title="" >}}
{{< figure src="images/3-points-line-4.png" class="figs" title="" >}}
{{< /columns >}}

As we can see from the above attempts, we can draw many lines passing through the point A (the first person’s point). We can also draw many lines similarly through B and C. We have already seen that if we take points A and B together, then we can draw one line connecting the two. Similarly A and C or B and C. But it does not look like we are able to draw a single line that goes through all the three points A, B and C.

We can try this a million times. The only condition is that each person should have their eyes closed until the points are being marked, then they can open their eyes and try to draw the line. The pattern will be the same as above. Now, suppose one particular group of 3 is able to do the following:
{{< columns >}}
{{< figure src="images/3-points-line-5.png" class="figs" title="" >}}
<--->
{{< /columns >}}

All the groups are likely to exclaim “interesting”. Further, imagine this group is able to do it consistently.
{{< columns >}}
{{< figure src="images/3-points-line-6.png" class="figs" title="" >}}
<--->
{{< figure src="images/3-points-line-7.png" class="figs" title="" >}}
{{< /columns >}}

Very interesting, right?

What we are saying is that if we are able to draw a single line through 3 points, then we would consider the points as interesting. Three randomly chosen points in a plane will seldom fall on a single straight line. But if we find them falling on a straight line under certain circumstances, and further, we find them consistently falling on a straight line in those circumstances, then we will call the 3 points and hence the circumstance itself very interesting. 

{{< highlight-box "Defn 1:" "none" "" "part" >}}
If 3 points in a plane fall on a single straight line, then the points are called collinear points.
{{< /highlight-box >}}

### Interesting Lines

Now, let’s do a slightly different experiment. We can reshuffle our groups if needed, but again let’s form groups of 3. Let’s then take a blank piece of paper, and all three of us in the group close our eyes. Now, the first person can draw any random straight line on the paper. (We will give a round of applause to anyone who can draw a perfect straight line eyes closed :). Let’s assume the person has a ruler to draw the line, but with eyes closed. We pass the paper to the second person whose eyes are closed all this while, and now the second person draws a straight line on the paper. Then passes it to the third person who draws a third straight line on the paper. Then all of us open our eyes. We don’t need to do anything more.

What do we expect to find?

{{< columns >}}
{{< figure src="images/3-lines-point-1.png" class="figs" title="" >}}
<--->
{{< figure src="images/3-lines-point-2.png" class="figs" title="" >}}
<--->
{{< figure src="images/3-lines-point-3.png" class="figs" title="" >}}
{{< /columns >}}

Any group that is able to generate all three lines passing through a single point gets a round of applause. Except that they have do it consistently :)

{{< columns >}}
{{< figure src="images/3-lines-point-4.png" class="figs" title="" >}}
<--->
{{< figure src="images/3-lines-point-5.png" class="figs" title="" >}}
<--->
{{< figure src="images/3-lines-point-6.png" class="figs" title="" >}}
{{< /columns >}}

What we are saying is that if we are able to draw 3 lines such that all 3 of them pass through a single point, then we would consider the lines as interesting. Three randomly chosen lines in a plane will seldom intersect at a single point. But if we find them intersecting at a single point under certain circumstances, and further, if we find them consistently intersecting at a single point in those circumstances, then we will call the 3 lines and hence the circumstance itself very interesting. 

{{< highlight-box "Defn 2:" "none" "" "part" >}}
If 3 lines intersect at a single point, then the lines are called concurrent lines.
{{< /highlight-box >}}

### Other interesting lines, points

We would have learnt other interesting lines in school when we take 2 lines, for e.g., two parallel lines or two perpendicular lines. When these happen consistently under certain circumstances, then it usually means there is some interesting geometric phenomenon going on.

With that background, we will dive into finding interesting points and interesting lines that triangles have - three lines that surprisingly intersect at a single point, three points that surprisingly fall on a single straight line, secrets that are waiting to be uncovered.

## Interesting Points in a Triangle

The triangle is one of the most fundamental geometry shapes that mathematicians have studied. We would have studied triangles a fair bit in our regular school syllabus. The definitions of different kinds of triangles should be well known and is reproduced here merely for completion.

Based on the angles of a triangle, we categorize triangles into the well known - right angled triangle, obtuse angled triangle and acute angled triangle - shown below.

{{< figure src="images/rgh-obt-acu-triangles.png" class="figs" title="" >}}

Based on the length of the sides, we categorize triangles into the well known - equilateral triangle, isosceles triangle and scalene triangle - shown below.

{{< figure src="images/equ-iso-sca-triangles.png" class="figs" title="" >}}

Equilateral triangles, isosceles triangles and right angled triangles all have some interesting properties of their own. To uncover properties that hold for all triangles in general, we usually draw a scalene acute angled triangle to get a feel for what is happening.

It is very interesting how a triangle brings together points and lines with some very special properties. It is almost like magic.

### Medians of a triangle

A median of a triangle is a line segment joining a vertex to the midpoint of the opposite side, bisecting it. 

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/median-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Notice that D is the midpoint of side BC of the triangle. Then we draw a line from vertex A to the midpoint, D, of its opposite side, BC. This line AD is a median of the triangle.

Every triangle has exactly three medians, one from each vertex. The medians of a triangle are very special. Before we look at the medians, let’s first look at some interesting happenings with the midpoints of the sides.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/median-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

In the above △ABC, we first mark the midpoint E of side AC, then we mark the midpoint F of side AB. Now, if we draw the line joining E and F, drawn in dotted green above, it turns out to have a very interesting property. The line EF turns out to be parallel to the side BC of △ABC. Always, in any triangle!

We will prove this theorem later in the session, but we have just found out the first interesting line in a triangle. (Technically, it did not have anything to do with the medians, but it is a very interesting property of a triangle and the midpoints of the sides of the triangle).

In the above picture, we can draw two medians of the triangle to the midpoints E and F, namely BE and CF, respectively. Let’s say they intersect at a point G. This is shown below.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/median-3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Nothing interesting here so far. We know that if we draw two lines they will generally intersect at a point, unless they are parallel. But what if we draw the third median? Will that also pass through G?

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/median-4.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We find that it does! It’s almost like magic. The third median also passes through the same point. In other words, the 3 medians of a triangle are concurrent at a single point. 

Note that we are drawing a line from A to D, where D is the midpoint of side BC of the triangle. It could have easily not gone through G, remember the game we played at the beginning of the session of drawing three lines at random. If you randomly choose a point R on the side BC, the line from A to R will not pass through G. It will cut the medians from B and C at two different points. But if you choose the midpoint D, then the line from A to D magically passes through the single point G, where the other two medians had intersected.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/median-5.png" class="figs" title="" >}}
<--->
{{< /columns >}}

This point is called the triangle’s centroid. If the triangle were made of say cardboard and if we hold the cardboard triangle up with a pin at the centroid, it will balance perfectly.

### Altitudes of a triangle

An altitude of a triangle is a line segment through a vertex and perpendicular to the opposite side. There are 3 altitudes of course for a triangle, one each from each of the vertices.

Shown below are two altitudes of the triangle from the vertex B and C.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/altitude-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The question that we want to ask as before, what if we now draw the third altitude? Surprisingly, it also passes through the same point. In other words, the 3 altitudes of a triangle are concurrent!

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/altitude-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The point of concurrency of the altitudes of a triangle is called the orthocenter of the triangle.

### Angle Bisectors of a triangle

An angle bisector of a triangle is a line segment that bisects an interior angle of the triangle. There are 3 angle bisectors of a triangle, one each at each of the vertices of the triangle. 

Shown below are two angle bisectors of the triangle at vertices B and C.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/angle-bisector-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Like before, the question we want to ask is what if we draw the third angle bisector? Will it pass through the same point? By now, the surprise might have worn off. Indeed, the third angle bisector also passes through the same point. In other words, the 3 angle bisectors of a triangle are concurrent.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/angle-bisector-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The point of concurrency of the angle bisectors is called the incenter of the triangle. We will see more about the incenter in the next session.

This may start to seem like most lines drawn from vertices of triangles are concurrent. Absolutely not. We can check this with a little game. We will form groups of 3 again. This time we will take a sheet that already has a triangle drawn on it. Now, each of the members in the group can randomly (with eyes closed) mark a point anywhere on the sheet of the paper. Then we join the vertices to these random points and check if they are concurrent. We will hardly ever find them so.

{{< columns "10,80,10" >}}
<--->
{{< figure src="images/random-lines-from-vertices.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We can also try something slightly different. We can randomly pick points D, E and F on the sides of the triangle (a little hard to do with eyes closed). Then draw lines from the vertices to these points to check if they are concurrent. We will hardly ever find them so.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/random-lines-from-vertices-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

To summarize, we have found some very interesting lines and points in the triangle. The 3 medians of the triangle intersect at a single point, likewise the 3 altitudes and the 3 angle bisectors. Before going on to finding other interesting points, we will explore and prove a few properties pertaining to medians, altitudes and angle bisectors.

## Tools of the Trade

Before we start exploring interesting properties of the above points and lines, we need to equip ourselves with a few tools that will help us prove these properties. These tools are usually covered in high school geometry syllabus and so we will merely state them here with some insights.

### Congruent Triangles

{{< highlight-box "Defn 3:" "none" "" "part" >}}
Two triangles are congruent if their corresponding sides are equal in length, and their corresponding angles are equal in measure.
{{< /highlight-box >}}

{{< figure src="images/congruent-similar-triangles.png" class="figs" title="" >}}

In the triangles depicted above, the two triangles on the left are congruent, while the third is similar to them. The last triangle is neither similar nor congruent to any of the others. Congruence permits alteration of some properties, such as location and orientation, but leaves others unchanged, like distance and angles. 

In the figure below,

{{< figure src="images/congruent-similar-triangles-2.png" class="figs" title="" >}}

If someone tells us that △ABC and △DEF are congruent, and △DEF and △LMN are congruent, then we can say the following:

{{< columns >}}
{{< table "header-bold-table" >}}
| △ABC ≅ △DEF |
| :-- |
| AB = DE |
| BC = EF |
| CA = FD |
| ∠ABC = ∠DEF |
| ∠BCA = ∠EFD |
| ∠CAB = ∠FDE |
{{< /table >}}
<--->
{{< table "header-bold-table" >}}
| △DEF ≅ △LMN |
| :-- |
| DE = LM |
| EF = MN |
| FD = NL |
| ∠DEF = ∠LMN |
| ∠EFD = ∠MNL |
| ∠FDE = ∠NLM |
{{< /table >}}
<--->
{{< table "header-bold-table" >}}
| △LMN ≅ △ABC |
| :-- |
| LM = AB |
| MN = BC |
| NL = CA |
| ∠LMN = ∠ABC |
| ∠MNL = ∠BCA |
| ∠NLM = ∠CAB |
{{< /table >}}
{{< /columns >}}

Notice how we take care to write the congruence relationship between the two triangles in the correct order so that it is straightforward to write out the angles that are equal and the sides that are equal.

In order to determine if two triangles are congruent, we don’t need to show all the 3 sides and all the 3 angles to be the same. It is sufficient to check for a subset of these 6 values.

- **S-S-S test:** If three pairs of sides of two triangles are equal in length, then the triangles are congruent.
- **S-A-S test:** If two pairs of sides of two triangles are equal in length, and the included angles are equal in measurement, then the triangles are congruent.
- **A-S-A test:** If two pairs of angles of two triangles are equal in measurement, and the included sides are equal in length, then the triangles are congruent.
- **A-A-S test:** If two pairs of angles of two triangles are equal in measurement, and a pair of corresponding non-included sides are equal in length, then the triangles are congruent.

Note that AAA is not a valid test for congruence. Note also that SSA (or ASS) is not a valid test for congruence. This is depicted in the picture below.

The shape of a triangle is determined up to congruence by specifying two sides and the angle between them (SAS), two angles and the side between them (ASA) or two angles and a corresponding adjacent side (AAS). Specifying two sides and an adjacent angle (SSA), however, can yield two distinct possible triangles (source Wikipedia).

{{< figure src="images/SSA-congruence.png" class="figs" title="" >}}

### Similar Triangles

Similarity is a little different (no pun intended) from congruence. While triangles are considered congruent only if they have the same shape as well as size, two triangles are considered similar if they have the same shape even if they have different sizes.

- **A-A-A test:** If two pairs of angles of the two triangles are equal in measure, then the triangles are similar. (If two pairs of angles are equal, the third pair of angles are also equal, since we know their sum is constant.)
- **S-S-S test:** If all pairs of sides of two triangles have the same ratio, then the triangles are similar. i.e.  
if \\( \frac{AB}{DE} = \frac{BC}{EF} = \frac{CA}{FD} \\)   
then △ABC ∼ △DEF
- **S-A-S test** If two pairs of have lengths in the same ratio, and the angles included between these sides have the same measure, then the triangles are similar.

We will not dwell on trying to prove these, and we will simply look at a few problems to get an intuition of congruence and similarity.

A few problems on congruence and similarity are provided in the supplementary sheet for practice, link [here](https://docs.google.com/document/d/1qtVYbkCd-H2FqaIiivKuqIhsQXsrOO50EI1UUuxZWVc/edit).

### Miscellaneous properties

We need a few more geometric properties that will come in handy. Again, these are typically covered in school geometry, so we will simply state them here.

#### Opposite angles

When two lines intersect each other at a point, there are two pairs of angles that are equal in measure. These are shown in the picture below.
{{< columns "25,50,25" >}}
<--->
{{< figure src="images/opposite-angles.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Note how the angles that are equal are decorated in the same way. The opposite acute angles are both marked 𝝰, and the opposite obtuse angles are both marked as 𝝱.
We also know from elementary geometry that 𝝰 + 𝝱 = 180°

#### Parallel lines and transversals

When two parallel lines are intersected by a third line, this line is called a transversal and some interesting properties emerge at the points of intersection. These are shown below.
{{< columns "25,50,25" >}}
<--->
{{< figure src="images/transversal-angles.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We have already learnt that opposite angles are equal in measure. What is interesting with parallel lines is that 𝝰1 and 𝝰2 in the above picture (alternate angles) are also equal. Similarly, 𝝱1 = 𝝱2 (corresponding angles). Finally, another property that should be obvious from the above picture is that 𝝰1 + 𝝱2 = 180°, i.e. interior angles formed by the transversal within the parallel lines add up to 180°.

The converse of these statements are also true. i.e., if we find that alternate angles made by a transversal are equal, i.e. if 𝝰1 = 𝝰2, then we can say that the lines intersected by the transversal are parallel. Same holds true if 𝝱1 = 𝝱2, or if  𝝰1 + 𝝱2 = 180°.

Also note how parallel lines are marked with a little arrow on them pointing in the same direction.

#### Sum of angles of a triangle

We know well from our high school textbooks that the angles of a triangle add up to 180, i.e. 𝝰 + 𝝱 + 𝝲 = 180°.
{{< columns "25,50,25" >}}
<--->
{{< figure src="images/triangle-angles.png" class="figs" title="" >}}
<--->
{{< /columns >}}

While this is so well known to us from our school geometry, this is one of the most fascinating discoveries made by mankind. And no one knows who did it first.

Imagine the surprise of the person who discovered this by themselves. 

Whoever did it might have done something like the following, broken a triangular slab of stone probably and put the corners next to each other:
{{< columns "25,50,25" >}}
<--->
{{< figure src="images/triangle-angles-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Today, we can see the same thing by folding a piece of paper (source AMSI.au):
{{< columns "25,50,25" >}}
<--->
{{< figure src="images/triangle-angles-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

#### Area of a triangle

{{< columns >}}

The final property that we are again well familiar with from high school geometry, that the area of a triangle is half of base times height. But how did we arrive at this? 

First, we need to define what area is. We will go with the loose definition that the area of a figure is the number of unit squares that fit in the figure. So, the area of this rectangle would be 9x5 = 45.

<--->

{{< figure src="images/triangle-area-1.png" class="figs" title="" >}}

{{< /columns >}}

{{< columns >}}

{{< figure src="images/triangle-area-2.png" class="figs" title="" >}}
<--->

Now, let’s say we have a triangle that has the same base and the same height as the rectangle. How do we find the area? To find the number of unit squares that fit in will be hard. There are a number of squares that are not fully within the triangle.

Someone came up with this bright idea to measure the area of the triangle.
{{< /columns >}}

{{< columns >}}

The triangle was broken up into two parts such that each part was half of a rectangular part of the original rectangle.

The two rectangular parts together make up the full rectangle.

From this it became obvious that the area of the triangle is half the area of the rectangle containing it. Thus,

<--->

{{< figure src="images/triangle-area-3.png" class="figs" title="" >}}

{{< /columns >}}

$$ \text{Area of a triangle }= \frac{1}{2} \times b\times h $$

What is key to note is that all triangles that share the same base and have the same height, all have the same area. And triangles that lie squarely between two parallel lines all have the same height. Few examples of triangles with equal area are below.

{{< figure src="images/triangle-area-4.png" class="figs" title="" >}}

## Some Basic Properties

Now that we are well set with all the background that we need, let’s get started in real. 

We merely stated the following theorem earlier, let’s prove it now.

{{< theorem-block "Theorem" "Proof" >}}

The line joining the midpoints of two sides of a triangle is parallel to the third side. 
{{< columns "25,50,25" >}}
<--->
{{< figure src="images/basic-props-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

<--->

We are going to first show that △ABC and △AFE are similar.  
∵ F is the midpoint of AB, AB = 2.AF  
∵ E is the midpoint of AC, AC = 2.AE  
∴ \\( \frac{AF}{AB} = \frac{AE}{AC} = \frac{1}{2} \\)   
In addition, ∠CAB = ∠EAF       (They are actually the same angle)  
Hence, by SAS test of similarity, △ABC ∼ △AFE.  

∵ △ABC ∼ △AFE  
∴ ∠ACB = ∠AEF  
i.e. the corresponding angles formed by transversal EC intersecting lines EF and CB are equal.  
∴ EF || CB  

Hence proved.

{{< /theorem-block >}}

### Some properties of medians

{{< theorem-block "Theorem" "Proof" >}}

The centroid divides each of the medians in the ratio 2 : 1.
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

<--->

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We will first show that △GEF and △GBC are similar.

Since EF || CB, we know that alternate angles are congruent.  
∴ ∠GCB = ∠GFE, and
  ∠GBC = ∠GEF

We also know that opposite angles are congruent.  
∴ ∠BGC = ∠EGF

∴ △GEF ∼ △GBC  
We have just shown that △ABC and △AFE are similar. And also that the sides of these two triangles are in the ratio 1:2.  
∴ \\( \frac{EF}{CB} = \frac{AF}{AB} = \frac{AE}{AC} = \frac{1}{2}  \\)

Now, from similar triangles △GEF and △GBC  
∴ \\( \frac{GE}{GB} = \frac{GF}{GC} = \frac{EF}{BC} = \frac{1}{2} \\) 

∴ The median CF is divided in the ratio 2:1 by the centroid G. Similarly, median BE. And can show the same for median AD.

Hence proved.

{{< /theorem-block >}}




{{< theorem-block "Theorem" "Proof" >}}

The 3 medians divide a triangle into 6 parts with equal areas.
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-4.png" class="figs" title="" >}}
<--->
{{< /columns >}}

<--->

First, lets draw median AD, and look at △ADC and △ADB.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-5.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Are they similar triangles? Are they congruent?? Neither!!!

It turns out they have equal areas.

|△ADB| = ½ . DB . AK    
|△ADC| = ½ . DC . AK   
∵ DB = DC   
∴ |△ADB| = |△ADC|   
(Note that |△ADB| is the notation for area of triangle ADB)

Notice now that we can say the same thing about △CGD and △BGD as shown here. They have the same height, and their base length is the same. Hence their areas are same too.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-6.png" class="figs" title="" >}}
<--->
{{< /columns >}}

And now the most interesting part of the proof.  

∵ |△ADB| = |△ADC| and  
∵ |△BGD| = |△CGD|  

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-7.png" class="figs" title="" >}}
<--->
{{< /columns >}}

∴ |△AGB| = |△AGC|  

Now, AGB and AGC are in turn made of two triangles of equal area.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-8.png" class="figs" title="" >}}
<--->
{{< /columns >}}

|△AGE| = |△CGE| = ½.|△AGC|   
|△AGF| = |△BGF| = ½.|△AGB|

∴ |△AGE| = |△CGE| = |△AGF| = |△BGF|

We have shown four of the triangles to have equal areas. It is a simple matter to show the remaining two as well.
.  
.  
.  
.  
.  
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

{{< columns "85,15" >}}
Most of these theorems are age old, dating to Euclid’s time, some probably earlier. So, it was amazing when a simple congruence theorem was put forth by a British Engineer, Lee Sallows, in the year 2014.

He discovered an interesting property of the 6 triangles above - that if pairs of them are joined together, then we get 3 congruent triangles. It is also fairly easy to prove.
<--->
{{< figure src="images/basic-props-9.png" class="figs" title="" >}}
{{< /columns >}}

{{< theorem-block "Theorem" "Proof" >}}

{{< figure src="images/basic-props-10.png" class="figs" title="" >}}

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
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
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

What is interesting is the fact that this property has been unnoticed until very recently. Wonder what other secrets lie hidden in triangles with their interesting lines and points.

### A property of altitudes

{{< theorem-block "Theorem" "Proof" >}}

The product of the lengths of the segments that the orthocenter divides an altitude into is the same for all three altitudes.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-11.png" class="figs" title="" >}}
<--->
{{< /columns >}}

AH.HD = BH.HE = CH.HF

<--->

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-12.png" class="figs" title="" >}}
<--->
{{< /columns >}}
.  
.  
.  
.  
.  
.  
.  
.  
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

### A property of angle bisectors

{{< theorem-block "Theorem" "Proof" >}}

An angle bisector of an angle of a triangle divides the opposite side in two segments that are proportional to the other two sides of the triangle.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-13.png" class="figs" title="" >}}
<--->
{{< /columns >}}

\\( \frac{AC}{CD} = \frac{AB}{BD} \\)

<--->

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-14.png" class="figs" title="" >}}
<--->
{{< /columns >}}
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
{{< columns "20,60,20" >}}
<--->
{{< figure src="images/basic-props-15.png" class="figs" title="" >}}
<--->
{{< /columns >}}
.  
.  
.  
.  
.  
.  
.  
.  
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

## CEVA's Theorem

We have now seen a few instances of concurrent lines in a triangle. The medians are concurrent, the altitudes are concurrent, the angle bisectors are concurrent.

Concurrent lines originating from the vertices of a triangle have an interesting property that carries the name of a 17th century Italian mathematician, Giovanni Ceva and is called Ceva’s theorem. But it was later found that the theorem was also known and proved by an 11th century king of the small kingdom of Zaragoza in Spain!

{{< theorem-block "Theorem" "Proof" >}}

If lines drawn from the vertices of a triangle are concurrent at O, 

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/ceva-theorem-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

then the following relation holds true:  
\\( \frac{AF}{FB} \cdot \frac{BD}{DC} \cdot \frac{CE}{EA} = 1 \\)

<--->

We have seen before that  
\\( \frac{|△ABD|}{|△ADC|} = \frac{BD}{DC} \\)

Likewise,  
\\( \frac{|△OBD|}{|△ODC|} = \frac{BD}{DC} \\)

From this it follows that (Think about this, why is this true?)  
\\( \frac{BD}{DC} = \frac{|△ABD| - |△OBD|}{|△ADC| - |△ODC|} = \frac{|△AOB|}{|△AOC|} \\)

Similarly,  
\\( \frac{AF}{FB} = \frac{|△AOC|}{|△BOC|} \text{ and } \frac{CE}{EA} = \frac{|△BOC|}{|△AOB|} \\)

Therefore,  
\\( \frac{AF}{FB}\cdot \frac{BD}{DC}\cdot \frac{CE}{EA} = \frac{|△AOB|}{|△AOC|}\cdot \frac{|△AOC|}{|△BOC|}\cdot \frac{|△BOC|}{|△AOB|} = 1 \\) 

Hence proved.

{{< /theorem-block >}}

The converse is also true, namely if we have three points on the sides of the triangles which satisfy the above property, then the lines from the vertices of the triangle to these points will all be concurrent. This is a little more tricky to prove.

## Secret Points in a Triangle

Now, let’s look at some other very interesting points in a triangle. 

### Fermat point

Let’s take a triangle and draw equilateral triangles on the sides of a triangle. Then connect the vertex of the original triangle to the opposite vertex of the equilateral triangle on the opposite side. It turns out that these 3 lines are concurrent!

{{< columns "0,100,0" >}}
<--->
{{< figure src="images/fermat-point.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The intersection point F is also called the Fermat point after the French mathematician. Yes, the same Fermat from Fermat’s little theorem we saw in the session on congruences.

It turns out that Fermat posed the following problem to Italian physicist and mathematician Evangelista Torricelli in a private letter (in the early 1600s) - find the point in a triangle such that the total distance from the point to the three vertices of the triangle is the minimum possible. Torricelli solved the problem, and in a slightly different way that Fermat himself had solved it. So the point is also called Fermat-Torricelli point sometimes. 

Torricelli, BTW, happens to be the inventor of the barometer. 😎

The Fermat point has another interesting property. If we look carefully at the construction, we notice that the angle subtended by the sides of the triangle at F are all equal. That is,

∠AFB = ∠BFC = ∠CFA

The Fermat point has some other interesting properties as well, and we will revisit it in the next session.

### Napoleon Triangle

What if we draw lines from the vertices of the original triangle to the centroids of the equilateral triangles. It turns out that these are also concurrent!

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/napolean-triangle-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

But there are some more interesting properties, some secrets hiding here. 

Firstly, the centroids of the equilateral triangles form a new equilateral triangle. This triangle is called Napoleon’s triangle, after the French military leader. It is not very clear if he did discover and/or prove this theorem. But the triangle nevertheless has his name attached.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/napolean-triangle-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

More interestingly, the centroid of this new equilateral triangle coincides with the centroid of the original triangle. And this holds true for any original triangle, note that the original triangle itself was any scalene triangle.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/napolean-triangle-3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

We can also draw equilateral triangles on the sides of the original triangle facing inwards. Then find the centroids of those equilateral triangles, and join them, and then find the centroid of that triangle, and compare this centroid to the centroid of the original triangle. 😎😎

Well, that is called the inner Napoleon triangle and is shown below. What is interesting is that the inner Napoleon triangle is also an equilateral triangle, and its centroid also coincides with the centroid of the original triangle.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/napolean-triangle-4.png" class="figs" title="" >}}
<--->
{{< /columns >}}

### Squares on the sides

Suppose we draw squares on the sides of a triangle. Then connect the center of each of the square to the opposite vertex of the triangle. Where will the 3 lines intersect?

Lo and behold, the lines are concurrent!

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/squares-on-triangle-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Let’s try something a little different in these same circumstances. Let’s draw lines from each vertex of the triangle to the midpoint of the far edge of the square. What do we expect? Indeed, they are all concurrent. 

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/squares-on-triangle-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

This may give us a false impression that all these kinds of lines are concurrent. But they are not. These are not concurrent for example.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/squares-on-triangle-3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

Here’s another interesting one. We draw squares on the triangle, then draw triangles on the squares such that the sides of these triangles are parallel to the original triangle.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/squares-on-triangle-4.png" class="figs" title="" >}}
<--->
{{< /columns >}}

And yet another. We introduce parallelograms between the squares and suddenly see a number of concurrent lines show up. Two of them are shown below.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/squares-on-triangle-5.png" class="figs" title="" >}}
<--->
{{< /columns >}}

## A Secret Line in the Triangle

All the examples we have seen so far are groups of 3 lines that turn out interesting because they are all concurrent at a point. Finally, let’s look at an example of collinearity in the triangle - a group of 3 points that fall on the same line.

### The circumcenter

But before we do that, let’s familiarize ourselves with one more very important point in the triangle - the circumcenter. The circumcenter is the point of intersection of the perpendicular bisectors of the sides of a triangle. 

The perpendicular bisector of a line segment is the perpendicular line that also bisects the given line segment, in other words, it passes through the midpoint of the line segment and is at right angles to it.

{{< columns "25,50,25" >}}
<--->
{{< figure src="images/circumcenter.png" class="figs" title="" >}}
<--->
{{< /columns >}}

The circumcenter has this nice property that it is equidistant from the vertices of the triangle. In the above picture, it should be obvious that △OBD ≅ △OCD. Hence OB = OC. Likewise OC = OA and OA = OB. Hence OA = OB = OC.

We will work a lot more with the circumcenter in the next session.

### EULER's line

Euler found a remarkable relation between three important points of a triangle - the median, the circumcenter and the orthocenter. Euler was about 60yrs old when he published this theorem and what exceeded the beauty of the finding was the simplicity of the proof.

{{< theorem-block "Theorem" "Proof" >}}

The centroid, the circumcenter and the orthocenter of any triangle are collinear.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/euler-line-1.png" class="figs" title="" >}}
<--->
{{< /columns >}}

<--->

The proof starts elegantly. 

Let the line joining the circumcenter O and the centroid G intersect the altitude at X. Euler then goes on to show that X is the same as H, the orthocenter. 

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/euler-line-2.png" class="figs" title="" >}}
<--->
{{< /columns >}}

∵ OD and AX are both perpendicular to BC,  
∴ OD || AX (corresponding angles)

∴ △AGX ∼ △DGO by AAA  
(alternate angles, opposite angles)

∵ Centroid G divides the median in the ratio 2:1  
∴ \\( \frac{OG}{XG} = \frac{DG}{AG} = \frac{1}{2} \\)

<br/>
Next, let’s look at △OGF and △XGC.  

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/euler-line-3.png" class="figs" title="" >}}
<--->
{{< /columns >}}

∵ Centroid G divides the median in the ratio 2:1  
∴ \\( \frac{FG}{CG} = \frac{1}{2} \\)  

From above, \\( \frac{OG}{XG} = \frac{1}{2} \\)   

And ∠OGF = ∠XGC, opposite angles.

∴ △OGF ∼ △XGC by SAS

<br/>
∴ ∠OFG = ∠XCG  
∴ OF || CX, since alternate angles are equal

∵ OF is perpendicular to AB  
∴ CX will also be perpendicular to AB.

∴ CX is the altitude from C.  
∵ CX and AX intersect at X,  
∴ X is the orthocenter.

Hence proved.

{{< /theorem-block >}}

Euler’s line has one very interesting point that also lies on it, and we will explore that point in the next session.

## Summary

We have seen a few interesting points and lines, many more of them have been discovered to the great joy of those who found them, and certainly many more remain waiting to be discovered. 

These are all secrets hidden within the triangle, for anyone who would like to go on a treasure hunt here. 

Happy hunting!!! 😎😎😎
