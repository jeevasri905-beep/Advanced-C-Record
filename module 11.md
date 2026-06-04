

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

Aim: To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

int main() {
    int a, b, c, d, max;
    scanf("%d %d %d %d",&a, &b, &c, &d);
    max=a;
    if (b>max)
        max=b;
    if (c>max)
        max=c;
    if (d>max)
        max=d;
        
    printf("%d",max);
    return 0;
}
```
Output:
<img width="532" height="857" alt="image" src="https://github.com/user-attachments/assets/f14b5455-7fdc-49dc-ad64-e0b08843ae70" />

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

Aim: To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>

void calc(int n, int k) {
    int a = 0, o = 0, x = 0;

    for(int i = 1; i <= n; i++) {
        for(int j = i + 1; j <= n; j++) {
            if((i & j) < k && (i & j) > a)
                a = i & j;

            if((i | j) < k && (i | j) > o)
                o = i | j;

            if((i ^ j) < k && (i ^ j) > x)
                x = i ^ j;
        }
    }
    printf("%d\n", a);
    printf("%d\n", o);
    printf("%d\n", x);
}

int main() {
    int n, k;
    printf("Enter n and k values: ");
    scanf("%d %d", &n, &k);
    calc(n, k);
    return 0;
}
```

Output:
<img width="1192" height="901" alt="image" src="https://github.com/user-attachments/assets/ba1cbd6c-8e8c-4ef4-be76-10f7b5ac76f7" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

Aim: To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int shelves, queries;
    scanf("%d %d", &shelves, &queries);

    int* book_count = (int*)calloc(shelves, sizeof(int));
    int** pages = (int**)malloc(shelves * sizeof(int*));
    for (int i = 0; i < shelves; i++) {
        pages[i] = NULL;
    }
    
    while (queries--) {
        int q_type;
        scanf("%d", &q_type);
        
        if (q_type == 1) {
            int shelf, pg_num;
            scanf("%d %d", &shelf, &pg_num);
            
            int c = book_count[shelf];
            pages[shelf] = (int*)realloc(pages[shelf], (c + 1) * sizeof(int));
            pages[shelf][c] = pg_num;
            book_count[shelf]++;
        } 
        else if (q_type == 2) {
            int shelf, book_idx;
            scanf("%d %d", &shelf, &book_idx);
            printf("%d\n", pages[shelf][book_idx]);
        } 
        else {
            int shelf;
            scanf("%d", &shelf);
            printf("%d\n", book_count[shelf]);
        }
    }

    free(book_count);
    for (int i = 0; i < shelves; i++) {
        free(pages[i]);
    }
    free(pages);
    return 0;
}
```
Output:
<img width="731" height="808" alt="image" src="https://github.com/user-attachments/assets/7e7280fb-1850-4580-b24d-e89e82e4eba3" />

Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

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
```
#include <stdio.h>
#include <stdlib.h>
int main() {
    int n, sum=0;
    scanf("%d", &n);
    int *arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL){
        printf("Memory allocation failed\n");
        return 1; 
    }for (int i = 0; i < n; i++){
        scanf("%d", &arr[i]);
        sum += arr[i];
    }
    printf("%d\n", sum);
    free(arr);
    return 0; 
    
}
```
Output:
<img width="576" height="803" alt="image" src="https://github.com/user-attachments/assets/80e30955-ec0b-43c6-a887-e6ee92029a87" />

Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

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
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char sentence[50];
    int count = 0, inWord = 0;
    fgets(sentence, 200, stdin);

    for (int i = 0; sentence[i] != '\0'; i++) {
        if (!isspace(sentence[i]) && !ispunct(sentence[i])) {
            if (inWord == 0) {
                count++;
                inWord = 1;
            }
        } else
            inWord = 0; 
    }
    printf("Word count: %d\n", count);
    return 0;
}

```

Output:
<img width="747" height="568" alt="image" src="https://github.com/user-attachments/assets/47756a49-7644-4b0c-9df7-412b84afc706" />

Result:
Thus, the program that counts the number of words in a given sentence is verified successfully.
