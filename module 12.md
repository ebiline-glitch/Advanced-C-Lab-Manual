

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
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
    struct Node *top = NULL, *newnode, *temp;
    int n, i;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    /* Create stack using linked list */
    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newnode->data);

        newnode->next = top;
        top = newnode;
    }

    /* Display stack elements */
    printf("\nStack elements are:\n");

    temp = top;

    while (temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }

    return 0;
    }
Output:

<img width="650" height="368" alt="image" src="https://github.com/user-attachments/assets/38fbfc80-0924-4404-aa27-2a1db3761408" />


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
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
    struct Node *top = NULL, *newnode, *temp;
    int n, i, poppedElement;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    /* Create stack using linked list */
    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newnode->data);

        newnode->next = top;
        top = newnode;
    }

    /* Pop operation */
    if (top == NULL)
    {
        printf("Stack Underflow");
    }
    else
    {
        temp = top;
        poppedElement = top->data;
        top = top->next;

        free(temp);

        printf("\nPopped element is: %d\n", poppedElement);

        printf("\nStack elements after pop:\n");

        temp = top;

        while (temp != NULL)
        {
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }

    return 0;
    }
Output:

<img width="777" height="403" alt="image" src="https://github.com/user-attachments/assets/3c918b97-8b2c-43af-910c-799a9357ddc1" />



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
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
    struct Node *front = NULL, *rear = NULL, *newnode, *temp;
    int n, i;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    /* Create queue using linked list */
    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newnode->data);

        newnode->next = NULL;

        if (front == NULL)
        {
            front = rear = newnode;
        }
        else
        {
            rear->next = newnode;
            rear = newnode;
        }
    }

    /* Display queue elements */
    printf("\nQueue elements are:\n");

    temp = front;

    while (temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }

    return 0;
    }
Output:

<img width="636" height="371" alt="image" src="https://github.com/user-attachments/assets/7d246b85-1ee7-443b-8f4f-e2ece636c4d9" />

Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
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
    struct Node *front = NULL, *rear = NULL, *newnode, *temp;
    int n, i, element;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    /* Create queue using linked list */
    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newnode->data);

        newnode->next = NULL;

        if (front == NULL)
        {
            front = rear = newnode;
        }
        else
        {
            rear->next = newnode;
            rear = newnode;
        }
    }

    /* Insert new element */
    newnode = (struct Node *)malloc(sizeof(struct Node));

    printf("Enter the element to insert: ");
    scanf("%d", &element);

    newnode->data = element;
    newnode->next = NULL;

    rear->next = newnode;
    rear = newnode;

    /* Display queue */
    printf("\nQueue elements after insertion:\n");

    temp = front;

    while (temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }

    return 0;
    }
Output:

<img width="664" height="364" alt="image" src="https://github.com/user-attachments/assets/e5085cbf-8df4-45bd-9f3c-b054f8abf7ad" />

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

    #include <stdio.h>
    #include <stdlib.h>

    struct Node
    {
    int data;
    struct Node *next;
    };

    void peek(struct Node *front)
    {
    if (front == NULL)
    {
        printf("Queue is empty");
    }
    else
    {
        printf("Peek element is: %d", front->data);
    }
    }

    int main()
    {
    struct Node *front = NULL, *rear = NULL, *newnode;
    int n, i;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    /* Create queue using linked list */
    for (i = 0; i < n; i++)
    {
        newnode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newnode->data);

        newnode->next = NULL;

        if (front == NULL)
        {
            front = rear = newnode;
        }
        else
        {
            rear->next = newnode;
            rear = newnode;
        }
    }

    /* Call peek function */
    peek(front);

    return 0;
    }
Output:

<img width="854" height="237" alt="image" src="https://github.com/user-attachments/assets/8f65f4ab-b891-4871-8494-e2ae6d762f04" />



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


