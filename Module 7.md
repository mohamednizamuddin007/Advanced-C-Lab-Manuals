## EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.
## NAME : MOHAMED NIZAMUDDIN A
## REG NO : 212224040194
#### Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 18 years of age.

#### Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 18
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
#### Program:
```
#include <stdio.h>

struct Person {
    char name[100];
    int age;
};

int main() {
    struct Person p;
    
    scanf("%d", &p.age);      
    scanf("%s", p.name);     

    printf("Age:%d\n", p.age);
    printf("Name:%s", p.name);
    printf("vaccine:%d\n", p.age);

    if (p.age > 18) printf("eligibility:yes\n");
    else printf("eligibility:no\n");
    

    return 0;
}

```

#### Output:

<img width="596" height="250" alt="image" src="https://github.com/user-attachments/assets/0c3b923b-0edb-482e-a36a-2af1d0593c27" />



#### Result:
Thus, the program is verified successfully. 



## EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
#### Aim:
To write a C program for passing structure as function and returning a structure from a function

#### Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
#### Program:

```
#include <stdio.h>
struct numbers {
    int a;
    int b;
};

struct numbers add(struct numbers n) {
    struct numbers result;   
    result.a = n.a + n.b;   
    result.b = 0;           
    return result;
}

int main() {
    struct numbers n, res;

    printf("Enter FIRST number: ");
    scanf("%d", &n.a);
    printf("Enter SECOND number: ");
    scanf("%d", &n.b);

    res = add(n);

    printf("Sum = %d\n", res.a);

    return 0;
}


```




#### Output:

<img width="394" height="163" alt="image" src="https://github.com/user-attachments/assets/a4750e70-e5a1-46ac-a307-2010e33de027" />





#### Result:
Thus, the program is verified successfully


 
## EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

#### Aim:
To write a C program to read a file name from user

#### Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
#### Program:

```
#include <stdio.h>
int main()
{
    char name[100];
    scanf("%s",name);
    FILE *file;
    printf("%s File Created Successfully\n",name);
    file=fopen(name,"w");
    printf("%s File Opened\n",name);
    fclose(file);
    printf("%s File Closed",name);
    
}
```




#### Output:


<img width="860" height="301" alt="image" src="https://github.com/user-attachments/assets/ca6f0c64-cb91-4447-8ac8-d5cc5df121b4" />











#### Result:
Thus, the program is verified successfully.
 


## EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
#### Aim:
To write a C program to read, a file and insert text in that file
#### Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
#### Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fp;
    char filename[100];
    int n;
    float value;

    scanf("%s", filename);

    fp = fopen(filename, "w");
    if (fp == NULL) {
        printf("Error\n");
        return 1;
    }

    printf("%s Opened\n", filename);

    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        scanf("%f", &value);
        fprintf(fp, "%.2f\n", value);
    }

    fclose(fp);

    printf("Data added Successfully\n");
    return 0;
}

```



#### Output:

<img width="591" height="293" alt="image" src="https://github.com/user-attachments/assets/5a3dbc90-4a42-48ef-a3b2-ab1920bef0c4" />







#### Result:
Thus, the program is verified successfully



## Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

#### Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

#### Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

#### Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Subject
{
    char name[20];
    int marks;
};
int main()
{
    int i,n;
    scanf("%d",&n);
    struct Subject *s = (struct Subject *)malloc(n*sizeof(struct Subject));
    if(s==NULL)
    {
        printf("Memory Alocation Failed\n");
        return 1;
    }
    for(i=0;i<n;i++)
    {
        scanf("%s %d",s[i].name,&s[i].marks);
    }
    for(i=0;i<n;i++)
    {
        printf("%s  %d\n",s[i].name,s[i].marks);
    }
    
    free (s);
    
    return 0;
}
```




#### Output:


<img width="401" height="280" alt="image" src="https://github.com/user-attachments/assets/d3f7647f-2161-4d42-9f8a-e0ce493cccf6" />







#### Result:
Thus, the program is verified successfully.
