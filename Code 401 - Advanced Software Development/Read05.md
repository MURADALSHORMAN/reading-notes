# Implementation: Linked Lists

In computer science, a linked list is a linear collection of data elements whose order is not given by their physical placement in memory. Instead, each element points to the next. It is a data structure consisting of a collection of nodes which together represent a sequence.


## Singly Linked Lists

![](https://miro.medium.com/max/1400/1*iiEWrP2IznA6HbmuIdK0lQ.png)

Linked lists are something we’ve all heard of, and for good reason: They serve as a base understanding for all other data structures. There are two different kinds of linked lists: Singly linked lists and Doubly linked lists. In this article, we’ll be discussing the former (and we’ll provide a brief comparison of both).
Before moving forward: An understanding of ES2015 JavaScript “Class” and “Instance Methods” syntax is required for this article. If you’ve never heard of or used JavaScript Classes, this information will be very hard to understand (as will many other data structures besides linked lists). If this is the case, do a bit of research and then come back! If you’ve got an understanding of this syntax, then let’s jump right in.



A linked list is a sequence of data structures, which are connected together via links.

Linked List is a sequence of links which contains items. Each link contains a connection to another link. Linked list is the second most-used data structure after array. Following are the important terms to understand the concept of Linked List.

Link − Each link of a linked list can store a data called an element.

Next − Each link of a linked list contains a link to the next link called Next.

LinkedList − A Linked List contains the connection link to the first link called First.

## Linked List Representation
Linked list can be visualized as a chain of nodes, where every node points to the next node.

![](https://www.tutorialspoint.com/data_structures_algorithms/images/linked_list.jpg)

As per the above illustration, following are the important points to be considered.

Linked List contains a link element called first.

Each link carries a data field(s) and a link field called next.

Each link is linked with its next link using its next link.

Last link carries a link as null to mark the end of the list.

## Types of Linked List
Following are the various types of linked list.

- Simple Linked List − Item navigation is forward only.

- Doubly Linked List − Items can be navigated forward and backward.

- Circular Linked List − Last item contains link of the first element as next and the first element has a link to the last element as previous.

## Basic Operations
Following are the basic operations supported by a list.

- Insertion − Adds an element at the beginning of the list.

- Deletion − Deletes an element at the beginning of the list.

- Display − Displays the complete list.

- Search − Searches an element using the given key.

- Delete − Deletes an element using the given key.






