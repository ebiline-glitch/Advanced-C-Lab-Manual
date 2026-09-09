EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:

    #include <stdio.h>

    struct Person
    {
    char name[50];
    int age;
    };

    int main()
    {
    struct Person p[10];
    int n, i;

    printf("Enter the number of persons: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++)
    {
        printf("\nEnter name: ");
        scanf("%s", p[i].name);

        printf("Enter age: ");
        scanf("%d", &p[i].age);
    }

    printf("\nVaccine Eligibility:\n");

    for(i = 0; i < n; i++)
    {
        if(p[i].age >= 18)
            printf("%s is Eligible for Vaccine\n", p[i].name);
        else
            printf("%s is Not Eligible for Vaccine\n", p[i].name);
    }

    return 0;
    }


Output:

<img width="740" height="409" alt="image" src="https://github.com/user-attachments/assets/c277904d-1a48-4353-b256-07e6468a5597" />


Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:

    #include <stdio.h>

    struct Student
    {
    char name[50];
    int age;
    float mark;
    };

    // Function to receive structure as argument
    void display(struct Student s)
    {
    printf("\nStudent Details:\n");
    printf("Name: %s\n", s.name);
    printf("Age: %d\n", s.age);
    printf("Mark: %.2f\n", s.mark);
    }

    // Function to return a structure
    struct Student getStudent()
    {
    struct Student s;

    printf("Enter name: ");
    scanf("%s", s.name);

    printf("Enter age: ");
    scanf("%d", &s.age);

    printf("Enter mark: ");
    scanf("%f", &s.mark);

    return s;
    }

    int main()
    {
    struct Student s1;

    // Receiving returned structure
    s1 = getStudent();

    // Passing structure to function
    display(s1);

    return 0;
    }




Output:


<img width="864" height="470" alt="image" src="https://github.com/user-attachments/assets/3c5b4954-ffff-4d68-92fa-65022a379ee2" />




Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

    #include <stdio.h>

    int main()
    {
    FILE *fp;
    char filename[50];
    char text[100];

    printf("Enter the file name: ");
    scanf("%s", filename);

    fp = fopen(filename, "w");

    if (fp == NULL)
    {
        printf("File cannot be opened.\n");
        return 1;
    }

    printf("Enter text to write into the file: ");
    scanf(" %[^\n]", text);

    fprintf(fp, "%s", text);

    fclose(fp);

    printf("Data successfully written into %s\n", filename);

    return 0;
    }



Output:


<img width="856" height="107" alt="image" src="https://github.com/user-attachments/assets/fae4abd5-c93c-4456-87f1-f8b9485600b1" />











Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

    #include <stdio.h>

    int main()
    {
    FILE *fp;
    char filename[50];
    char text[200];

    printf("Enter the file name: ");
    scanf("%s", filename);

    fp = fopen(filename, "w");

    if (fp == NULL)
    {
        printf("Error! File cannot be opened.\n");
        return 1;
    }

    printf("Enter the text to insert into the file: ");
    scanf(" %[^\n]", text);

    fprintf(fp, "%s", text);

    fclose(fp);

    printf("\nText successfully written into %s\n", filename);

    return 0;
    }



Output:


<img width="896" height="125" alt="image" src="https://github.com/user-attachments/assets/e2a92621-b38f-47a5-8fe4-a8bab14d4aef" />






Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

    #include <stdio.h>

    struct Student
    {
    char name[50];
    int rollNo;
    int age;
    float mark;
    };

    int main()
    {
    struct Student s;

    printf("Enter student name: ");
    scanf("%s", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.rollNo);

    printf("Enter age: ");
    scanf("%d", &s.age);

    printf("Enter mark: ");
    scanf("%f", &s.mark);

    printf("\n--- Student Details ---\n");
    printf("Name        : %s\n", s.name);
    printf("Roll Number : %d\n", s.rollNo);
    printf("Age         : %d\n", s.age);
    printf("Mark        : %.2f\n", s.mark);

    return 0;
    }




Output:


<img width="683" height="290" alt="image" src="https://github.com/user-attachments/assets/8e74b694-380a-4c17-8c85-fe59b80eea52" />






Result:
Thus, the program is verified successfully
