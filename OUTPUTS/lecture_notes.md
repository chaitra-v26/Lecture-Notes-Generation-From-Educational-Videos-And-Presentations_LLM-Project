## Data Structures and Its Applications (UE19CS202)
---

**Instructors:*
* Shylaja S S & Kusuma K V
**Department:*
* Computer Science & Engineering

---

## n-ary Tree Traversal 🌳
---

### Tree Traversal


**Structure of a treenode:**

```c
struct treenode{
 	int info;
	struct treenode *child;
	struct treenode *sibling;
};
```

---

### Tree Traversal Implementation with Child and Sibling Pointers


With the `treenode` implemented using pointers to the first child and immediate sibling, the preorder, inorder, and postorder traversals for a tree are defined as follows:

#### Preorder Traversal

1. Visit the root of the first tree in the forest.
2. Traverse in preorder the forest formed by the subtrees of the first tree, if any.
3. Traverse in preorder the forest formed by the remaining trees in the forest, if any.

**💡 **Example:***
* A B E F C G H D

**Code Implementation:**

```c
void preorder(TREE *root)
{
     if(root!=NULL)
     {
       printf(" %d ",root->info);
       preorder(root->child);
       preorder(root->sibling);
    }
}
```

---

#### Inorder Traversal

1. Traverse in inorder the forest formed by the subtrees of the first tree, if any.
2. Visit the root of the first tree in the forest.
3. Traverse in inorder the forest formed by the remaining trees in the forest, if any.


**💡 **Example:***
* E F B H G C D A

**Code Implementation:**

```c
void inorder(TREE *root)
{
   if(root!=NULL)
     {
       inorder(root->child);
       printf(" %d ",root->info);
       inorder(root->sibling);
    }
}
```

---

#### Postorder Traversal

1. Traverse in postorder the forest formed by the subtrees of the first tree, if any.
2. Traverse in postorder the forest formed by the remaining trees in the forest, if any.
3. Visit the root of the first tree in the forest.


**💡 **Example:***
* F E H G D C B A

**Code Implementation:**

```c
void postorder(TREE *root)
{
   if(root!=NULL)
     {
       postorder(root->child);
       postorder(root->sibling);
       printf(" %d ", root->info);
    }
}
```

---

📧 shylaja.sharath@pes.edu

Thank you! 🙏
