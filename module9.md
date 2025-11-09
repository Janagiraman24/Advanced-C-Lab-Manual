## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

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
```C
float stack[100];
int top, i;

void display()
{
    for (i = top; i >= 0; i--) 
    {
        printf("%.1f ", stack[i]);  
    }
}
```
Output:

<img width="837" height="532" alt="11" src="https://github.com/user-attachments/assets/2ed6225f-0630-440e-bed2-99fef72fa7b7" />

Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```C
char stack[100];
int size=3,top=-1;
void push (char data)
{
    if(top==size-1){
        printf("stack is full\n");
    }
    else{
        top=top+1;
        stack[top]=data;
    }
}
```
Output:

<img width="832" height="563" alt="12" src="https://github.com/user-attachments/assets/6c1c4595-918c-4aa3-bc2a-efe5e5e60dac" />

Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```C
float queue[50];
int rear=-1, front=-1;
void display()
{
    if(front==-1||front>rear){
        printf("No elements to display");
        return;
    }
    for(int i=front;i<=rear;i++){
        printf("%.1f\n",queue[i]);
    }
}
```
Output:

<img width="877" height="539" alt="13" src="https://github.com/user-attachments/assets/4671bc4c-1f2a-41c5-a843-78f1a65c868a" />


Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```C
int front,rear,size=10;
char queue[50];
void enqueue(char data)
{
     if(rear<size){
        if(front==-1){
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
     }
}
```
Output:

<img width="887" height="464" alt="14" src="https://github.com/user-attachments/assets/be20d5ba-2e84-4952-8ff2-262dd4340ebc" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



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
```C
int front, rear;
void dequeue()
{
    if(front==-1)
    {
        printf("Queue Underflow.\n");
    }
    else
    {
        front++;
    }
}
```
Output:

<img width="912" height="655" alt="15" src="https://github.com/user-attachments/assets/fa1aec57-ae40-4ed9-89fa-2d4650ffe0c2" />

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
