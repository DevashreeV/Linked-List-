# Linked-List-

A linked list is a group of nodes—a collection of items—that are scattered throughout memory. Each node contains two fields: one for data storage and the other for the next node's memory location. The first node's address is included in the head node, and a pointer to the null is found in the linked list's last node. Many different operations may be carried out on linked lists using linked list operations including insert, remove, traverse, search, and sort.

![image](https://user-images.githubusercontent.com/91966097/234397392-6cea8294-9975-4c60-ac2e-4193eacc7b8b.png)


Basic Syntax:

    struct Node {
        int data;
        struct Node* next;
    };
   
To create a linked list, you start by creating the head node, and then you add new nodes to the list by creating them dynamically with the malloc() function and setting the next pointer of the previous node to point to the new node.

## Types of Linked List:

Singly Linked List: Singly linked list is the most common linked list type. Each node stores data as well as a pointer to the next node.

Doubly Linked List: A doubly linked list is created by adding pointers to the previous and next nodes.

Circular Linked List: A circular linked list is a variation of a linked list in which the last element is linked to the first element.

## Applications:

Stacks and queues implementation

Dynamic memory allocation

Graphs implementation

Representing sparse matrices

Precision arithmetic

## Code:

    #include <stdio.h>
    #include <stdlib.h>

    struct node {
      int value;
      struct node *next;
    };


    void printLinkedlist(struct node *p) {
      while (p != NULL) {
        printf("%d ", p->value);
        p = p->next;
      }
    }

    int main() {

      struct node *head;
      struct node *one = NULL;
      struct node *two = NULL;
      struct node *three = NULL;


      one = malloc(sizeof(struct node));
      two = malloc(sizeof(struct node));
      three = malloc(sizeof(struct node));

      one->value = 1;
      two->value = 2;
      three->value = 3;

      one->next = two;
      two->next = three;
      three->next = NULL;

      head = one;
      printLinkedlist(head);
    }

## Explanation:

 1. First it defines a struct called node that has two fields: an integer value and a pointer to the next node in the list.
 
 2.Then a  function takes a pointer to the head of a linked list and prints out each node's value field in order by following the next pointers until it reaches the end of the list (indicated by a NULL pointer).
 
 3.In the main function  it defines and initialises to NULL four pointers to node structs, one of which is a reference to the list's head (head).
 
 4.The malloc() method is then used to dynamically create memory for three nodes and assign them to pointers 1, 2, and 3. Each node's value field is set to 1, 2, or 3 depending on the node.
 
 5.The next node in the list is then pointed to by each node's next pointer. It specifically sets the next pointers for one to point to two, two to point to three, and three to point to NULL to denote the list's conclusion.
 
 6.It sets the head pointer to point to one (the first node in the list) and calls the printLinkedlist() function to print out the values of each node in the list.
 
 OUTPUT:
 
 ![Screenshot (739)](https://user-images.githubusercontent.com/91966097/234399800-7a237de4-04f8-45a5-b951-4e93d86457ee.png)

