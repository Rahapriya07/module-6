# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## Name:Raha Priya Dharshini M
## Reg no.:212224240124
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
    int length, width;
    int *ptrLength = &length;
    int *ptrWidth = &width;
    int area;

    printf("Enter length and width of the rectangle:\n");
    scanf("%d %d", ptrLength, ptrWidth);

    area = (*ptrLength) * (*ptrWidth);

    printf("Area of the rectangle: %d\n", area);

    return 0;
}
```

## OUTPUT
![Screenshot 2025-05-23 002644](https://github.com/user-attachments/assets/8d71cfa0-2f99-4322-a18d-5933564e7213)

		       	


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
        printf("Memory allocation failed.\n");
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

    printf("%s\n", str);

    free(str);  

    return 0;
}
```

## OUTPUT
![Screenshot 2025-05-23 002819](https://github.com/user-attachments/assets/548449f0-6d92-4afc-8bec-7584c7a215b8)



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully

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

struct Student {
    char name[50];
    int roll;
    float marks;
};

int main() {
    struct Student s;

    printf("Enter name: ");
    fgets(s.name, sizeof(s.name), stdin);

    printf("Enter roll number: ");
    scanf("%d", &s.roll);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s", s.name);
    printf("Roll Number: %d\n", s.roll);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```

## OUTPUT
![Screenshot 2025-05-23 003407](https://github.com/user-attachments/assets/bd6bd495-e93c-4dc4-aff3-cb4133950108)


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

struct Employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct Employee emp[3];
    int i;

    for (i = 0; i < 3; i++) {
        printf("Enter details of employee %d\n", i + 1);

        printf("Name: ");
        getchar();  
        fgets(emp[i].name, sizeof(emp[i].name), stdin);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);

        emp[i].gross_salary = emp[i].basic_salary + (0.1 * emp[i].basic_salary) + (0.15 * emp[i].basic_salary);
    }

    printf("\nEmployee Details with Gross Salary:\n");
    for (i = 0; i < 3; i++) {
        printf("Name: %s", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Gross Salary: %.2f\n\n", emp[i].gross_salary);
    }

    return 0;
}
```


 ## OUTPUT
 ![Screenshot 2025-05-23 003757](https://github.com/user-attachments/assets/7c074c72-9b47-4586-86d9-dd2470f2127e)


 

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

Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input and iteration.

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

struct student {
    char name[50];     
    int rollno;         
    int subject[5];
    int total;
    float average;
};

int main() {
    struct student s[2];
    int i, j;

    for (i = 0; i < 2; i++) {
        printf("Enter marks of 5 subjects for student %d:\n", i + 1);
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0f;
    }

    for (i = 0; i < 2; i++) {
        printf("Student %d Total Marks = %d\n", i + 1, s[i].total);
        printf("Student %d Average Marks = %.2f\n", i + 1, s[i].average);
    }

    return 0;
}
```

## OUTPUT
![Screenshot 2025-05-23 004552](https://github.com/user-attachments/assets/2bbccff9-53c5-40fd-a344-f4a934ce9d51)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


