# Ex19 B+ Tree
## DATE:19.3.25
## AIM:
To write a C function to traverse the elements in a B+ Tree.

## Algorithm
1.Start

2.Iterate through each element in the node's data array.

3.If the node is not a leaf, recursively call traverse on the current child pointer.

4.Print the current data element.

5.After the loop, if the node is not a leaf, traverse the last child pointer.

6.Return after completing the traversal.

7.End  

## Program:
```
/*
Program to traverse the elements in a B+ Tree.
Developed by: S V SHADHANASHREE
RegisterNumber:  212223230202
*/
/*struct B_TreeNode 
{ 
int *data; 
struct B_TreeNode **child_ptr; 
int leaf; 
int n; 
}; 
struct B_TreeNode *root = NULL, *np = NULL, *x = NULL;*/ 
 
void traverse(struct B_TreeNode *p) 
{ 
int i; 
for(i=0;i<p->n;i++) 
{ 
if(p->leaf==0) 
{ 
traverse(p->child_ptr[i]); 
} 
printf("%d ",p->data[i]); 
} 
if(p->leaf==0) 
{ 
traverse(p->child_ptr[i]); 
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/50091dfb-7d1d-4039-aa56-67bf4c99f963)



## Result:
Thus, the function to traverse the elements in a B+ Tree is implemented successfully.
