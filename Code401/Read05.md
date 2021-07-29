# Linked Lists

- What is a Linked List؟
 
> It's a data structure that contains sequence of nodes that connected to each other and each node points to the next one.

> One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

> There are two types of Linked List - Singly and Doubly.


* <b>Singly</b> - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

* <b>Doubly</b> - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

* <b>Node</b> - An individual item in the linked list that hold/contain the data for each link.

* <b>Next</b> - It a node property that contains the reference to the next node.

* <b>Head</b> - First node in the list.

* <b>Current</b> - The Current is a reference of type Node to the node that is currently being looked at. 

![parts-of](https://miro.medium.com/max/875/1*K0_eV07tJtKQSVGKfP18bw.jpeg)


![linked-list](https://miro.medium.com/max/1200/1*hk2vLhF9CK94grEu93pzLQ.png)


### Big-O Notation of the Linked list and Arrays to see the difference

![big-O](https://i.ytimg.com/vi/z4pzb-hX2EI/maxresdefault.jpg)


### Memory : 

- Arrays => It takes a one contiguous block in the memory. 

- Linked List => Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout.

![memory](https://miro.medium.com/max/875/1*G43FVT5xJ1n1QDKVNZUxXQ.jpeg)


- The fundamental difference between arrays and linked lists is that arrays are static data structures (always needs a given size and amount of memory.), while linked lists are dynamic data structures (It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.). 