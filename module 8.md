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
```c
int main(){
    int n;
    scanf("%d",&n);
    if(n>=21&&n<=29){
        switch(n){
            case 21:
            printf("twenty one\n");
            break;
            case 22:
            printf("twenty two\n");
            break;
            case 23:
            printf("twenty three\n");
            break;
            case 24:
            printf("twenty four\n");
            break;
            case 25:
            printf("twenty five\n");
            break;
            case 26:
            printf("twenty six\n");
            break;
            case 27:
            printf("twenty three\n");
            break;
            case 28:
            printf("twenty four\n");
            break;
            case 29:
            printf("twenty five\n");
            break;
        }
    }
    else {
        printf("Greater than 29");
    }
}
```
Output:
<img width="670" height="267" alt="Screenshot 2025-10-23 111349" src="https://github.com/user-attachments/assets/8caf5b83-1b66-4f19-88ea-e45cc790fc79" />

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
```c
#include <stdio.h>
#include <ctype.h>

int main() {
    char str[100];
    
    scanf("%s", str);
    
    int frequency[10] = {0};

    for (int i = 0; str[i] != '\0'; i++) {
        if (isdigit(str[i])) {
            int digit = str[i] - '0';
            frequency[digit]++;
        }
    }
    
    for (int i = 0; i < 10; i++) {
        printf("%d ", frequency[i]);
    }
    printf("\n");
    
    return 0;
}
```
Output:
<img width="709" height="223" alt="Screenshot 2025-10-23 111612" src="https://github.com/user-attachments/assets/e89e3a5a-c227-4639-90d2-a82bb7031f2c" />

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
```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

void swap(char **a, char **b) {
    char *temp = *a;
    *a = *b;
    *b = temp;
}

int next_permutation(char *arr[], int n) {
    int i = n - 2;
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0)
        i--;
    if (i < 0)
        return 0;
    int j = n - 1;
    while (strcmp(arr[i], arr[j]) >= 0)
        j--;
    swap(&arr[i], &arr[j]);
    for (int l = i + 1, r = n - 1; l < r; l++, r--)
        swap(&arr[l], &arr[r]);
    return 1;
}

int compare(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}

int main() {
    int n;
    scanf("%d", &n);
    char **arr = (char **)malloc(n * sizeof(char *));
    for (int i = 0; i < n; i++) {
        arr[i] = (char *)malloc(101 * sizeof(char)); // Assuming max length 100
        scanf("%s", arr[i]);
    }
    
    qsort(arr, n, sizeof(char *), compare);
    
    do {
        for (int i = 0; i < n; i++)
            printf("%s%c", arr[i], i == n - 1 ? '\n' : ' ');
    } while (next_permutation(arr, n));
    
    for (int i = 0; i < n; i++)
        free(arr[i]);
    free(arr);
    
    return 0;
}
```
Output:
<img width="615" height="375" alt="Screenshot 2025-10-23 111721" src="https://github.com/user-attachments/assets/a305e7fe-4523-45f6-880f-9cf20afa96a9" />

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
```c
#include<stdio.h>
int main(){
    int n;
    scanf("%d",&n);
    int size=2*n-1;
    for(int i=0;i<size;i++){
        for(int j=0;j<size;j++){
            int value=n-(i<j?(i<size-j-1?i:size-j-1):(j<size-i-1?j:size-i-1));
            printf("%d ",value);
        }
        printf("\n");
    }
}
```
Output:
<img width="996" height="596" alt="Screenshot 2025-10-23 111855" src="https://github.com/user-attachments/assets/62e2dc79-f1c0-45f9-8bfa-948f58a49f49" />


Result:
Thus, the program is verified successfully

EXP NO:10 Given a five digit integer n, print the sum of its digits.

Aim:

To Write Given a five digit integer n, print the sum of its digits.

Algorithm:

1.Input n. 

2.Initialize sum = 0. 

3.Repeat 5 times: digit = n % 10 sum = sum + digit n = n / 10 (integer division) 

4.Print sum.

Program:
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    int d1, d2, d3, d4, d5, sum;
    d1 = n / 10000;          
    d2 = (n / 1000) % 10;   
    d3 = (n / 100) % 10;   
    d4 = (n / 10) % 10;    
    d5 = n % 10;            
    sum = d1 + d2 + d3 + d4 + d5;
    printf("%d\n", sum);
    return 0;
}
```
Output:

<img width="433" height="193" alt="image" src="https://github.com/user-attachments/assets/ee86fd75-415a-4b4c-8bab-76b8e543ed1b" />

Result:
Thus, the program is verified successfully



























