## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
## NAME : MOHAMED NIZAMUDDIN A
## REG NO : 212224040194
#### Aim:
To write a C program to search a given element in the given linked list.

#### Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
#### Program:
```
struct Node{
    float data; 
    struct Node *next;
}*head;

void search(float data)
{
    struct Node *ptr;
    int i=1,flag=0;
    ptr=head;
    if (ptr==NULL){
        printf("\nEmpty List\n");
    }
    else{
        while(ptr!=NULL){
            if (ptr->data==data){
                printf("item %.2f found at location %d",data,i);
                flag=1;
                break;
            }
            i++;
            ptr=ptr->next;
       }
       if (flag==0){
           printf("Item not found\n");
       }
    }
}
```

#### Output:

<img width="658" height="289" alt="image" src="https://github.com/user-attachments/assets/dcf6b69d-e369-4433-a976-5e83c9f46b6c" />


#### Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
#### Aim:
To write a C program to insert a node in a linked list.
#### Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
#### Program:
```
struct Node{
    int data; 
    struct Node *next;
}*head;


void insert(int data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node *temp;
    
    if (head==NULL){
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

#### Output:

<img width="294" height="364" alt="image" src="https://github.com/user-attachments/assets/0acd2afd-3406-4b79-951c-522e22987f15" />


#### Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
#### Aim:
To write a C program to traverse a doubly linked list.

#### Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
#### Program:
```
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
    while (ptr!=NULL){
        printf("%.2f ",ptr->data);
        ptr=ptr->next;
    }
}
```

#### Output:
<img width="495" height="351" alt="image" src="https://github.com/user-attachments/assets/a7173b0b-bae7-4b3f-8cef-0042f5c0b09f" />

#### Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
#### Aim:
To write a C program to insert an element in doubly linked list

#### Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
#### Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *ptr,*temp;
    ptr=(struct Node *)malloc(sizeof(struct Node));
    if (ptr==NULL){
        printf("OVERFLOW\n");
        
    }
    else{
        ptr->data=data;
        if (head==NULL){
            ptr->next=NULL;
            ptr->prev=NULL;
            head=ptr;
        }
        else{
            temp=head;
            while (temp->next!=NULL){
                temp=temp->next;
            }
            temp->next=ptr;
            ptr->prev=temp;
            ptr->next=NULL;
        }
    }
}
```
#### Output:
<img width="496" height="348" alt="image" src="https://github.com/user-attachments/assets/e100a84f-fc8c-498b-bea2-43a2b999387a" />

#### Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

#### Aim:
To write a C function that deletes a given element from a linked list.

#### Algorithm:
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


#### Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void delete()
{
    struct Node *ptr;
    if (head==NULL){
        printf("UNDERFLOW\n");
    }
    else if (head->next==NULL){
        head=NULL;
        free(head);
        printf("Node deleted\n");
    }
    else{
        ptr=head;
        head=head->next;
        head->prev=NULL;
        free(ptr);
        printf("Node deleted\n");
    }  
}
```

#### Output:
<img width="555" height="377" alt="image" src="https://github.com/user-attachments/assets/9e1f2ab6-a5dd-466c-8310-c85932246cf8" />



#### Result:
Thus, the function that deletes a given element from a linked list is verified successfully.
