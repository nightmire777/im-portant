
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

# Linked List
- Collection of items in list data structure, can be stored and organized in memory

- List data structure: abstract type linear structure with sequence of elements

- Contains many nodes which are connected. 

- Each node has data and the address(pointer) of the next node 

- head is the address of the starting node

- the last node will have the next node's address as null 


`Arrays +-`

+fast access to random elements

+easy to use and code

-fixed size, costly to change 

-insert and delete are slow

`LinkedList +-`

+dynamic size (no need declare at start)

+can add or remove easily from middle

+no size limit

# Operations 

determine size

insert item 

search 

get item

delete

## creating the structure
each "data" to be inserted into a linked list need to become a node 

each node would have data and the address of the next node

```
class LinkedList { 
 public: 
   NodeType* head; 
   LinkedList();
   int getSize();
};

```
## Traversal
example of printing all elements
```
node *current = head;
while (current->next != nullptr){
	cout << current->next->info;
}

```

## getting list size 
```
//code to calculate size as it goes
int size =0 ;
node *current = head;
while (current->next !=  nullptr){
	size++;
	current = current->next;
}
//return size
int getSize(){
	return size;
}
```

## Inserting new element infront
```
void insert(node*& head, int data){
	node *newnode = new node; //create the new node
	newnode->info = data; //put data into the new node 
	newnode->next = head; //change the new node next node into head
	head = newnode; //make new node the new head
	size++; //increase the list size
}
```
## Inserting new element infront
```
void insertRear(node*& head, int data) { 
	node* newnode = new node(id);
	if (head == nullptr) {
		head = newnode;
	}
	else {
		node *current = head; 
		while(current->next != nullptr){
			current = current->next;
		}
		current->next = newnode;
		newnode->next = nullptr;
	}
}
```

## cleaning up
```
void deleteAll(){
   NodeType * current = head;
   while(head != NULL){
	current = current->link;
	delete head;
	head = current;
   }
}
```

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

# Graph

What :  A graph is a collection of nodes (or vertices) connected by edges. 

```
Vertices (Nodes): The individual elements of the graph.
Edges: The connections between the vertices.
Directed Graph: A graph where edges have a direction (e.g., A → B).
Undirected Graph: A graph where edges do not have a direction (e.g., A -- B).
Weighted Graph: A graph where edges have weights (e.g., distances or costs)
Degree of vertex: The degree of a vertex is the number of edges connected to it. In directed graphs, we differentiate between in-degree (incoming edges) and out-degree (outgoing edges).
Connected Graph:  A graph is connected if there is a path between every pair of vertices. In directed graphs, it is strongly connected if there is a directed path in both directions between every pair of vertices.
```

## Directed Graph VS Undirected Graph
In a directed graph, edges have a direction, indicating a one-way relationship. In an undirected graph, edges do not have a direction, indicating a two-way relationship.

Example 
A directed graph could represent a Twitter following (User A follows User B), while an undirected graph could represent a Facebook friendship (User A is friends with User B).

### Directed
Applications: Computer networks, Project management, family tree, dependencies 

- +can model complex relationships, good for representing dependencies, Can be used for analysis
- -May be more complex, require more processing power

### Undirected
Applications: Social Networks, Traffic flow optimization, Website analysis(linkage between websites)

- +simple and easy, less computing power, flexible
- -no direction, limited info

## traversals 
Graph traversal refers to the process of visiting all the vertices in a graph.

Depth first traversal : Explores as far as possible along each branch before backtracking. It uses a stack (either explicitly or via recursion).
Breadth first traversal : Explores all neighbors at the present depth prior to moving on to nodes at the next depth level. It uses a queue.
Comparison: DFS can be more memory efficient for deep graphs, while BFS is better for finding the shortest path in unweighted graphs.

## Dijkstra's algorithm 
finds the shortest path from a source vertex to all other vertices in a weighted graph.

Steps:
Initialize distances from the source to all vertices as infinite, except for the source itself (distance = 0).
Mark all vertices as unvisited. Set the source vertex as the current vertex.
For the current vertex, consider all its unvisited neighbors and calculate their tentative distances. Update the distance if the new distance is smaller.
Once all neighbors are considered, mark the current vertex as visited. A visited vertex will not be checked again.
Select the unvisited vertex with the smallest tentative distance as the new current vertex and repeat until all vertices are visited.
Example: Given a graph with vertices A, B, C, and D, and edges with weights, the algorithm will iteratively update the shortest paths from A to all other vertices.

## Minimum spanning tree
A minimum spanning tree (MST) is a subset of edges in a weighted graph that connects all vertices with the minimum total edge weight and without any cycles. A cycle is when the graph have loops. 

Prim's Algorithm: Starts with a single vertex and grows the MST by adding the smallest edge that connects a vertex in the MST to a vertex outside the MST.
Kruskal's Algorithm: Sorts all edges in ascending order by weight and adds edges to the MST, ensuring no cycles are formed, until all vertices are connected.

# Trees and binary search 
what :A tree is a set of nodes connected by edges to indicate a hierarchical relationship among the nodes

```
Nodes are arranged in levels 
Top level is a single node called the root
Nodes at a given level are children of nodes of the previous level
A node that has children is called their parent (all nodes have exactly one parent, except root)
Nodes with the same parent are siblings
Nodes that have no children are leaves

A subtree of a node is a tree rooted at a child of that node
The nodes in a subtree of node A are the children of node A
A node is reached from the root by a path

```

## traversal 
Pre-order Traversal: Visit the root node first, then recursively visit the left subtree, followed by the right subtree. (Order: Root, Left, Right)
In-order Traversal: Recursively visit the left subtree first, then the root node, and finally the right subtree. This traversal yields nodes in non-decreasing order for binary search trees. (Order: Left, Root, Right)
Post-order Traversal: Recursively visit the left subtree, then the right subtree, and finally the root node. This is useful for deleting trees or evaluating expressions. (Order: Left, Right, Root)
Comparison: Pre-order is used for copying trees, in-order for sorting, and post-order for deleting or evaluating expressions.


## binary search tree
Node Ordering: For any given node, all values in the left subtree are less than the node's value, and all values in the right subtree are greater.
Unique Values: Typically, BSTs do not allow duplicate values.

### inserting 
```
Start at the root node.
Compare the value of the new node with the current node's value.
If the new value is less, move to the left child; if greater, move to the right child.
Repeat this process until you find an empty spot (null) where the new node can be inserted.
```

## binary trees
what:  A binary tree is a tree data structure in which each node has at most two children, referred to as the left child and the right child.


```
Maximum Nodes: A binary tree with height (h) can have a maximum of (2^{h+1} - 1) nodes.
Height: The height of a binary tree is the number of edges on the longest path from the root to a leaf.

```

Types of Binary Trees:
Full Binary Tree: Every node has either 0 or 2 children.
Complete Binary Tree: All levels are fully filled except possibly for the last level, which is filled from left to right.
Perfect Binary Tree: All internal nodes have two children, and all leaf nodes are at the same level.




































