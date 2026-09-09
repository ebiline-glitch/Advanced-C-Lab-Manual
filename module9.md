EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

    #include <stdio.h>

    #define MAX 10

    int main()
    {
    int stack[MAX];
    int top = -1;
    int n, i;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    if (n > MAX)
    {
        printf("Stack Overflow");
        return 0;
    }

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &stack[++top]);
    }

    printf("\nStack elements are:\n");

    for (i = top; i >= 0; i--)
    {
        printf("%d\n", stack[i]);
    }

    return 0;
    }
Output:

<img width="730" height="351" alt="image" src="https://github.com/user-attachments/assets/c8f6ecf9-ab77-43b1-af34-673a71f03ab3" />



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

    #include <stdio.h>

    #define MAX 10

    int main()
    {
    int stack[MAX];
    int top = -1;
    int n, i, element;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &stack[++top]);
    }

    printf("Enter the element to push: ");
    scanf("%d", &element);

    if (top == MAX - 1)
    {
        printf("Stack Overflow");
    }
    else
    {
        top++;
        stack[top] = element;

        printf("\nElement pushed successfully.\n");

        printf("Stack elements are:\n");

        for (i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }

    return 0;
    }
Output:

<img width="837" height="400" alt="image" src="https://github.com/user-attachments/assets/c325a848-184f-4a7c-8c54-422fe5b340f4" />




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

    #include <stdio.h>

    #define MAX 10

    int main()
    {
    int queue[MAX];
    int front = 0, rear = -1;
    int n, i;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    if (n > MAX)
    {
        printf("Queue Overflow");
        return 0;
    }

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &queue[++rear]);
    }

    printf("\nQueue elements are:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%d\n", queue[i]);
    }

    return 0;
    }
Output:

<img width="767" height="357" alt="image" src="https://github.com/user-attachments/assets/0e6dea2c-f696-47bf-ad55-8f668434eb5e" />


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

    #include <stdio.h>

    #define MAX 10

    int main()
    {
    int queue[MAX];
    int front = 0, rear = -1;
    int n, i, element;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &queue[++rear]);
    }

    printf("Enter the element to insert: ");
    scanf("%d", &element);

    if (rear == MAX - 1)
    {
        printf("Queue Overflow");
    }
    else
    {
        rear++;
        queue[rear] = element;

        printf("\nElement inserted successfully.\n");

        printf("Queue elements are:\n");

        for (i = front; i <= rear; i++)
        {
            printf("%d\n", queue[i]);
        }
    }

    return 0;
    }
Output:

<img width="603" height="386" alt="image" src="https://github.com/user-attachments/assets/9649aca8-20e2-4dcc-b796-babd0b1ec847" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

    #include <stdio.h>

    #define MAX 10

    int main()
    {
    int queue[MAX];
    int front = 0, rear = -1;
    int n, i, deletedElement;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        rear++;
        scanf("%d", &queue[rear]);
    }

    if (front > rear)
    {
        printf("Queue Underflow");
    }
    else
    {
        deletedElement = queue[front];
        front++;

        printf("\nDeleted element is: %d\n", deletedElement);

        printf("\nQueue elements after deletion are:\n");

        for (i = front; i <= rear; i++)
        {
            printf("%d\n", queue[i]);
        }
    }

    return 0;
    }

Output:

<img width="714" height="387" alt="image" src="https://github.com/user-attachments/assets/c6e02c22-b2cc-4a5e-9903-bd64b2d1b0e2" />


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
