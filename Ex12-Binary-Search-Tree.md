# Ex12 Binary Search Tree
## DATE: 13-03-25
## AIM:
To write a C function to insert the elements in the binary search tree

## Algorithm
1. Start
2. 3. Check if the current node is NULL; if true, create a new node with the given key.
Allocate memory for the new node, set its key, and initialize its left and right children to
NULL.
4. 5. If the current node is not NULL, compare the key with the current node's key.
If key <= node->key, recursively insert the key into the left subtree and update the left child
pointer.
6. If key > node->key, recursively insert the key into the right subtree and update the right
child pointer.
7. Return the current node after the insertion.
8. End   

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: C.Shrenidhi
RegisterNumber:  212223040196
*/

/*struct node {
int key;
struct node *left, *right;
};*/
struct node* insert(struct node* node, int key)
{
if(node==NULL)
{
struct node* node=(struct node*)malloc(sizeof(struct node));
node->key=key;
node->left=NULL;
node->right=NULL;
return node;
}
else
{
struct node* cur;
if(key<=node->key)
{
cur=insert(node->left,key);
node->left=cur;
}
else
{
}
cur=insert(node->right,key);
node->right=cur;
return node;
}
}

```

## Output:
<img width="369" alt="image" src="https://github.com/user-attachments/assets/ced21cc3-2946-4de6-a948-4f7e574fb87a" />




## Result:
Thus, the C function to insert the elements in the binary search tree is implemented successfully.
