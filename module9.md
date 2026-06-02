EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

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
```
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top = -1;

void push(int value) {
    if(top == MAX - 1)
        printf("Stack Overflow\n");
    else
        stack[++top] = value;
}

void display() {
    int i;
    if(top == -1)
        printf("Stack is Empty\n");
    else {
        printf("Stack Elements are: ");

        for(i = top; i >= 0; i--)
            printf("%d ", stack[i]);
    }
}

int main() {
    int n, i, value;
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        scanf("%d", &value);
        push(value);
    }

    display();
    return 0;
}
```


Output:
<img width="917" height="812" alt="image" src="https://github.com/user-attachments/assets/f3fe5094-3efa-490a-8882-48ebd7359e7b" />

Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

Aim: To create a C function to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
~~~
int size=3,top=1;
float stack[100];
void push (float data) {
    if (top==size-1)
        printf("stack is full\n");
    else
        stack[++top] = data;
}
~~~

Output:
<img width="672" height="900" alt="image" src="https://github.com/user-attachments/assets/fee7d83e-e8fa-45c5-ad27-2b13409063b6" />

Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

Aim:To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
int queue[50], rear=-1, front=-1;
void display() {
    int i;
    if(front==-1||front>rear)
    printf("No elements to display\n");
    else {
        for(i=front;i<=rear;i++)
            printf("%d\n",queue[i]);
    }
}
```
Output:
<img width="708" height="775" alt="image" src="https://github.com/user-attachments/assets/86c1af69-38d8-4298-8914-2fc4e6917075" />

Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
int queue[50];
int rear, front, size=10;
void enqueue(int data) {
    if (front==-1)
        front++;
    queue[++rear]=data;
}
```
Output:
<img width="803" height="752" alt="image" src="https://github.com/user-attachments/assets/ab659ae5-e651-490d-b9f4-346bf237a1d2" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.

EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

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
```
int front, rear;
void dequeue() {
    if(front==-1)
        printf("Queue Underflow.\n");
    else
        front++;
}
```

Output:
<img width="722" height="782" alt="image" src="https://github.com/user-attachments/assets/e9ab8e4a-e912-40f6-b28c-e3feaf116562" />

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
