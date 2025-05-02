# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

```

#include <stdio.h>

int main() {
    float length, width, area;
    float *ptrLength = &length, *ptrWidth = &width, *ptrArea = &area;

    printf("Enter the length of the rectangle: ");
    scanf("%f", ptrLength); 
    printf("Enter the width of the rectangle: ");
    scanf("%f", ptrWidth); 
    *ptrArea = (*ptrLength) * (*ptrWidth); 
    printf("The area of the rectangle is: %.2f\n", *ptrArea);

    return 0;
}

```
## OUTPUT
		       	
![image](https://github.com/user-attachments/assets/430b1ddc-7b14-4eb3-9bb2-18a1e335f77f)


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h> 

int main() {
   
    char *str = (char *)malloc(8 * sizeof(char)); 
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1; 
    }
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0'; 
    printf("The string is: %s\n", str);
    free(str);

    return 0;
}




```
## OUTPUT

![image](https://github.com/user-attachments/assets/eec7fbf2-8d0d-4248-990b-65afc41bcc08)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

// Define a structure to hold student information
struct Student {
    char name[50];     // To store the name of the student
    int rollNumber;    // To store the roll number
    float marks;       // To store the marks
};

int main() {
    int n;
    printf("Enter the number of students: ");
    scanf("%d", &n);
    struct Student students[n];
    for (int i = 0; i < n; i++) {
        printf("\nEnter details for student %d\n", i + 1);
        printf("Enter name: ");
        getchar(); 
        fgets(students[i].name, sizeof(students[i].name), stdin); 
        printf("Enter roll number: ");
        scanf("%d", &students[i].rollNumber);
        printf("Enter marks: ");
        scanf("%f", &students[i].marks);
    }
    printf("\nStudent Information:\n");
    for (int i = 0; i < n; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Name: %s", students[i].name); 
        printf("Roll Number: %d\n", students[i].rollNumber);
        printf("Marks: %.2f\n", students[i].marks);
    }

    return 0;
}



```

## OUTPUT

![image](https://github.com/user-attachments/assets/01ea6c22-73f6-4c49-a459-578c5cb18685)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

// Define a structure to hold employee information
struct Employee {
    char name[50];         // To store the employee's name
    float basicSalary;     // To store the employee's basic salary
    float hra;             // To store House Rent Allowance
    float da;              // To store Dearness Allowance
    float grossSalary;     // To store the calculated gross salary
};

int main() {
    // Declare an array of structures to store information for 3 employees
    struct Employee employees[3];

    // Input data for 3 employees
    for (int i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d\n", i + 1);
        
        // Input the employee's name, basic salary, HRA, and DA
        printf("Enter name: ");
        getchar();  // To clear the newline character left by previous input
        fgets(employees[i].name, sizeof(employees[i].name), stdin);  // Read name with spaces
        printf("Enter basic salary: ");
        scanf("%f", &employees[i].basicSalary);
        printf("Enter HRA (House Rent Allowance): ");
        scanf("%f", &employees[i].hra);
        printf("Enter DA (Dearness Allowance): ");
        scanf("%f", &employees[i].da);

        // Calculate the gross salary: Gross Salary = Basic Salary + HRA + DA
        employees[i].grossSalary = employees[i].basicSalary + employees[i].hra + employees[i].da;
    }

    // Display the employee details along with the calculated gross salary
    printf("\nEmployee Information and Gross Salary:\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name: %s", employees[i].name);  // Name includes newline from fgets
        printf("Basic Salary: %.2f\n", employees[i].basicSalary);
        printf("HRA: %.2f\n", employees[i].hra);
        printf("DA: %.2f\n", employees[i].da);
        printf("Gross Salary: %.2f\n", employees[i].grossSalary);
    }

    return 0;
}




```

 ## OUTPUT
![image](https://github.com/user-attachments/assets/295a0275-1165-489b-a8c7-3609fc43c713)

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```

#include <stdio.h>

// Define a structure to hold student information
struct Student {
    char name[50];         // To store the student's name
    float marks[5];        // To store marks for 5 subjects
    float total;           // To store the total marks
    float average;         // To store the average marks
};

int main() {
    struct Student student;  // Declare a variable of type Student

    // Input student details
    printf("Enter student's name: ");
    getchar();  // To clear the newline character left by previous input
    fgets(student.name, sizeof(student.name), stdin);  // Read student's name (can include spaces)

    // Input marks for 5 subjects
    printf("Enter marks for 5 subjects:\n");
    student.total = 0;  // Initialize total to 0
    for (int i = 0; i < 5; i++) {
        printf("Enter marks for subject %d: ", i + 1);
        scanf("%f", &student.marks[i]);
        student.total += student.marks[i];  // Add marks to total
    }

    // Calculate the average marks
    student.average = student.total / 5;

    // Display the student's details, total marks, and average marks
    printf("\nStudent Details:\n");
    printf("Name: %s", student.name);  // Name includes newline from fgets
    printf("Total Marks: %.2f\n", student.total);
    printf("Average Marks: %.2f\n", student.average);

    return 0;
}

```

## OUTPUT

 ![image](https://github.com/user-attachments/assets/899f4fa4-27c7-49c6-9094-57645b97030a)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


