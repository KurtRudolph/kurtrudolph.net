---
layout: post
title: "Tree of Scope"
description: "A short wisdom piece"
category:
tags: ['hacker', 'wisdom']
---
{% include JB/setup %}

The following is a short wisdom piece passed along to me
by a professor at UIUC and originally written by a former
students of his after one of their discussions:

## Tree of Scope
Imagine a binary tree that represents all the requirements 
that a product or feature needs to fulfill. At the root, is 
the tree that says that this things should solve every 
problem on the face of the earth. As you go down, you 
reduce scope and generality.
You can define the scope of your problem as the tree rooted 
at a particular node. The leaves are the 
eventualities/requirements that this feature or product needs to fulfill.
A candidate that examines the problem at a node higher 
up in the tree is too academic and will not produce a useful 
solution in any reasonable amount of time.
A candidate that works at a node that is further down in 
the tree does not understand the full problem. Their solution 
is not general enough and will not be able to cope with additional 
requirements. This solution doesn't actually "solve" the problem, 
but just meets the requirements at hand and only those. 
It does not take into account future scope or refactoring.

![Tree Image](http://www.templates.com/blog/wp-content/uploads/2012/08/Create-Binary-Trees-Using-JavaScript-HTML5-Canvas.jpg)
