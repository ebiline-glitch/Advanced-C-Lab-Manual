EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

    #include <stdio.h>
    #include <stdlib.h>

    struct Node
    {
    int data;
    struct Node *next;
    };

    int main()
    {
    struct Node *head = NULL, *newnode, *temp;
    int n, i, element, found = 0, position = 1;

    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter data: ");
        scanf("%d", &newnode->data);

        newnode->next = NULL;

        if (head == NULL)
        {
            head = newnode;
            temp = newnode;
        }
        else
        {
            temp->next = newnode;
            temp = newnode;
        }
    }

    printf("Enter the element to search: ");
    scanf("%d", &element);

    temp = head;

    while (temp != NULL)
    {
        if (temp->data == element)
        {
            found = 1;
            break;
        }

        temp = temp->next;
        position++;
    }

    if (found == 1)
        printf("Element %d found at position %d", element, position);
    else
        printf("Element not found");

    return 0;
    }
Output:

<img width="647" height="214" alt="image" src="https://github.com/user-attachments/assets/7a626d6c-968c-4820-a1aa-a2d319a8ceff" />



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

    #include <stdio.h>
    #include <stdlib.h>

    struct Node
    {
    int data;
    struct Node *next;
    };

    int main()
    {
    struct Node *head = NULL, *newnode, *temp;
    int n, i, element;

    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter data: ");
        scanf("%d", &newnode->data);

        newnode->next = NULL;

        if (head == NULL)
        {
            head = newnode;
            temp = newnode;
        }
        else
        {
            temp->next = newnode;
            temp = newnode;
        }
    }

    newnode = (struct Node *)malloc(sizeof(struct Node));

    printf("Enter the element to insert: ");
    scanf("%d", &element);

    newnode->data = element;
    newnode->next = NULL;

    temp->next = newnode;

    printf("\nLinked List after insertion:\n");

    temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
    }
Output:

<img width="740" height="249" alt="image" src="https://github.com/user-attachments/assets/f6709e52-ba1f-495f-a037-e92fc9106fb7" />

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

    #include <stdio.h>
    #include <stdlib.h>

    struct Node
    {
    int data;
    struct Node *prev;
    struct Node *next;
    };

    int main()
    {
    struct Node *head = NULL, *newnode, *temp, *last = NULL;
    int n, i;

    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter data: ");
        scanf("%d", &newnode->data);

        newnode->prev = NULL;
        newnode->next = NULL;

        if (head == NULL)
        {
            head = newnode;
            last = newnode;
        }
        else
        {
            last->next = newnode;
            newnode->prev = last;
            last = newnode;
        }
    }

    printf("\nDoubly Linked List elements are:\n");

    temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
    }
Output:

<img width="695" height="261" alt="image" src="https://github.com/user-attachments/assets/900458a2-5322-4afa-a990-d66717f1b327" />


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

    #include <stdio.h>
    #include <stdlib.h>

    struct Node
    {
    int data;
    struct Node *prev;
    struct Node *next;
    };

    int main()
    {
    struct Node *head = NULL, *newnode, *temp, *last = NULL;
    int n, i, element;

    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter data: ");
        scanf("%d", &newnode->data);

        newnode->prev = last;
        newnode->next = NULL;

        if (head == NULL)
        {
            head = newnode;
        }
        else
        {
            last->next = newnode;
        }

        last = newnode;
    }

    newnode = (struct Node *)malloc(sizeof(struct Node));

    printf("Enter the element to insert: ");
    scanf("%d", &element);

    newnode->data = element;
    newnode->prev = last;
    newnode->next = NULL;

    last->next = newnode;
    last = newnode;

    printf("\nDoubly Linked List after insertion:\n");

    temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
    }
Output:

<img width="708" height="253" alt="image" src="https://github.com/user-attachments/assets/46cec00b-90d1-4a74-953b-8f6125ad4ecc" />


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

    #include <stdio.h>
    #include <stdlib.h>

    struct Node
    {
    int data;
    struct Node *next;
     };

    int main()
    {
    struct Node *head = NULL, *newnode, *temp, *prev;
    int n, i, element;

    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    /* Create linked list */
    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter data: ");
        scanf("%d", &newnode->data);

        newnode->next = NULL;

        if (head == NULL)
        {
            head = newnode;
            temp = newnode;
        }
        else
        {
            temp->next = newnode;
            temp = newnode;
        }
    }

    printf("Enter the element to delete: ");
    scanf("%d", &element);

    temp = head;
    prev = NULL;

    while (temp != NULL && temp->data != element)
    {
        prev = temp;
        temp = temp->next;
    }

    if (temp == NULL)
    {
        printf("Element not found");
    }
    else
    {
        if (temp == head)
        {
            head = head->next;
        }
        else
        {
            prev->next = temp->next;
        }

        free(temp);

        printf("\nLinked List after deletion:\n");

        temp = head;

        while (temp != NULL)
        {
            printf("%d ", temp->data);
            temp = temp->next;
        }
    }

    return 0;
    }

Output:

<img width="804" height="282" alt="image" src="https://github.com/user-attachments/assets/536489a7-81fb-4047-80c3-f16d56250af6" />





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





