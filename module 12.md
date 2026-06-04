

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
struct Node {  
float data;  
struct Node *next;  
}*head;  

void display() {  
    struct Node*temp=head;
    if(head==NULL){
        printf("No elements to display");
        return;
    }
    while(temp!=NULL){
        printf("%.3f\n",temp->data);
        temp=temp->next;
    }
}
```
Output:
<img width="493" height="761" alt="image" src="https://github.com/user-attachments/assets/5bf562bc-0a99-4ed8-9988-312d3ad39593" />

Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node {  
    double data;  
    struct Node *next;  
}*head;  

void pop() {
    struct Node *temp=head;
    if(head==NULL)
        printf("stack is empty");
    else {
        head=temp->next;
        free(temp);
    }
}
```
Output:<img width="1106" height="827" alt="image" src="https://github.com/user-attachments/assets/d4811c99-704d-46cc-906c-14c01b5add0c" />


Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
struct Node {
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;

void display() {
    if (front==NULL)
        printf("queue is empty");
    else {
        struct Node *temp=front;
        while (temp) {
            printf("%d\n",temp->data);
            temp=temp->next;
        }
    }
}
```
Output:
<img width="601" height="776" alt="image" src="https://github.com/user-attachments/assets/cc74122e-ae03-444a-a924-6b50d244dd04" />

Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
struct Node {
   double data;
   struct Node *next;
}*front=NULL,*rear=NULL;

void enqueue(double data) {
   struct Node *newNode;
   newNode=(struct Node*)malloc(sizeof(struct Node));
   newNode->data=data;
   newNode->next=NULL;
   if(front==NULL) {
      front=newNode;
      rear=newNode;
      
   }
   else {
      rear->next=newNode;
      rear=newNode;
   }
}
```
Output:
<img width="651" height="772" alt="image" src="https://github.com/user-attachments/assets/6725d7af-a706-4aa8-a525-a83c72de698d" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek() {
    if (head==NULL)
        printf("queue is empty");
    else
        printf("%c\n",front->data);
}
```
Output:
<img width="617" height="783" alt="image" src="https://github.com/user-attachments/assets/9d6cc8e1-1cfb-4e30-84a8-624db91285e5" />

Result:
Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


