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
~~~
#include <stdio.h>
void calculateArea(float *length, float *width, float *area) {
    *area = (*length) * (*width);
}
int main() {
    float length, width, area;
    scanf("%f", &length);
    scanf("%f", &width);
    calculateArea(&length, &width, &area);
    printf("Area of rectangle = %f sq. units", area);
    return 0;
}
~~~
<img width="760" height="812" alt="image" src="https://github.com/user-attachments/assets/78906b07-a7d6-4523-b5c4-c1166a13a426" />


## OUTPUT
<img width="926" height="184" alt="image" src="https://github.com/user-attachments/assets/c11fa8a8-8853-42cf-a153-9ee19ef30bd4" />



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
~~~
#include <stdio.h>
#include<stdlib.h>
# include<ctype.h>
# include <string.h>
int main()
{
    char *p=(char *)malloc(7*sizeof(char));
    strcpy(p,"Printer");
    printf("%s",p);
    free(p);
    return 0;
}
~~~
<img width="566" height="745" alt="image" src="https://github.com/user-attachments/assets/521f8847-fa11-4013-89e1-fd8848284708" />

## OUTPUT
<img width="332" height="167" alt="image" src="https://github.com/user-attachments/assets/222b6b2e-c42b-4656-bd7b-566d1c541722" />



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
~~~
#include <stdio.h>
struct student {
    int roll;
    char name[50];
    float marks;
};
int main() {
    struct student s[5];
    int i;
    for(i = 0; i < 5; i++) {
        scanf("%s %f", s[i].name, &s[i].marks);
        s[i].roll = i + 1;   
    }
    printf("Displaying Information:\n");
    for(i = 0; i < 5; i++) {
        printf("Roll number: %d\n", s[i].roll);
        printf("First name: %s\n", s[i].name);
        printf("Marks: %.1f\n\n", s[i].marks);
    }
    return 0;
}
~~~
<img width="671" height="528" alt="image" src="https://github.com/user-attachments/assets/85d509e9-4c8b-4aff-afe9-2e690e4eef07" />

## OUTPUT
<img width="707" height="645" alt="image" src="https://github.com/user-attachments/assets/dd712d37-5def-4638-bd4a-4293f5a56103" />


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
~~~
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basic, hra, da, gross;
};
int main() {
    struct Employee emp[3];
    int i;
    for(i = 0; i < 3; i++) {
        scanf("%[^\n]", emp[i].name);
        scanf("%d", &emp[i].id);
        scanf("%f %f %f", &emp[i].basic, &emp[i].hra, &emp[i].da);
        getchar();
        emp[i].gross = emp[i].basic + emp[i].hra + emp[i].da;
    }
    for(i = 0; i < 3; i++) {
        printf("%s\n", emp[i].name);
        printf("%d\n", emp[i].id);
        printf("%.2f\n", emp[i].gross);
    }
    return 0;
}

~~~


 ## OUTPUT

 <img width="729" height="572" alt="image" src="https://github.com/user-attachments/assets/8a9428b1-54d1-49c6-95e4-58096d280d4a" />


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
~~~
#include <stdio.h>
struct Student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};
int main() {
    struct Student s[2];
    int i, j;
    for(i = 0; i < 2; i++) {
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for(i = 0; i < 2; i++) {
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    for(i = 0; i < 2; i++) {
        printf("%d %.2f\n", s[i].total, s[i].average);
    }
    return 0;
}

~~~

## OUTPUT
<img width="836" height="474" alt="image" src="https://github.com/user-attachments/assets/a74899c2-ea24-4274-ad8c-025c0e827d5a" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


