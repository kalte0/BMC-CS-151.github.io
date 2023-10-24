---
layout: default
title: "Binary Trees"
type: Lab
number: 07
active_tab: lab
release_date: 2023-10-25

---

<!-- Check whether the assignment is ready to release -->
{% capture today %}{{'now' | date: '%s'}}{% endcapture %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% if release_date > today %} 
<div class="alert alert-danger">
Warning: this assignment is out of date.  It may still need to be updated for this year's class.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}
<!-- End of check whether the assignment is up to date -->


<!-- Check whether the assignment is up to date -->
<!--{% capture this_year %}{{'now' | date: '%Y'}}{% endcapture %}
{% capture due_year %}{{page.due_date | date: '%Y'}}{% endcapture %}
{% if this_year != due_year %} 
<div class="alert alert-danger">
Warning: this assignment is out of date.  It may still need to be updated for this year's class.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}-->
<!-- End of check whether the assignment is up to date -->



{% if page.materials %}
<div class="alert alert-info">
You can download the materials for this assignment here:
<ul>
{% for item in page.materials %}
<li><a href="{{item.url}}">{{ item.name }}</a></li>
{% endfor %}
</ul>

</div>
{% endif %}





{{page.type}} {{page.number}}: {{page.title}}
=============================================================
You will be submitting this lab to Gradescope. 

## Objectives:

The main goals for this lab are:
1. Get practice with binary trees
1. Get more practice using checkstyle, JUnit, and implementing an interface


### Paired Programming rules
This lab is a **paired programming assignment.** What exactly does that mean? 
You will be working in pairs on the CS lab computers. Each pair will be working on one computer. One person will be the **driver** and the other person
 will be the **navigator**. Here is the rule: the **driver** controlls the lab computer, but the **driver** can only type what the **navigator** tells 
them to type. For this to work well, each pair should be constantly talking 
among themselves. After each problem, you will switch roles, the navigator will become the driver and the driver will become the navigator.


## Exercise 1 - LinkedBinaryTree

Download the `LabBinaryTree` interface from 
<a href="{{ site.url }}{{ site.baseurl }}/labs/lab07/LabBinaryTree.java">{{ site.url }}{{ site.baseurl }}/labs/lab07/LabBinaryTree.java</a>

Implement a `LinkedBinaryTree` that implements `LabBinaryTree`.
Start with the methods `size`, `isEmpty`, `insert`,
and `toString`, which creates a string representation
of the tree by traversing through the nodes
of the binary tree in in-order traversal order.
`insert` allows you to add to the tree and `toString()` allows
you to check the contents of your tree.

Note that the interface requires that all listed methods be 
implemented, but for now you can just implement method stubs for 
the remaining methods
and come back to them later in the lab.

## Exercise 2 - Testing
In a file called `TestLinkedBinaryTree.java`,
write JUnit tests test your methods. 
Remember to thorougly test each method. 

## Exercise 3 - `contains` and `height`
Proceed with implementing and testing `contains` and `height`.
Then, write JUnit tests in `TestLinkedBinaryTree.java` to 
make sure they work correctly.

# Summary

In this lab we covered binary trees. You gained more experiece using
checkstyle, unit testing, and implementing an interface.

### Signing out
You do not need to be signed out by a TA for this lab. You will be submitting
your code on Gradescope.

Remember, your code **must** pass the checkstyle.

Files to submit include:
- `LinkedBinaryTree.java`
- `TestLinkedBinaryTree.java`
