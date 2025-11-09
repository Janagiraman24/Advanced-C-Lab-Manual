

## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```C
#include <stdio.h>

int max_of_four(int a, int b, int c, int d) {
    int max = a;
    if(b > max) max = b;
    if(c > max) max = c;
    if(d > max) max = d;
    return max;
}

int main() {
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    printf("%d\n", max_of_four(a, b, c, d));
    return 0;
}
```

Output:

<img width="479" height="349" alt="21" src="https://github.com/user-attachments/assets/804d126e-abb0-453d-9f20-7db7eaa62c37" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
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
```C
#include <stdio.h>

void calculate_the_maximum(int n, int k) {
    int max_and=0, max_or=0, max_xor=0;
    for(int i=1;i<=n;i++){
        for(int j=i+1;j<=n;j++){
            if((i&j)<k && (i&j)>max_and) max_and=i&j;
            if((i|j)<k && (i|j)>max_or)  max_or=i|j;
            if((i^j)<k && (i^j)>max_xor) max_xor=i^j;
        }
    }
    printf("%d\n%d\n%d\n", max_and, max_or, max_xor);
}

int main(){
    int n,k;
    scanf("%d %d",&n,&k);
    calculate_the_maximum(n,k);
    return 0;
}
```

Output:

<img width="552" height="390" alt="22" src="https://github.com/user-attachments/assets/fc523228-ab7a-4510-ad20-341ba5bddfb3" />


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```C

#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, q;
    scanf("%d %d", &n, &q);

    int *count = (int*)calloc(n, sizeof(int));
    int **shelf = (int**)malloc(n * sizeof(int*));
    for(int i=0;i<n;i++) shelf[i] = (int*)malloc(1000 * sizeof(int));

    while(q--){
        int type, x, y;
        scanf("%d", &type);
        if(type==1){
            scanf("%d %d", &x, &y);
            shelf[x][count[x]++] = y;
        }
        else if(type==2){
            scanf("%d %d", &x, &y);
            printf("%d\n", shelf[x][y]);
        }
        else{
            scanf("%d", &x);
            printf("%d\n", count[x]);
        }
    }

    for(int i=0;i<n;i++) free(shelf[i]);
    free(shelf);
    free(count);
    return 0;
}
```

Output:

<img width="471" height="258" alt="23" src="https://github.com/user-attachments/assets/a294a2f3-717f-4d76-958e-70e103f186e6" />


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
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
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);

    int *arr = (int *)malloc(n * sizeof(int));  
    if (arr == NULL) return 1;  

    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }

    printf("%d", sum);
    free(arr);  
    return 0;
}
```

Output:

<img width="600" height="252" alt="24" src="https://github.com/user-attachments/assets/799e6f2e-d615-4256-9482-a2f9af94d715" />


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE


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
```C
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[1000];
    int i, words = 0;
        fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = '\0';
    for (i = 0; str[i] != '\0'; i++) {
        if ((i == 0 && !isspace(str[i])) || 
            (isspace(str[i - 1]) && !isspace(str[i]))) {
            words++;
        }
    }

    printf("Total number of words in the string is :%d\n", words);
    return 0;
}
```

Output:

<img width="1123" height="202" alt="25" src="https://github.com/user-attachments/assets/8f8a5178-93ed-435d-bc28-eddfa4888a43" />

Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
