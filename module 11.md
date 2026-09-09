

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
     
    #include <stdio.h>

    int greatest(int a, int b, int c);

    int main()
    {
    int a, b, c, result;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    result = greatest(a, b, c);

    printf("Greatest number = %d", result);

    return 0;
    }

    int greatest(int a, int b, int c)
    {
    if (a >= b && a >= c)
        return a;
    else if (b >= a && b >= c)
        return b;
    else
        return c;
    }
Output:
<img width="461" height="72" alt="image" src="https://github.com/user-attachments/assets/a4be82e9-7a6b-4071-8041-d77f6f422c80" />

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
    
    #include <stdio.h>

    int main()
    {
    int n, k, i, j;
    int max_and = 0, max_or = 0, max_xor = 0;

    printf("Enter n and k: ");
    scanf("%d %d", &n, &k);

    for (i = 1; i < n; i++)
    {
        for (j = i + 1; j <= n; j++)
        {
            if ((i & j) < k && (i & j) > max_and)
                max_and = i & j;

            if ((i | j) < k && (i | j) > max_or)
                max_or = i | j;

            if ((i ^ j) < k && (i ^ j) > max_xor)
                max_xor = i ^ j;
        }
    }

    printf("%d\n", max_and);
    printf("%d\n", max_or);
    printf("%d\n", max_xor);

    return 0;
    }
Output:
<img width="551" height="109" alt="image" src="https://github.com/user-attachments/assets/d25c0a26-5f7a-4fab-b82a-339ed5794a58" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
    
    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
    int noshel, noque;
    int **shelarr;
    int *nobookarr;
    int i, j, type, x, y;

    printf("Enter number of shelves and queries: ");
    scanf("%d %d", &noshel, &noque);

    shelarr = (int **)malloc(noshel * sizeof(int *));
    nobookarr = (int *)calloc(noshel, sizeof(int));

    for (i = 0; i < noshel; i++)
    {
        shelarr[i] = NULL;
    }

    for (i = 0; i < noque; i++)
    {
        scanf("%d", &type);

        if (type == 1)
        {
            scanf("%d %d", &x, &y);

            shelarr[x] = (int *)realloc(
                shelarr[x],
                (nobookarr[x] + 1) * sizeof(int)
            );

            shelarr[x][nobookarr[x]] = y;
            nobookarr[x]++;
        }
        else if (type == 2)
        {
            scanf("%d %d", &x, &y);

            printf("%d\n", shelarr[x][y]);
        }
    }

    for (i = 0; i < noshel; i++)
    {
        free(shelarr[i]);
    }

    free(shelarr);
    free(nobookarr);

    return 0;
    }
Output:
<img width="548" height="229" alt="image" src="https://github.com/user-attachments/assets/4bfd17a5-dc27-4b41-9dc2-efc2eb2ae028" />


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
    
    #include <stdio.h>

    int main()
    {
    int n, i, sum = 0;
    int arr[100];

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter the array elements: ");

    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
        sum = sum + arr[i];
    }

    printf("Sum of the array elements = %d", sum);

    return 0;
    }
Output:
<img width="556" height="85" alt="image" src="https://github.com/user-attachments/assets/45e63c8b-1802-4a86-9817-627445754572" />

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
    
    #include <stdio.h>

    int main()
    {
    char str[100];
    int i, count = 0;

    printf("Enter a sentence: ");
    scanf(" %[^\n]", str);

    for (i = 0; str[i] != '\0'; i++)
    {
        if (str[i] == ' ' && str[i + 1] != ' ')
        {
            count++;
        }
    }

    if (str[0] != '\0')
        count++;

    printf("Number of words = %d", count);

    return 0;
    }
Output:
<img width="586" height="69" alt="image" src="https://github.com/user-attachments/assets/7f603279-f053-48a4-aa75-fbc8d23d9b97" />



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
