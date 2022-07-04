# **Trees**

## **Binary Tree**

 ![Binary Tree](./binary_tree.png)

## Terminology
- **Node** - A Tree node is a component which __may contain its own values, and references to other nodes__.
- **Root** - The root is the __node at the beginning__ of the tree

- **K** - A number that specifies the __maximum number of children__ any node may have in a `k-ary tree`. _In a `binary tree`, **`k = 2`**_.

- **Left** - A **reference** to one child node, **in a binary tree**.

- **Right** - A **reference** to the other child node, in a binary tree.

- **Edge** - The edge in a tree is **the link between a parent and child** node.

- **Leaf** - A leaf is a **node that does not have any children**.
- **Height** - The height of a tree is **the number of edges from the root to the furthest leaf**. [1]





## **Traversals**
**Traversing a tree allows us to search for a node, print out the contents of a tree**, and more.

The two categories of trees traversals:
1. Depth First.
2. Breadth First.

### **Depth First**
**Depth first traversal is where we prioritize going through the depth (height) of the tree first**. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal: [1]

- **Pre-order:** `root >> left >> right`
- **In-order:** `left >> root >> right`
- **Post-order:** `left >> right >> root`

### **`Traversal Pseudocode`**
1. **Pre-order**

        ALGORITHM preOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- pre-order output of tree node's values

            OUTPUT <-- root.value

            if root.left is not Null
                preOrder(root.left)

            if root.right is not NULL
                preOrder(root.right)

2. **In-order**

        ALGORITHM inOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- in-order output of tree node's values

            if root.left is not NULL
                inOrder(root.left)

            OUTPUT <-- root.value

            if root.right is not NULL
                inOrder(root.right)

3. **Post-order**

        ALGORITHM postOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- post-order output of tree node's values

            if root.left is not NULL
                postOrder(root.left)

            if root.right is not NULL
                postOrder(root.right)

            OUTPUT <-- root.value


### **Breadth First**
**Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.**

Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree. 

### **`Pseudocode`**
Here is the `pseudocode`, _utilizing a built-in queue to implement a breadth first traversal_.

        ALGORITHM breadthFirst(root)
        // INPUT  <-- root node
        // OUTPUT <-- front node of queue to console

        Queue breadth <-- new Queue()
        breadth.enqueue(root)

        while ! breadth.is_empty()
            node front = breadth.dequeue()
            OUTPUT <-- front.value

            if front.left is not NULL
            breadth.enqueue(front.left)

            if front.right is not NULL
            breadth.enqueue(front.right)

## **Binary Tree Vs K-ary Trees**

Trees can have any number of children per node, but Binary Trees restrict the number of children to two.

### **K-ary Trees**
If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. [1]

### **Breadth First Traversal**
>Traversing a K-ary tree requires a similar approach to the breadth first traversal. **_We are still pushing nodes into a queue_**, **but we are now moving down a list of children of length k, instead of checking for the presence of a left and a right child**. [1]

 ![Kary Tree](./k_ary_tree.png)

### **`Pseudocode`**

        ALGORITHM breadthFirst(root)
        // INPUT  <-- root node
        // OUTPUT <-- front node of queue to console

        Queue breadth <-- new Queue()
        breadth.enqueue(root)

        while ! breadth.is_empty()
            node front = breadth.dequeue()
            OUTPUT <-- front.value

            for child in front.children
                breadth.enqueue(child)

## **Adding a node** <sup>[1]</sup>
Because there are no structural rules for where nodes are “supposed to go” in a binary tree, _it really doesn’t matter where a new node gets placed._

**One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down. To do so, we would leverage the use of `breadth first traversal`**. During the traversal, we find the first node that does not have all its children filled, and insert the new node as a child. We fill the child slots from left to right.

**In the event you would like to have a node placed in a specific location, you need to reference both the new node to create, and the parent node which the child is attached to.**







### **Big O**
- The **Big O time complexity for inserting a new node is O(n)**.
- **Searching for a specific node will also be O(n).**
Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. _If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity._

- **The Big O space complexity for a node insertion using breadth first insertion will be O(w)**, **_where `w` is the largest width of the tree._**

- A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is **`2^(h-1)`**, where _`h` is the height of the tree_. Height can be calculated as **log n**, where **`n`** is the number of nodes. [1]



**For more on the subject of _Trees_, refer to the following article titled *`Implementation: Trees`* at `Codefellows.github`**
 - [Implementation: Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)
 


<br/>

## I want to learn more about
 - Methods of `Tree` Traversal.
 - MAnipulating the `Nodes` of a `Tree`.
 


[1]: https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html
[2]: 