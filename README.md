# treeQ
A q/kdb+ library to convert a normalized table to a tree structure

# `tree` Function 

It takes 2 arguments :
* Normalized table
* Path of the tree to be constructed 

Sample Code :

    q)data:flip `l1`l2`l3`l4!("aaaaaaaaaaaaa";"bbffjjjjjssww";"ccggkknppttxx";"dehilmoqruvyz");
    q)tree[data;`l1`l2`l3`l4]
    
    q)-1_1_.j.j tree[data;`l1`l2`l3`l4]
    {"name":"a","children":[{"name":"b","children":[{"name":"c","children":[{"l4":"d","name":"d"},
     {"l4":"e","name":"e"}]}]},
     {"name":"f","children":[{"name":"g","children":[{"l4":"h","name":"h"},
     {"l4":"i","name":"i"}]}]},
     {"name":"j","children":[{"name":"k","children":[{"l4":"l","name":"l"},
     {"l4":"m","name":"m"}]},
     {"name":"n","children":[{"l4":"o","name":"o"}]},
     {"name":"p","children":[{"l4":"q","name":"q"},
     {"l4":"r","name":"r"}]}]},
     {"name":"s","children":[{"name":"t","children":[{"l4":"u","name":"u"},
     {"l4":"v","name":"v"}]}]},
     {"name":"w","children":[{"name":"x","children":[{"l4":"y","name":"y"},
     {"l4":"z","name":"z"}]}]}]}


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
