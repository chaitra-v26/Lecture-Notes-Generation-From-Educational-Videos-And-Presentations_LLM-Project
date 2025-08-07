```
n-ary Tree Traversal (UE19CS202)

+-----------------+     
| treenode       |     
+--------+--------+     
|  info  |        |     
+--------+--------+     
| child  |----->  +--------+--------+
+--------+        |  info  |        |
| sibling|----->  +--------+--------+
+--------+        | child  |-----> ...
                  +--------+--------+
                  | sibling|-----> ...
                  +--------+--------+


Tree Traversal Implementations (child & sibling pointers)

                 +------------+
                 |   TREE     |
                 +-----+------+
                       | root
                       v
+-------------------+  +-------------------+  +-------------------+
| Preorder          |  | Inorder          |  | Postorder         |
+--------+--------+  +--------+--------+  +--------+--------+
|  Visit |        |  | Traverse|        |  | Traverse|        |
|  Root  |----->  |  Left   |----->  |  Left   |----->  |  Left   |
+--------+--------+  +--------+--------+  +--------+--------+
| Traverse|        |  |  Visit |        |  | Traverse|        |
| Right  |----->  |  Root  |----->  |  Right  |----->  |  Right  |
+--------+--------+  +--------+--------+  +--------+--------+
|        |        |  | Traverse|        |  |  Visit |        |
|        |        |  | Right  |----->  |  Root  |
+--------+--------+  +--------+--------+  +--------+--------+

Example Tree (Assume A is root, B and C are its children, etc.):
      A
     / \
    B   C
   /     \
  E       G
 / \     / \
F   -   H   D


Preorder:  A B E F C G H D
Inorder:   E F B H G C D A
Postorder: F E H G D C B A

```