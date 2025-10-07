## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
## NAME : MOHAMED NIZAMUDDIN A
## REG NO : 212224040194
#### Aim:
To write a C program to create a function to find the greatest number

#### Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
#### Program:
```
#include <stdio.h>
int max(int x, int y) {
    return (x > y) ? x : y;
}
int max_of_four(int a, int b, int c, int d) {
    return max(max(a, b), max(c, d));
}

int main() {
    int a, b, c, d;
    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);
    scanf("%d", &d);
    printf("%d\n", max_of_four(a, b, c, d));

    return 0;
}
```

#### Output:
<img width="243" height="223" alt="image" src="https://github.com/user-attachments/assets/7d33e89d-075d-4603-87f8-add4946bafdc" />


#### Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
#### Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

#### Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
#### Program:
```
#include<stdio.h>
void calculate_the_maximum(int n,int k){
    int max_and=0,max_or=0,max_xor=0;
    
    for (int a=1;a<=n;a++){
        for (int b=a+1;b<=n;b++){
            int and_val=a&b;
            int or_val=a|b;
            int xor_val=a^b;
            
            if (and_val<k && and_val>max_and) max_and=and_val;
            if (or_val<k && or_val>max_or) max_or=or_val;
            if (xor_val<k && xor_val>max_xor) max_xor=xor_val;
        }
    }
    printf("%d\n%d\n%d",max_and,max_or,max_xor);
}
int main(){
    int n,k;
    scanf("%d %d",&n,&k);
    calculate_the_maximum(n,k);    
}
```


#### Output:
<img width="246" height="257" alt="image" src="https://github.com/user-attachments/assets/fe358888-a4a6-474b-9460-63ff6c0068b6" />



#### Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
#### Aim:
To write a C program to write the logic for the requests

#### Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
#### Program:
```
#include <stdio.h>
#define MAX_BOOKS 1100

int main() {
    int n;
    scanf("%d", &n);

    int a[n][MAX_BOOKS]; 
    int top[n];           

    for (int i = 0; i < n; i++)
        top[i] = 0;

    int c;
    scanf("%d", &c);

    for (int i = 0; i < c; i++) {
        int ch, x, y;
        scanf("%d", &ch);

        if (ch == 1) {
            scanf("%d%d", &x, &y);
            a[x][top[x]] = y;
            top[x]++;
        } else if (ch == 2) {
            scanf("%d%d", &x, &y);
            printf("%d\n", a[x][y]);
        } else if (ch == 3) {
            scanf("%d", &x);
            printf("%d\n", top[x]);
        }
    }

    return 0;
}
```

#### Output:
<img width="254" height="197" alt="image" src="https://github.com/user-attachments/assets/1a6ce552-de04-46d6-b095-d43ede6a401c" />



#### Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
#### Aim:
To write a C program print the sum of the integers in the array.

#### Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



#### Program:
```
#include<stdio.h>
#include<stdlib.h>

int main(){
    int n,i,sum=0;
    scanf("%d",&n);
    int *arr=(int *)malloc(n*sizeof(int));
    for(i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    for(i=0;i<n;i++){
        sum+=arr[i];
    }
    printf("%d",sum);
}
```

#### Output:

<img width="350" height="153" alt="image" src="https://github.com/user-attachments/assets/c805d494-95ac-4af1-8e2f-58abbe4fa806" />

 


#### Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

#### Aim:

To write a C program that counts the number of words in a given sentence.

#### Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



#### Program:
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[200];
    int count=0;
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    
    for (int i=0;str[i]!=0;i++){
        if (str[i]==' '&& str[i+1]!=' ' && str[i+1]!='\0'){
            count++;
        }
    }
    if (strlen(str)>0){
        count++;
    }
    printf("Total number of words in the string is :%d ",count);
}
```

#### Output:
<img width="818" height="118" alt="image" src="https://github.com/user-attachments/assets/18b0d7e9-acc1-43a1-8b23-6238a2cc5320" />



#### Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
