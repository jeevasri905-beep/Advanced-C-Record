EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
struct Node{
    int data;
    struct Node *next;
}*head;

void search(int data)
{
    int flag=0, count=1;
    struct Node *ptr= head;
    if(ptr == NULL) {
        printf("\nEmpty List\n");
        return;
    }
    while (ptr) {
        if(ptr->data == data) {
            printf("item %d found at location %d ",data,count);
            flag=1;
        }
        count++;
        ptr = ptr->next;
    }
    if (flag==0)
        printf("Item not found");
}
```
Output:
<img width="852" height="752" alt="image" src="https://github.com/user-attachments/assets/902d5982-74d7-4dff-8dfe-ec05ba4ea4fc" />


Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.

Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```
struct Node{
    char data; 
    struct Node *next;
}*head;

void insert(char data) {
    struct Node *nnode=(struct Node*)malloc(sizeof(struct Node));
    nnode->data=data;
    nnode->next=NULL;
    struct Node *temp=head;
    if (head==NULL) {
        head=nnode;
        return;
    }
    while(temp && temp->next)
        temp=temp->next;
    temp->next=nnode;    
}
```
Output:
<img width="618" height="900" alt="image" src="https://github.com/user-attachments/assets/1f14bba2-03fd-4899-a427-3e3c95fdb4f4" />

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```
struct Node {
    char data;
    struct Node *prev;
    struct Node *next;
}*head;

void display() {
    struct Node *temp = head;
    while(temp){
        printf("%c ", temp->data);
        temp = temp->next;
    }   
}
```
Output:
<img width="608" height="507" alt="image" src="https://github.com/user-attachments/assets/3c2cc67f-7b7f-455f-aa2f-ad321b5e907a" />

Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *temp, *pt;
    pt=(struct Node*)malloc(sizeof(struct Node));
    pt->data=data;
    pt->prev=NULL;
    pt->next=NULL;
    
    if (head==NULL)
        head=pt;
    else {
        temp=head;
        while(temp->next) 
            temp=temp->next;
        temp->next=pt;
        pt->prev=temp;
    }
}
```
Output:
<img width="612" height="750" alt="image" src="https://github.com/user-attachments/assets/f81a68c7-1f86-43cb-b8a0-c28d7b2b5c2f" />

Result:
Thus, the program to insert an element in doubly linked list is verified successfully.

EXP NO:20 C FUNCTION TO DELETE AN ELEMENT IN THE GIVEN LINKED LIST

Aim:
To write a C function that deletes the first element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
6.	End the Function.


Program:
```
struct Node {
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void delete() {
    struct Node *temp=head;
    if (head==NULL)
        printf("UNDERFLOW");
    else {
        printf("Node deleted\n");
        head=head->next;
        free(temp);
    }
}
```
Output:
<img width="1062" height="797" alt="image" src="https://github.com/user-attachments/assets/55b1a3ea-4e86-47db-8175-a15ba420ce8a" />

Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





