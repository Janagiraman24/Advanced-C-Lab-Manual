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

```
#include <stdio.h>

struct person {
    int age;
    char name[10];
};

int main() {
    struct person p;
    scanf("%d %s", &p.age, p.name);
    printf("Age:%d\n", p.age);
    printf("Name:%s", p.name);
    printf("vaccine:%d\n", p.age); 
    printf("eligibility:");

    if (p.age > 18) {
        printf("yes");
    } else {
        printf("no");
    }

    return 0;
}
```

Output:

<img width="1161" height="318" alt="image" src="https://github.com/user-attachments/assets/40c253cf-6831-4ad5-8c21-79afd144f2c6" />


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

```
#include <stdio.h>
struct Input
{
    int x;
    int y;
};

struct Output
{
    int sum;
};

struct Output add(struct Input in) 
{
    struct Output out;
    out.sum = in.x + in.y;
    return out;
}

int main() {
    struct Input values;
    struct Output result;
    scanf("%d", &values.x);
    scanf("%d", &values.y);
    result = add(values);
    printf("%d\n", result.sum);

    return 0;
}
```



Output:


<img width="884" height="316" alt="image" src="https://github.com/user-attachments/assets/4ac0aa2d-c5d2-4538-b537-f47487a7aa62" />




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
```
#include <stdio.h>
int main()
{
    FILE *fp;
    char name[20];
    scanf("%s",name);
    fp=fopen(name,"w");
    if(fp==NULL)
    {
        printf("error checking");
    }
    else
    {
        printf("%s File Created Successfully\n%s File Opened\n",name,name);
    }
    fclose(fp);
    printf("%s File Closed\n",name);
}
```



Output:


<img width="1044" height="384" alt="image" src="https://github.com/user-attachments/assets/438de3c5-22b3-40ba-bb57-585a4466246d" />


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

```
#include <stdio.h>

int main() {
    char filename[100];
    char line[100];
    int n, i;
    FILE *file;
    scanf("%s", filename);
    file = fopen(filename, "w");

    if (file == NULL) 
    {
        printf("Error: Could not create %s\n", filename);
        return 1;
    }
    scanf("%d", &n);
    getchar();
    for (i = 0; i < n; i++) {
        fgets(line, sizeof(line), stdin); 
        fputs(line, file);                
    }

  
    fclose(file);
    printf("%s Opened\n", filename);
    printf("Data added Successfully\n");

    return 0;
}
```



Output:


<img width="845" height="373" alt="image" src="https://github.com/user-attachments/assets/0e7affcb-7995-412d-96fd-9d9d0102889a" />



Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, 
and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

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

```
#include <stdio.h>

#define TOTAL_WORKING_DAYS 84
#define MAX_DAYS_PER_MONTH 21

struct Student {
    int regNo;
    char name[50];
    int june;
    int july;
    int august;
    int september;
    int totalPresent;
    float attendancePercentage;
    char eligibility[4]; 
};

int main() {
    struct Student s;
    scanf("%d", &s.regNo);
    scanf("%s", s.name);
    scanf("%d", &s.june);
    scanf("%d", &s.july);
    scanf("%d", &s.august);
    scanf("%d", &s.september);
    
    if (s.june > MAX_DAYS_PER_MONTH || s.july > MAX_DAYS_PER_MONTH ||
        s.august > MAX_DAYS_PER_MONTH || s.september > MAX_DAYS_PER_MONTH) 
        {
        printf("Error: Days present in any month should not exceed 21.\n");
        return 1;
    }

    s.totalPresent = s.june + s.july + s.august + s.september;
    
    s.attendancePercentage = (s.totalPresent / (float)TOTAL_WORKING_DAYS) * 100;
    
    if (s.attendancePercentage > 75.0)
        sprintf(s.eligibility, "yes");
    else
        sprintf(s.eligibility, "no");
        
    printf("Reg.no:%d\n", s.regNo);
    printf("Name:%s\n", s.name);
    printf("Total.No.of.present days:%d\n", s.totalPresent);
    printf("Attendence:%.2f\n", s.attendancePercentage);
    printf("eligibility:%s\n", s.eligibility);

    return 0;
}

```



Output:


<img width="848" height="432" alt="image" src="https://github.com/user-attachments/assets/0175a816-1a2a-4807-aac0-f5d4e31e293e" />


Result:

Thus, the program is verified successfully
