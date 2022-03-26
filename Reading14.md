# JavaScript data structure: tree

## Abstract 
> Tree is one of the most commonly used data structures in web development. This sentence applies to both developers and users: developers create a DOM through HTML, and users consume network information through DOM.
Further, the text you are reading is rendered in a browser in the form of a tree. The paragraph in the article is represented by the text in the < p > tag, which is nested in the < body > element, while the < body > element is a sub-element of < HTML >.
The nesting of data is similar to a pedigree: the < HTML > element is a father, the < body > element is a child, and the < p > element is a child of the < body > element. If you feel this analogy is easy to understand, then in the next process of implementing a tree, more analogies should not be a problem for you.
In this article, we will create a tree with two traversal modes: Depth-First-Search(DFS) depth-first search and Breadth-First-Search(BFS) breadth-first search (traversal refers to each node accessing the tree). These two traversals emphasize the different positions of a tree, and they use the data structure we mentioned earlier: DFS uses stacks, BFS uses queues

## Trees (DFS and BFS)
>Tree is a data structure that uses nodes to simulate hierarchical data. Nodes store data and point to other nodes (each node stores its own data and pointers to other nodes). Some readers may not be familiar with the terms node, pointer and so on, so let's make an analogy here: to compare a tree to an organizational structure. This organizational structure has a top person in charge (root node), such as the general manager. This is closely followed by a position, such as a vice president.
We use an arrow from the boss to the vice president to show this relationship. Chief Executive Vice President. A position (chief executive) is a node; the relationship between chief executive and vice president (arrow) is the pointer. To create more similar relationships in the organizational chart, just repeat the steps above, one node points to another.
Conceptually, I want nodes and pointers to make sense. In practice, we can cite another DOM chestnut. The root node of a DOM is <html>, which points to <head> and <body>. Then repeat to generate a DOM tree.
The best thing about doing this is that it has the ability to nest nodes: a < UL > can have n < li > nodes inside, and each < li > can also have brothers < li > nodes. (The author gave a strange compliment)

**Manipulating trees**
>Trees and nodes can be described by two separate constructors: Node and Tree.

* Node
   - data stores a value

    - Parent points to the parent of this node

    - children points to the next node in the table (which may have a heap, then an array)

* Tree
- Root points to the root node of the tree

- traverseDF(callback) traverses tree nodes using DFS

- Traverse BF (callback) traverses tree nodes using BFS

- contains(data,traversal) searches for a node in the tree

- add(data,toData,traverse) Add a node to the tree

- remove(child,parent) delete a node of the tree