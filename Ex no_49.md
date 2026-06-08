# EX 49 C function to search an element in the doubly linked list.
## DATE:
## AIM:
To write a C function to search an element in the doubly linked list.

## Algorithm
1. Start.
2. Define a variables.
3. Write a function to perform all basic operations.
4. Read the value using scanf.
5. Ask the user to make an input.
6. Print out the answer.
7. End   

## Program:
```
struct Node
{
struct Node *prev; 
struct Node *next; 
float data;
}*head;
void display()
{
struct Node *temp; 
temp=head;
while(temp!=NULL)
{
printf("%.2f ",temp->data); 
temp=temp->next;
}
}
SAVEETHA ENGINEERING COLLEGE
void insert(float data)
{
struct Node *n=(struct Node*)malloc(sizeof(struct Node)); 
struct Node *temp;
if(head==NULL)
{
head=n;
n->data=data;
n->next=NULL;
n->prev=NULL; 
temp=head;
}
else
{
while(temp->next!=NULL)
{
temp=temp->next;
}
n->data=data;
n->next=NULL; 
n->prev=temp; 
temp->next=n;
}
}
void search(float data)
{
struct Node *temp; 
temp=head;
int i=0,f=0;
while(temp!=NULL)
{
if(temp->data==data)
{
printf("item %.2f found at location %d\n",data,i+1); 
SAVEETHA ENGINEERING COLLEGE
i++;
temp=temp->next;
}
if(f==0)
{
printf("Item not found\n");
}
}
void delete()
{
struct Node *p;
p=head; 
if(p==NULL)
{
printf("UNDERFLOW \n");
}
else if(head->next==NULL)
{
head=NULL; 
free(head);
printf("Node deleted\n");
}
else
{
p=head; 
head=head->next;
head->prev=NULL; 
printf("Node deleted\n");
}
}
```

## Output:

![image](https://github.com/user-attachments/assets/614f33f2-6b5a-4421-a44b-3cb36c8929d2)


## Result:
Thus the program was executed and the output was verified successfully.
