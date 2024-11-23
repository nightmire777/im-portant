
> [!WARNING]
> notes may contain issues or unfinished sections, pls read with caution

# THEORY BULLLSHIT 

## Wat is a Data structure
An organization of information, a certain way a data is stored so that it can be used efficiently in algorithms and calculations

*Atomic data*

- Single data or scalar data
- like an ATOM cannot be broken down further 
- Ex: integer 69 42 

*Composite data*

- data that can be broken down further
- GenshinAccount record can be further broken down to UID, Characters, Rank, Username, server
- can be implemented in c++ with struct and (class?)
- structured data

## data types
*simple* :  integral(char,short,long,int) floating (float,double, long double)

*structured* : arrays, struct, class, union

A data structure is combination of elements consisting of atomic and/or composite data 

*abstract data type *

maybe abit like abstraction from OOP or like the header file???
includes declaration of data, implementations of operations and encapsulations op the data and its operations. 

## measuring effeciency
A good algorithm should balance between time and space effeciency

> compt flashabacks
effeciency can be measured using big O complexity O(n)

best case complexity > minimum number of steps on any instance of n 

worst case > max number of steps ... you get it 


average case > 


# Queue (rank
A queue is a list of  homogeneous elements

FIFO first in first out
> when adding data(enqueue), only can add at the back, when taking out data(dequeue), can only take oout from front. Middle elements cant be accessed.

*real world applications*
- bank reception 
- reservations systems
- anything witha  first come first serve concept
>sometimes in life, FIFO just cant work like in hospital emergency room for example... 
>
>Therefore we have priority queue 

*ways to represent queue*

>using 1d arrays

Implementation should have: 

- an array to store the elements 
- qfront variable ( used to keep trac of the front of the array)
- qrear variable to keep track of the back of the queue
- maxqsize variable to set a maximum size for the queue if needed. 

However this method may not be the best method

- array size is fixed
-  array implementation of queue requires it to be treated differently (circular)

**solution**

When the queue start reaches the end, shift all elements which kinda suck cuz its slow if the array is huge. 

EX: lets say an array of max 5 items
- maxqsize =5
- qfront = -1
- qrear = 0

```
now we start with adding c f a u 
so the values become:
- maxqsize = 5
- qfront = 1
- qrear = 4
[c,f,a,u]

then you remove c from array and. It becomes:
[c,f,a,u]
- maxqsize = 5
- qfront = 2
- qrear = 4

then you add n to array, it suddenly becomes full cuz maxqsize = qrear
BUT IS IT ACTUALLY FULL?
[c,f,a,u,n]
- maxqsize = 5
- qfront = 2
- qrear = 5
```

So if the queue reaches the end, we move all elements forward

Another way is can use a circular array. 

which basically is the back element will come all the way back to the front (like human centipede)

>using linkedlist

Its honestly way easier and better and its dynamic

just q the nodes in one by one then all is good



# stacks

# tree
hierarchically organizaing data(file system, family tree,game lore, anything with **ancestors and decendants**)

## wat is a tree
a tree is only a set of nodes connected by edges to form a hierarchical relationship 

- top level is root 
- like a family tree, nodes after another are called children
- nodes with same parents is called siblings 
- node with no children (me) are called leaves

- tree height is the number of levels 

- depth is how the furthest leaf is from the root

- node degree: number of kids 

- tree degree: max degree across the entire tree


## binary tree

- each node max 2 kids
- the kids are L and R 

### complete tree

### full tree 
>everynode either have 0 or 2 kids 
>full tree with heigh H have (2^h)-1 nodes , includes root and leaves

# Graphs
Its a data structure that has a set of nodes that relate to one another

The nodes are linked using edges, these edges describe the relationships among the vertices


**uses** 
- electrical circuits
- network communications 
- finding shortest route
- searching for dependency




































