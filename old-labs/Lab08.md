---
layout: default
title: "Array based Binary Trees & Heaps"
type: Lab
number: 08
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


## Exercise 1 - ArrayBinaryTree
Download the `LabBinaryTree` interface from 
<a href="{{ site.url }}{{ site.baseurl }}/labs/lab08/LabBinaryTree.java">{{ site.url }}{{ site.baseurl }}/labs/lab08/LabBinaryTree.java</a>


Design and implement `ArrayBinaryTree` that 
implements `LabBinaryTree`. 
Note that different from last week's lab and homework 05,
this is now an array-based binary tree. 

Also note that you only need
to implement a binary tree, not a binary search tree (in the sense that each node can have
max two children, but no ordering of any kind is enforced, between the parent/children, or
among the siblings). Think about what instance variables you will need.

Start with the methods `size` and `isEmpty`. 
Implement the suggested helper methods below
before moving onto `insert` and 
`toStringBreadthFirst`, 
which prints out the elements of
the binary tree in breadth first traversal order (layer-by-layer). Breadth-first traversal should be straight forward
when you have an array-based binary tree.


1. `int parent(int i);` - returns the index of the parent of child stored at i
2. `int left(int i);` - returns index of left child of parent stored at i
3. `int right(int i);` returns index of right child of parent stored at i
4. `void swap(int i, int j);` - swaps the two nodes stored at indices i and j
5. `int containsIdx(E element);` - returns the index of the node containing element 


###  Testing
In a file called `TestArrayBinaryTree.java`,
write JUnit tests test your methods. 
Remember to thorougly test each method. 

Then, in `ArrayBinaryTree.java`,
write a main method where you create an
`ArrayBinaryTree<Integer>` object
and insert the integers 1-20 into the tree.
Use the `toStringBreadthFirst()` method
to print out the object. 

### Remove & getRootElement
Proceed with implementing `getRootElement` and `remove`. Note that an artibrary
binary tree is not guaranteed to be complete (the user may execute remove on any element
at any time) and you need to decide how handle the case where positions may become null
through out your tree. Hint: use `swap`

Make sure to add JUnit tests that sufficiently test `getRootElement` and `remove`.

## Exercise 2 - ArrayHeap
Download the `LabPriorityQueue.java` interface from 
<a href="{{ site.url }}{{ site.baseurl }}/labs/lab08/LabPriorityQueue.java">{{ site.url }}{{ site.baseurl }}/labs/lab08/LabBinaryTree.java</a>

Implement `ArrayHeap` that extends `ArrayBinaryTree` and 
implements `LabPriorityQueue`. Start with overriding `insert` so
that elements can be inserted in heap order.

Proceed with implementing peek().

Make sure to write JUnit tests that sufficiently test the new methods
in `ArrayHeap`.

This is not required for lab, but think about how remove should be overidden to maintain
heap order, and how you will implement poll.

# Summary

In this lab we covered array implementations of binary trees
and binary heaps. 

### Signing out
Before leaving, make sure your TA/instructor have signed you out of the lab. If you finish the lab early, you are free to go.
If you do not finish the lab in time, you will need to go to office hours so
that a TA can check your work.
