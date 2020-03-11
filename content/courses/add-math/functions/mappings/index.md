---
title: "Mappings"
date: 2020-01-21T06:57:11+05:30
draft: false
weight: 2
---

## Definition

Now that we have looked at sets in fair amount of detail, we can start doing some interesting math when we take two sets and start relating the elements in one set to the elements in the other.

{{< highlight-box "Defn 1:" "none" "" "part" >}}
A **Mapping** is simply a rule that connects elements of one set to the elements of another set.
{{< /highlight-box >}}

Note that implicit in the defintion is notion of a first set whose elements are connected or mapped to the elements on the other set, the second set.

An example will help understand this idea. Imagine a team game such as soccer or basketball or Ultimate frisbee. Usually, when you line up as part of your team, your captain will have a chat on the strategy to pursue. When you are in defence, a common strategy to pursue in many of these team games is called man-to-man marking. Each of the members in your team decide which player of the opposing team to mark.

As you can imagine, your team can be considered as one set and the opposing team as the second set. And the rule that you guys come up with to mark each member of the opposite team naturally fits itself as an example of a mapping.

We can depict this pictorially as shown below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/mapping man-on-man v1.png" class="figs" title="A mapping of members of the home team H to the members of the opposing away team A in a man-to-man marking strategy" >}}
<--->
{{< /columns >}}

### 1-to-1 mapping

This above mapping is called a 1-to-1 mapping. In this mapping whenever an element of the first set is mapped to an element of the second set, it is mapped to *one unique* element of the second set.

Don't be misled by the straight lines in the mapping above. The picture below is yet another example of a valid 1-to-1 mapping.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/mapping man-on-man v2.png" class="figs" title="Another example of a 1-to-1 mapping" >}}
<--->
{{< /columns >}}

It is not necessary that all elements of the first set are mapped to elements of the second set. For e.g., in a game such as soccer, the goalkeeper typically does not mark any other person and remains at the goal post. This is depicted in the mapping below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/mapping man-on-man v3.png" class="figs" title="Another example of a 1-to-1 mapping, with some unmapped elements" >}}
<--->
{{< /columns >}}

The key point to note is that any element of the first set that is mapped to the second set should map to a unique element of the second set. This definition does allow for elements that are not mapped at all as in the example above.

Just to be clear and re-iterate the definition of a 1-to-1 mapping, the following conditions should be satisfied:

- each element of the first set that is mapped to an element of the second set should map to only one element of the second set. No element should map to more than one element.
- no two elements of the first set should map to the same element of the second set. Each element should map to a separate unique element.
- both of these conditions imply that if an element of the first set is mapped to an element of the second set, it should map to *one unique* element of the second set.

### 1-to-many mapping

Imagine a situation where a player of your team is injured or worse a player gets a timeout for foul play, and lets say your team has lesser players on the field compared the opposition. In this situation, one of your team members will have to mark more than one of the opponents. As you can imagine, this would no longer be a 1-to-1 mapping. This is called a 1-to-many mapping, and is depicted pictorially below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/mapping man-on-man 1-to-m.png" class="figs" title="An example of a 1-to-m mapping" >}}
<--->
{{< /columns >}}

Notice that for a mapping to be called 1-to-many (sometimes abridged as 1-to-m mapping), it is sufficient even if one of the elements of the first set is mapped to more than one element of the second set, while all the other elements each map to unique elements. As before, there can be elements in the first set that are not mapped.

### many-to-1 mapping

The third type of mapping is one where multiple elements of the first set all map to the same element of the second set.

In professional soccer for many years now, man marking is a thing of the past. Zonal marking is the most commonly followed strategy when in defensive mode.

To depict this strategy as a mapping, the first set is again our team, and the second set is now zones of the field. Suppose we consider the field split into three zones. Each of the players in our team would be alloted to one of the zones as shown below.

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/mapping zonal.png" class="figs" title="An example of a m-to-1 mapping" >}}
<--->
{{< /columns >}}

In this method of marking, when the action gets into your zone of the field with an opponent getting into that zone with the football (or frisbee, etc), then you start tackling that opponent. As before, there can be elements in the first set that are not mapped.

### many-to-many mapping

To understand many-to-many mapping, we will consider a different example. Suppose the first set is the set of all teachers in your school, and the second set is the set of all students. The mapping we are interested in is a parent to child mapping, i.e., we connect a teacher from the first set with his/her children if they are studying at the same school.

The picture of this mapping would looks omewhat like below:

{{< columns "20,60,20" >}}
<--->
{{< figure src="images/teacher-student parent-child mapping.png" class="figs" title="An example of a m-to-m mapping" >}}
<--->
{{< /columns >}}

The following points may be noted about the mapping depicted above:

- Teacher T1 has one child S1 studying in the school. The same is true with teacher T2 and student S2. Both these connections are of the 1-to-1 nature.
- The parent of student S3 is not a teacher in the school, hence there is no connection to this student in this mapping.
- The teachers T3 and T4 both have one child, the same child S4, who is a student in the school. Presumably they are the mother and father of this student. The connection from T3 and T4 to the single student S4 is of the many-to-1 nature.
- Teacher T5 does not have any student studying in the school. Likewise students S5 and S6 do not have any of their parents as teachers in the school.
- Finally, teach T6 has 3 children studying in the school as shown by the 1-to-many connections from T6 to the students S7, S8 and S9.
- Teacher T7 does not have any children in the school, and neither of the parents of student S10 teach in the school.

As you can probably make out from these connections, this particular mapping does not fit the definition of any of the mapping types that we discussed earlier. It is not 1-to-1, not 1-to-m and not m-to-1 either. It looks like some combination of all three of these.

More specifically, if a mapping contains some connections which are of the 1-to-m kind and some connections which are of the m-to-1 kind, then the mapping is called a many-to-many mapping. Notice that 1-to-1 connections or elements of either set that are not mapped do not change the nature of the mapping. It is simply the presence of both 1-to-m connections and m-to-1 connections that make the mapping a m-to-m mapping.

With that we conclude our exploration of mappings.

## Marking strategies

Before we move on to one of the most important topic in Mathematics, that of functions, a little bit of detour may not harm us much.

Check out this cute video on marking strategies in soccer.

{{< youtube id="BLMhylkO2eo" >}}

A wonderful saying from the video is this - "The perfect game of football would end 0 - 0". No wonder football is often called the beautiful game, or *o jogo bonito* in Portuguese.
