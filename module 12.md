# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## NAME : MOHAMED NIZAMUDDIN A
## REG NO : 212224040194
#### Aim:
To write a C program to display stack elements using linked list.

#### Algorithm:
1.	Define a structure Node with two members: data to store the string value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
#### Program:
```
struct Node   
{  
    int data;  
    struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp = head;
    while (temp!=NULL){
        printf("%c\n",temp->data);
        temp=temp->next;
    }
}
```

#### Output:
<img width="279" height="325" alt="image" src="https://github.com/user-attachments/assets/db7c2dfc-0fc3-4a9c-a802-4f1b10843a62" />


#### Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
#### Aim:
To write a C program to pop an element from the given stack using liked list.

#### Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
#### Program:
```
struct Node   
{  
    int data;  
    struct Node *next;  
}*head;  

void pop()  
{ 
    struct Node *ptr;
    if (head==NULL){
        printf("stack is empty\n");
    }
    else{
        ptr=head;
        head=ptr->next;
        free(ptr);
    }
}
```

#### Output:
<img width="607" height="317" alt="image" src="https://github.com/user-attachments/assets/038db375-7e32-4deb-8bcf-248a1f405e0f" />




#### Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
#### Aim:
To write a C program to display queue elements using linked list.
#### Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
#### Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    
    if(front!=NULL){
        printf("queue elements:\n");
        while (front!=NULL){
            printf("%.2f\n",front->data);
            front=front->next;
        }
    }
    else{
        printf("queue is empty");
    }
}
```


#### Output:
<img width="435" height="359" alt="image" src="https://github.com/user-attachments/assets/0e4add59-3619-4fe8-9a09-a80d6763e468" />


#### Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

#### Aim:
To write a C program to insert elements in queue using linked list

#### Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
#### Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *newNode;
    newNode=(struct Node *)malloc(sizeof(struct Node));
    newNode->data=data;
    newNode->next=NULL;
    if (front==NULL){
        front=rear=newNode;
    }
    else{
        rear->next=newNode;
        rear=newNode;
    }
}
```



#### Output:
<img width="408" height="363" alt="image" src="https://github.com/user-attachments/assets/812c964a-fd50-435e-949d-3fffa0947eda" />


#### Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


#### Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

#### Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

#### Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%.2f",front->data);
}
```

#### Output:

<img width="331" height="383" alt="image" src="https://github.com/user-attachments/assets/a6375ec9-d18d-4720-9860-b2b5b417ccfa" />


#### Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
