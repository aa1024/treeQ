# treeQ
A q/kdb+ library to convert a normalized table to a tree structure

# `tree` Function 

It takes 2 arguments :
* Normalized table
* Path of the tree to be constructed 

Sample Code :

    q)data:flip `l1`l2`l3`l4!("aaaaaaaaaaaaa";"bbffjjjjjssww";"ccggkknppttxx";"dehilmoqruvyz");
    q)tree[data;`l1`l2`l3`l4]

Table :

    l1 l2 l3 l4
    -----------
    a  b  c  d
    a  b  c  e
    a  f  g  h
    a  f  g  i
    a  j  k  l
    a  j  k  m
    a  j  n  o
    a  j  p  q
    a  j  p  r
    a  s  t  u
    a  s  t  v
    a  w  x  y
    a  w  x  z

Converted to Tree structure :

![](tree.png?raw=true)
