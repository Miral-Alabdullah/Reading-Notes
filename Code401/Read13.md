# Trees

<br>


**Common Terminology**

<br>


| Terminology   | What for?                                                                                                        |
| ------------- | ---------------------------------------------------------------------------------------------------------------- |
| Node          | A Tree node is a component which may contain it’s own values, and references to other nodes                      |
| Root          | The root is the node at the beginning of the tree                                                                |
| K             | A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2| 
| Left          | A reference to one child node, in a binary tree                                                                  | 
| Right         | A reference to the other child node, in a binary tree                                                            | 
| Edge          | The edge in a tree is the link between a parent and child node                                                   | 
| Leaf          | A leaf is a node that does not have any children                                                                 | 
| Height        | The height of a tree is the number of edges from the root to the furthest leaf                                   | 


<br>
<hr>
<br>


## Traversals : 

<br>


- Depth First Search

  - We use the stack to implement this.

  Here is where we prioritize going through the depth (height) of the tree first.

    - Here are three methods for depth first traversal:
	  
	  * Pre-order: `root >> left >> right`

	  * In-order: `left >> root >> right`

	  * Post-order: `left >> right >> root`


  ![!](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)


  By Looking at the tree above, applying the three methods will give us the following results : 


    * Pre-order: `A, B, D, E, C, F`

    * In-order: `D, B, E, A, F, C`

    * Post-order: `D, E, B, F, C, A`

-  The biggest difference between each of the traversals is when you are looking at the root node.

<br>
<br>
<br>


- Breadth First Search

  - We use the queue to implement this.

  - Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

  ![!](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)

<br>

   * By Looking at the tree above the result will be as following: 

       `A, B, C, D, E, F`


<br>
<hr>
<br>

# Recursion

- What is Recursion? 
 
   * The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.

   * The function “ f( ) ” itself is being called inside the function, so this phenomenon is named as recursion and the function containing recursion is called recursive function.


- Why Stack Overflow error occurs in recursion? 

If the base case is not reached or not defined, then the stack overflow problem may arise. Let us take an example to understand this.



```
int fact(int n)
{
    // wrong base case (it may cause
    // stack overflow).
    if (n == 100) 
        return 1;

    else
        return n*fact(n-1);
}
```

> If fact(10) is called, it will call fact(9), fact(8), fact(7) and so on but the number will never reach 100. So, the base case is not reached. If the memory is exhausted by these functions on the stack, it will cause a stack overflow error. 