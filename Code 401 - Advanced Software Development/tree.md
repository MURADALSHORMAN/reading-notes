

A tree data structure can be defined recursively as a collection of nodes (starting at a root node), where each node is a data structure consisting of a value, together with a list of references to nodes (the "children"), with the constraints that no reference is duplicated, and none points to the root.

Alternatively, a tree can be defined abstractly as a whole (globally) as an ordered tree, with a value assigned to each node. Both these perspectives are useful: while a tree can be analyzed mathematically as a whole, when actually represented as a data structure it is usually represented and worked with separately by node (rather than as a set of nodes and an adjacency list of edges between nodes, as one may represent a digraph, for instance). For example, looking at a tree as a whole, one can talk about "the parent node" of a given node, but in general, as a data structure, a given node only contains the list of its children but does not contain a reference to its parent (if any).


## Common Terminology:
- Node : A Tree node is a component which may contain it’s own values, and references to other nodes
- Root : The root is the node at the beginning of the tree
- K : A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left : A reference to one child node, in a binary tree
- Right : A reference to the other child node, in a binary tree
- Edge : The edge in a tree is the link between a parent and child node
- Leaf : leaf is a node that does not have any children
- Height : The height of a tree is the number of edges from the root to the furthest leaf


## Traversals
traverse tree , two common ways DFS,BFS techniques:

- Pre-order: root =>> left =>> right
- In-order: left =>> root =>> right
- Post-order: left =>> right =>> root

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)
