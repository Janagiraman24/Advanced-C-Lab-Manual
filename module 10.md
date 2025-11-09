## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```C
struct Node{
    int data; 
    struct Node *next;
}*head;

void search(int data)
{
    struct Node *ptr;
    ptr=head;
    int item=data;
    int i=1,flag;
    if(ptr==NULL){
        printf("List is empty");
    }
    else{
        while(ptr!=NULL){
            if(ptr->data==item){
                printf("item %d found at location %d",item,i);
                flag=0;
                break;
            }
            else{
                flag=1;
            }
            i++;
            ptr=ptr->next;
        }
        if(flag==1){
            printf("Item not found");
        }
        
    }
}
```
Output:
<img width="773" height="535" alt="16" src="https://github.com/user-attachments/assets/3a97a86e-6cd1-4f00-a179-08b6e1d2b7e9" />

Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```C
struct Node{
    int data; 
    struct Node *next;
}*head;

void insert(int data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL){
        head=n;
        head->data=data;
        n->next=NULL;
        return;
    }
    temp=head;
    while(temp->next!=NULL){
        temp=temp->next;
    }
    n->data=data;
    n->next=NULL;
    temp->next=n;
    
}
```
Output:
<img width="759" height="544" alt="17" src="https://github.com/user-attachments/assets/5b9773e8-edc2-4be5-af28-92fd2c1dfe5d" />

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```C
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    struct Node *ptr;
    ptr=head;
    while(ptr!=NULL){
        printf("%.2f ",ptr->data);
        ptr=ptr->next;
    }
    
}
```
Output:
<img width="772" height="507" alt="18" src="https://github.com/user-attachments/assets/0f2bccdf-4efa-4794-bbee-8b3dd37c2950" />

Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```C
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *ptr,*temp;
    ptr=(struct Node*)malloc(sizeof(struct Node));
    if(ptr==NULL){
        printf("OVERFLOW");
    }
    else{
        ptr->data=data;
        if(head==NULL){
            ptr->next=NULL;
            ptr->prev=NULL;
            head=ptr;
        }
        else{
            temp=head;
            while(temp->next!=NULL){
                temp=temp->next;
            }
            temp->next=ptr;
            ptr->prev=temp;
            ptr->next=NULL;
        }
    }
    
    
    
}
```
Output:
<img width="771" height="513" alt="19" src="https://github.com/user-attachments/assets/b129f8ef-e023-4859-bb58-499d15ec3f90" />

Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST



Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:
```C
struct Node{
    float data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node *ptr;
    ptr=head;
    if(ptr==NULL){
        printf("List is empty");
    }
    else{
    head=head->next;
    free(ptr);
    printf("Node deleted from the begining ...\n");
    }
}
```

Output:
<img width="1136" height="625" alt="20" src="https://github.com/user-attachments/assets/c3a39790-735d-4489-8948-e4f9e95f7092" />

Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





