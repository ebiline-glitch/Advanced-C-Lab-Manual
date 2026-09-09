EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

    #include <stdio.h>

    int main()
    {
    int n;

    printf("Enter a number (1-10): ");
    scanf("%d", &n);

    switch(n)
    {
        case 1:
            printf("one");
            break;
        case 2:
            printf("two");
            break;
        case 3:
            printf("three");
            break;
        case 4:
            printf("four");
            break;
        case 5:
            printf("five");
            break;
        case 6:
            printf("six");
            break;
        case 7:
            printf("seven");
            break;
        case 8:
            printf("eight");
            break;
        case 9:
            printf("nine");
            break;
        case 10:
            printf("ten");
            break;
        default:
            printf("Invalid number");
    }

    return 0;
    }



Output:


<img width="552" height="82" alt="image" src="https://github.com/user-attachments/assets/bc1e8394-8e9e-4e9f-aa00-8706aa8d7b99" />






Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

    #include <stdio.h>

    int main()
    {
    int n, i;
    int digit;
    int frequency[10] = {0};

    printf("Enter the number of digits: ");
    scanf("%d", &n);

    printf("Enter %d digits (0 to 3):\n", n);

    for(i = 0; i < n; i++)
    {
        scanf("%d", &digit);
        frequency[digit]++;
    }

    printf("Frequency of digits from 0 to 9:\n");

    for(i = 0; i < 10; i++)
    {
        printf("%d ", frequency[i]);
    }

    return 0;
    }




Output:


<img width="701" height="153" alt="image" src="https://github.com/user-attachments/assets/82790fc1-942f-4348-9da4-51e44ba90d15" />






Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

    #include <stdio.h>
    #include <string.h>
    #include <stdlib.h>

    int compare(const void *a, const void *b)
    {
    return (*(char *)a - *(char *)b);
    }

    void swap(char *a, char *b)
    {
    char temp = *a;
    *a = *b;
    *b = temp;
    }

    void permute(char str[], int l, int r)
    {
    int i;

    if (l == r)
    {
        printf("%s\n", str);
    }
    else
    {
        for (i = l; i <= r; i++)
        {
            swap(&str[l], &str[i]);
            permute(str, l + 1, r);
            swap(&str[l], &str[i]);
        }
    }
    }

    int main()
    {
     char str[100];
    int n;

    printf("Enter a string: ");
    scanf("%s", str);

    n = strlen(str);

    // Sort the string in lexicographical order
    qsort(str, n, sizeof(char), compare);

    printf("Permutations in lexicographical order:\n");

    permute(str, 0, n - 1);

    return 0;
    }



Output:


<img width="733" height="272" alt="image" src="https://github.com/user-attachments/assets/4d35986b-26ef-4089-adbc-ecc7ab7b5287" />






Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
     
     #include <stdio.h>

    int main()
    {
    int n, i, j, len, min;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    len = n * 2 - 1;

    for (i = 0; i < len; i++)
    {
        for (j = 0; j < len; j++)
        {
            min = i;

            if (j < min)
                min = j;

            if (len - 1 - i < min)
                min = len - 1 - i;

            if (len - 1 - j < min)
                min = len - 1 - j;

            printf("%d ", n - min);
        }

        printf("\n");
    }

    return 0;
    }




Output:


<img width="525" height="260" alt="image" src="https://github.com/user-attachments/assets/a8878085-b2fc-42d3-b292-73d625baac23" />






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

    #include <stdio.h>

    int square();

    int main()
    {
    int result;

    result = square();

    printf("Square of the number = %d", result);

    return 0;
    }

    int square()
    {
    int n, sq;

    printf("Enter a number: ");
    scanf("%d", &n);

    sq = n * n;

    return sq;
    }



Output:


<img width="680" height="81" alt="image" src="https://github.com/user-attachments/assets/12d4b8b6-0793-4be3-a67e-72d20e7082c6" />






Result:
Thus, the program is verified successfully



























