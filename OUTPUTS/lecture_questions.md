**Q1:**  Given a n-ary tree node structure defined as `struct treenode{ int info; struct treenode *child; struct treenode *sibling; };`, what do `child` and `sibling` pointers represent?
**A1:** `child` points to the first child of the node, and `sibling` points to the next sibling of the node (or null if it's the last sibling).

**Q2:** What is the preorder traversal output for the following n-ary tree (represented by nested parentheses): A(B(E,F),C(G,H),D)?
**A2:** A B E F C G H D

**Q3:**  The inorder traversal of an n-ary tree visits the root *when* in relation to its children and siblings?
**A3:** After visiting all children (subtrees) but before visiting any siblings.

**Q4:** What is the postorder traversal output for the following n-ary tree (represented by nested parentheses):  A(B,C(D,E))?
**A4:** B D E C A

**Q5:** Which traversal algorithm would be most suitable for deleting nodes in an n-ary tree implemented with child and sibling pointers, and why?
**A5:** Postorder. Because in postorder traversal, we visit the children before the parent. So, we can delete the children first and then the parent, preventing any dangling pointers.


**Q6:**  Consider the `inorder` traversal function provided in the notes.  If `root->child` is NULL, what will happen?
**A6:** The function will skip the recursive call to `inorder(root->child)` and proceed to print the current node's info and then process the siblings.


**Q7:** In the given `treenode` structure, how are n-ary trees represented using only two pointers?
**A7:** The `child` pointer represents a linked list of children, and the `sibling` pointer links nodes at the same level (siblings). This creates the n-ary tree structure.

**Q8:**  What does the forest metaphor represent in the context of n-ary tree traversal descriptions?
**A8:**  A forest represents a set of trees. In the traversal descriptions, the children of a node, and the subsequent siblings and their children, are treated as separate trees within a "forest."

**Q9:**  If a node has no children, what will be the value of its `child` pointer?
**A9:** NULL


**Q10:**  True or False:  Preorder traversal of an n-ary tree implemented with child/sibling pointers is the same as depth-first search.
**A10:** True. Preorder traversal effectively explores as deep as possible along each branch before backtracking, just like depth-first search.
