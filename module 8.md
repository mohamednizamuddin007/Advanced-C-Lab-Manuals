## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
## NAME : MOHAMED NIZAMUDDIN A
## REG NO: 212224040194
#### Aim:
To write a C program print the lowercase English word corresponding to the number
#### Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 41: Print "forty one"
-	Case 42: Print "forty two"
-	Case 43: Print "forty three"
-	...
-	Case 49: Print "forty nine"
-	Default: Print "Greater than 49"
4.	Exit the program.
 
#### Program:
```
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);

    switch(n) {
        case 41: printf("forty one\n"); break;
        case 42: printf("forty two\n"); break;
        case 43: printf("forty three\n"); break;
        case 44: printf("forty four\n"); break;
        case 45: printf("forty five\n"); break;
        case 46: printf("forty six\n"); break;
        case 47: printf("forty seven\n"); break;
        case 48: printf("forty eight\n"); break;
        case 49: printf("forty nine\n"); break;
        default: printf("Greater than 49\n");
    }
    return 0;
}

```
#### Output:
<img width="479" height="227" alt="image" src="https://github.com/user-attachments/assets/f9ebfe6e-6582-4656-81ef-21cbef092beb" />

#### Result:
Thus, the program is verified successfully
 
## EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 9 .
#### Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 9.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 9
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
#### Program:
```
#include <stdio.h>
#include <string.h>


int main() {
    char str[1000];           
    int freq[10] = {0};       
    scanf("%s", str);

    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= '0' && str[i] <= '9') {
            freq[str[i] - '0']++; 
        }
    }
    for (int i = 0; i < 10; i++) {
        printf("%d ", freq[i]);
    }
}
```

#### Output:
<img width="639" height="149" alt="image" src="https://github.com/user-attachments/assets/79ca536f-17a6-4a5b-b4de-7dc854a4a843" />

#### Result:
Thus, the program is verified successfully

## EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
#### Aim:
To write a C program to print all of its permutations in strict lexicographical order.

#### Algorithm:
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
 
#### Program:
```
#include<stdio.h>
#include<string.h>
#include<stdbool.h>
void swap(char a[100],char b[100]){
    char t[100];
    strcpy(t,a);
    strcpy(a,b);
    strcpy(b,t);
}
bool per(char a[][100],int n){
    int k=-1,l;
    for (int i=0;i<n-1;i++){
        if (strcmp(a[i],a[i+1])<0){
            k=i;
        }
    }
    if (k==-1) return false;
    
    for (int i=k+1;i<n;i++){
        if (strcmp(a[k],a[i])<0){
            l=i;
        }
    }
    swap(a[k],a[l]);
    for (int i=k+1,j=n-1;i<j;i++,j--){
        swap(a[i],a[j]);
    }
    return true;
}
int main()
{
    int n;
    scanf("%d",&n);
    char a[n][100];
    for (int i=0;i<n;i++){
        scanf("%s",a[i]);
    }
    do{
        for (int i=0;i<n;i++){
            printf("%s ",a[i]);
        }
        printf("\n");
    }while (per(a,n));
}
```

#### Output:
<img width="329" height="286" alt="image" src="https://github.com/user-attachments/assets/ef56aa57-b619-4728-b532-d5a22f706be1" />

#### Result:
Thus, the program is verified successfully
 
## EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.
#### Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
#### Program:
```
#include<stdio.h>
int main(){
    int n;
    scanf("%d",&n);
    int size=2*n-1;
    for (int i=0;i<size;i++){
        for (int j=0;j<size;j++){
            int min=i<j?i:j;
            min=min<size-i?min:size-i-1;
            min=min<size-j?min:size-j-1;
            printf("%d ",n-min);
        }
        printf("\n");
    }
}
```

#### Output:
<img width="457" height="476" alt="image" src="https://github.com/user-attachments/assets/99ff0818-0f38-4eed-bbce-d7d911ae79f3" />


#### Result:
Thus, the program is verified successfully



## EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

#### Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

#### Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

#### Program:
```
#include <stdio.h>
void square();
int main(){
    
    square();
    return 0;
}
void square(){
    int a;
    scanf("%d",&a);
    float ans = a*a;
    printf("The square of %d is : %.2f",a,ans);
}

```

#### Output:
<img width="1024" height="279" alt="image" src="https://github.com/user-attachments/assets/d1522e5c-8af7-4fe5-accf-f697a392c590" />

#### Result:
Thus, the program is verified successfully.
