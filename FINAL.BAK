#include<iostream.h>
#include<conio.h>
#include<stdlib.h>
//linked list
//**********************************************************************************************************************
//**********************************************************************************************************************
   //single linked list
   struct NODE
{
int data;
struct NODE *next;
};
struct NODE *Start = NULL;
struct NODE *Create_ll(struct NODE *);
struct NODE *Display(struct NODE *);
struct NODE *Insert_beg(struct NODE *);
struct NODE *Insert_end(struct NODE *);
struct NODE *Insert_before(struct NODE *);
struct NODE *Insert_after(struct NODE *);
struct NODE *Delete_beg(struct NODE *);
struct NODE *Delete_end(struct NODE *);
struct NODE *Delete_NODE(struct NODE *);
struct NODE *Delete_after(struct NODE *);
struct NODE *Delete_list(struct NODE *);
struct NODE *sort_list(struct NODE *);

   struct NODE *Create_ll(struct NODE *Start)
{
struct NODE *new_NODE, *ptr;
int num;
cout<<"\n Enter -1 to end";
cout<<"\n Enter the data : ";
cin>>num;
while(num!=-1)
{
new_NODE = (struct NODE*)malloc(sizeof(struct NODE));
new_NODE -> data=num;
if(Start==NULL)
{
new_NODE -> next = NULL;
Start = new_NODE;
}
else
{
ptr=Start;
while(ptr->next!=NULL)
 ptr=ptr->next;
 ptr->next = new_NODE;
 new_NODE->next=NULL;
 }
 cout<<"\n Enter the data :";
 cin>>num;
}
return Start;
}
struct NODE *Display(struct NODE *Start)
{
struct NODE *ptr;
ptr = Start;
while(ptr != NULL)
{
 cout<<"\t %d"<< ptr -> data;
 ptr = ptr -> next;
}
return Start;
}
struct NODE *Insert_beg(struct NODE *Start)
{
struct NODE *new_NODE;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_NODE = (struct NODE *)malloc(sizeof(struct NODE));
new_NODE -> data = num;
new_NODE -> next = Start;
Start = new_NODE;
return Start;
}
struct NODE *Insert_end(struct NODE *Start)
{
struct NODE *ptr, *new_NODE;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_NODE = (struct NODE *)malloc(sizeof(struct NODE));
new_NODE -> data = num;
new_NODE -> next = NULL;
ptr = Start;
while(ptr -> next != NULL)
ptr = ptr -> next;
ptr -> next = new_NODE;
return Start;
}
struct NODE *Insert_before(struct NODE *Start)
{
struct NODE *new_NODE, *ptr, *preptr;
int num, val;
cout<<"\n Enter the data :";
cin>>num;
cout<<"\n Enter the value before which the data has to be inserted : ";
cin>>val;
new_NODE = (struct NODE *)malloc(sizeof(struct NODE));
new_NODE -> data = num;
ptr = Start;
while(ptr -> data != val)
{
preptr = ptr;
ptr = ptr -> next;
}
preptr -> next = new_NODE;
new_NODE -> next = ptr;
return Start;
}
struct NODE *Insert_after(struct NODE *Start)
{
struct NODE *new_NODE, *ptr, *preptr;
int num, val;
cout<<"\n Enter the data : ";
cin>>num;
cout<<"\n Enter the value after which the data has to be inserted : ";
cin>>val;
new_NODE = (struct NODE *)malloc(sizeof(struct NODE));
new_NODE -> data = num;
ptr = Start;
preptr = ptr;
while(preptr -> data != val)
{
preptr = ptr;
ptr = ptr -> next;
}
preptr -> next=new_NODE;
new_NODE -> next = ptr;
return Start;
}
struct NODE *Delete_beg(struct NODE *Start)
{
struct NODE *ptr;
ptr = Start;
Start = Start -> next;
free(ptr);
return Start;
}
struct NODE *Delete_end(struct NODE *Start)
{
struct NODE *ptr, *preptr;
ptr = Start;
while(ptr -> next != NULL)
{
preptr = ptr;
ptr = ptr -> next;
}
preptr -> next = NULL;
free(ptr);
return Start;
}
struct NODE *Delete_NODE(struct NODE *Start)
{
struct NODE *ptr, *preptr;
int val;
cout<<"\n Enter the value of the NODE which has to be deleted :";
cin>>val;
ptr = Start;
if(ptr -> data == val)
{
Start = Delete_beg(Start);
return Start;
}
else
{
while(ptr -> data != val)
 {
 preptr = ptr;
 ptr = ptr -> next;
 }
 preptr -> next = ptr -> next;
 free(ptr);
 return Start;
}
}
struct NODE *Delete_after(struct NODE *Start)
{
struct NODE *ptr, *preptr;
int val;
cout<<"\n Enter the value after which the NODE has to deleted : ";
cin>>val;
ptr = Start;
preptr = ptr;
while(preptr -> data != val)
{
 preptr = ptr;
 ptr = ptr -> next;
}
preptr -> next=ptr -> next;
free(ptr);
return Start;
}
struct NODE *Delete_list(struct NODE *Start)
{
	 struct NODE *ptr; // Lines 252-254 were modified from original code to fix unresposiveness in output window
if(Start!=NULL){
 ptr=Start;
 while(ptr != NULL)
 {
 cout<<"\n %d is to be deleted next"<<ptr -> data;
 Start = Delete_beg(ptr);
ptr = Start;
 }
}
return Start;
}
struct NODE *sort_list(struct NODE *Start)
{
struct NODE *ptr1, *ptr2;
int temp;
ptr1 = Start;
while(ptr1 -> next != NULL)
{
 ptr2 = ptr1 -> next;
 while(ptr2 != NULL)
 {
 if(ptr1 -> data > ptr2 -> data)
 {
 temp = ptr1 -> data;
 ptr1 -> data = ptr2 -> data;
 ptr2 -> data = temp;
 }
 ptr2 = ptr2 -> next;
 }
 ptr1 = ptr1 -> next;
}
return Start; // Had to be added
}
   //end of single linked list
   //double linked list
      struct node
{
struct node *next;
int data;
struct node *prev;
};
struct node *start = NULL;
struct node *create_ll(struct node *);
struct node *display(struct node *);
struct node *insert_beg(struct node *);
struct node *insert_end(struct node *);
struct node *insert_before(struct node *);
struct node *insert_after(struct node *);
struct node *delete_beg(struct node *);
struct node *delete_end(struct node *);
struct node *delete_before(struct node *);
struct node *delete_after(struct node *);
struct node *delete_list(struct node *);

struct node *create_ll(struct node *start)
{
struct node *new_node, *ptr;
int num;
cout<<"\n Enter -1 to end";
cout<<"\n Enter the data : ";
cin>>num;
while(num != -1)
{
if(start == NULL)
{
new_node = (struct node*)malloc(sizeof(struct node));
new_node -> prev = NULL;
new_node -> data = num;
new_node -> next = NULL;
start = new_node;
}
else
{
ptr=start;
new_node = (struct node*)malloc(sizeof(struct node));
new_node->data=num;
while(ptr->next!=NULL)
ptr = ptr->next;
ptr->next = new_node;
new_node->prev=ptr;
new_node->next=NULL;
}
cout<<"\n Enter the data : ";
cin>>num;
}
return start;
}
struct node *display(struct node *start)
{
struct node *ptr;
ptr=start;
while(ptr!=NULL)
{
cout<<ptr -> data;
ptr = ptr -> next;
}
return start;
}
struct node *insert_beg(struct node *start)
{
struct node *new_node;
int
 num;
cout<<"\n Enter the data : ";
cin>>num;
new_node = (struct node *)malloc(sizeof(struct node));
new_node -> data = num;
start -> prev = new_node;
new_node -> next = start;
new_node -> prev = NULL;
start = new_node;
return start;
}
struct node *insert_end(struct node *start)
{
struct node *ptr, *new_node;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_node = (struct node *)malloc(sizeof(struct node));
new_node -> data = num;
ptr=start;
while(ptr -> next != NULL)
ptr = ptr -> next;
ptr -> next = new_node;
new_node -> prev = ptr;
new_node -> next = NULL;
return start;
}
struct node *insert_before(struct node *start)
{
struct node *new_node, *ptr;
int num, val;
cout<<"\n Enter the data : ";
cin>>num;
cout<<"\n Enter the value before which the data has to be inserted:";
cin>>val;
new_node = (struct node *)malloc(sizeof(struct node));
new_node -> data = num;
ptr = start;
while(ptr -> data != val)
ptr = ptr -> next;
new_node -> next = ptr;
new_node -> prev = ptr-> prev;
ptr -> prev -> next = new_node;
ptr -> prev = new_node;
return start;
}
struct node *insert_after(struct node *start)
{
struct node *new_node, *ptr;
int num, val;
cout<<"\n Enter the data : ";
cin>>num;
cout<<"\n Enter the value after which the data has to be inserted:";
cin>>val;
new_node = (struct node *)malloc(sizeof(struct node));
new_node -> data = num;
ptr = start;
while(ptr -> data != val)
ptr = ptr -> next;
new_node -> prev = ptr;
new_node -> next = ptr -> next;
ptr -> next -> prev = new_node;
ptr -> next = new_node;
return start;
}
struct node *delete_beg(struct node *start)
{
struct node *ptr;
ptr = start;
start = start -> next;
start -> prev = NULL;
free(ptr);
return start;
}
struct node *delete_end(struct node *start)
{
struct node *ptr;
ptr = start;
while(ptr -> next != NULL)
 ptr = ptr -> next;
ptr -> prev -> next = NULL;
free(ptr);
return start;
}
struct node *delete_after(struct node *start)
{
struct node *ptr, *temp;
int val;
cout<<"\n Enter the value after which the node has to deleted : ";
cin>>val;
ptr = start;
while(ptr -> data != val)
 ptr = ptr -> next;
temp = ptr -> next;
ptr -> next = temp -> next;
temp -> next -> prev = ptr;
free(temp);
return start;
}
struct node *delete_before(struct node *start)
{
struct node *ptr, *temp;
int val;
cout<<"\n Enter the value before which the node has to deleted:";
cin>>val;
ptr = start;
while(ptr -> data != val)
 ptr = ptr -> next;
temp = ptr -> prev;
if(temp == start)
 start = delete_beg(start);
else
{
 ptr -> prev = temp -> prev;
 temp -> prev -> next = ptr;
}
free(temp);
return start;
}
struct node *delete_list(struct node *start)
{
while(start != NULL)
 start = delete_beg(start);
return start;
}
   //end of double linked list
   //circular linked list
   struct NOde
{
 int data;
struct NOde *next;
};
struct NOde *STart = NULL;
struct NOde *CReate_cll(struct NOde *);
struct NOde *DIsplay(struct NOde *);
struct NOde *INsert_beg(struct NOde *);
struct NOde *INsert_end(struct NOde *);
struct NOde *DElete_beg(struct NOde *);
struct NOde *DElete_end(struct NOde *);
struct NOde *DElete_after(struct NOde *);
struct NOde *DElete_list(struct NOde *);
   struct NOde *CReate_cll(struct NOde *STart)
{
struct NOde *new_NOde, *ptr;
int num;
cout<<"\n Enter –1 to end";
cout<<"\n Enter the data : ";
cin>>num;
while(num!=-1)
{
new_NOde = (struct NOde*)malloc(sizeof(struct NOde));
new_NOde -> data = num;
if(STart == NULL)
{
new_NOde -> next = new_NOde;
STart = new_NOde;
 }
 else
 { ptr = STart;
 while(ptr -> next != STart)
 ptr = ptr -> next;
 ptr -> next = new_NOde;
 new_NOde -> next = STart;
 }
 cout<<"\n Enter the data : ";
 cin>>num;
}
return STart;
}
struct NOde *DIsplay(struct NOde *STart)
{
struct NOde *ptr;
ptr=STart;
while(ptr -> next != STart)
{
 cout<<"\t %d"<< ptr -> data;
 ptr = ptr -> next;
}
cout<<"\t %d"<< ptr -> data;
return STart;
}
struct NOde *INsert_beg(struct NOde *STart)
{
struct NOde *new_NOde, *ptr;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_NOde = (struct NOde *)malloc(sizeof(struct NOde));
new_NOde -> data = num;
ptr = STart;
while(ptr -> next != STart)
 ptr = ptr -> next;
ptr -> next = new_NOde;
new_NOde -> next = STart;
STart = new_NOde;
return STart;
}
struct NOde *INsert_end(struct NOde *STart)
{
struct NOde *ptr, *new_NOde;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_NOde = (struct NOde *)malloc(sizeof(struct NOde));
new_NOde -> data = num;
ptr = STart;
while(ptr -> next != STart)
 ptr = ptr -> next;
ptr -> next = new_NOde;
new_NOde -> next = STart;
return STart;
}
struct NOde *DElete_beg(struct NOde *STart)
{
struct NOde *ptr;
ptr = STart;
while(ptr -> next != STart)
ptr = ptr -> next;
ptr -> next = STart -> next;
free(STart);
STart = ptr -> next;
return STart;
}
struct NOde *DElete_end(struct NOde *STart)
{
struct NOde *ptr, *preptr;
ptr = STart;
while(ptr -> next != STart)
{
preptr = ptr;
ptr = ptr -> next;
}
preptr -> next = ptr -> next;
free(ptr);
return STart;
}
struct NOde *DElete_after(struct NOde *STart)
{
struct NOde *ptr, *preptr;
int val;
cout<<"\n Enter the value after which the NOde has to deleted : ";
cin>>val;
ptr = STart;
preptr = ptr;
while(preptr -> data != val)
{
preptr = ptr;
ptr = ptr -> next;
}
preptr -> next = ptr -> next;
if(ptr == STart)
STart = preptr -> next;
free(ptr);
return STart;
}
struct NOde *DElete_list(struct NOde *STart)
{
struct NOde *ptr;
ptr = STart;
while(ptr -> next != STart)
STart = DElete_end(STart);
free(STart);
return STart;
}
   //end of circular linked list
//circular doubly linked list
struct NODe
{
struct NODe *NEXt;
int data;
struct NODe *PREv;
};
struct NODe *STArt = NULL;
struct NODe *CREate_ll(struct NODe *);
struct NODe *DISplay(struct NODe *);
struct NODe *INSert_beg(struct NODe *);
struct NODe *INSert_end(struct NODe *);
struct NODe *DELete_beg(struct NODe *);
struct NODe *DELete_end(struct NODe *);
struct NODe *delete_NODe(struct NODe *);
struct NODe *DELete_list(struct NODe *);

struct NODe *CREate_ll(struct NODe *STArt)
{
struct NODe *new_NODe, *ptr;
int num;
cout<<"\n Enter –1 to end";
cout<<"\n Enter the data : ";
cin>>num;
while(num != -1)
{
if(STArt == NULL)
{
new_NODe = (struct NODe*)malloc(sizeof(struct NODe));
new_NODe -> PREv = NULL;
new_NODe -> data = num;
new_NODe -> NEXt = STArt;
STArt = new_NODe;
}
else
{
new_NODe = (struct NODe*)malloc(sizeof(struct NODe));
new_NODe -> data = num;
ptr = STArt;
while(ptr -> NEXt != STArt)
ptr = ptr -> NEXt;
new_NODe -> PREv = ptr;
ptr -> NEXt = new_NODe;
new_NODe -> NEXt = STArt;
STArt -> PREv = new_NODe;
}
cout<<"\n Enter the data : ";
cin>>num;
}
return STArt;
}
struct NODe *DISplay(struct NODe *STArt)
{
struct NODe *ptr;
ptr = STArt;
while(ptr -> NEXt != STArt)
{
cout<<"\t %d" <<ptr -> data;
ptr = ptr -> NEXt;
}
cout<<"\t %d"<< ptr -> data;
return STArt;
}
struct NODe *INSert_beg(struct NODe *STArt)
{
struct NODe *new_NODe, *ptr;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_NODe = (struct NODe *)malloc(sizeof(struct NODe));
new_NODe-> data = num;
ptr = STArt;
while(ptr -> NEXt != STArt)
ptr = ptr -> NEXt;
new_NODe -> PREv = ptr;
ptr -> NEXt = new_NODe;
new_NODe -> NEXt = STArt;
STArt -> PREv = new_NODe;
STArt = new_NODe;
return STArt;
}
struct NODe *INSert_end(struct NODe *STArt)
{
struct NODe *ptr, *new_NODe;
int num;
cout<<"\n Enter the data : ";
cin>>num;
new_NODe = (struct NODe *)malloc(sizeof(struct NODe));
new_NODe -> data = num;
ptr = STArt;
while(ptr -> NEXt != STArt)
ptr = ptr -> NEXt;
ptr -> NEXt = new_NODe;
new_NODe -> PREv = ptr;
new_NODe -> NEXt = STArt;
STArt-> PREv = new_NODe;
return STArt;
}
struct NODe *DELete_beg(struct NODe *STArt)
{
struct NODe *ptr;
ptr = STArt;
while(ptr -> NEXt != STArt)
ptr = ptr -> NEXt;
ptr -> NEXt = STArt -> NEXt;
struct NODe* temp = STArt;
STArt=STArt->NEXt;
STArt->PREv=ptr;
free(temp);
return STArt;
}
struct NODe *DELete_end(struct NODe *STArt)
{
struct NODe *ptr;
ptr=STArt;
while(ptr -> NEXt != STArt)
 ptr = ptr -> NEXt;
ptr -> PREv -> NEXt = STArt;
STArt -> PREv = ptr -> PREv;
free(ptr);
return STArt;
}
struct NODe *delete_NODe(struct NODe *STArt)
{
struct NODe *ptr;
int val;
cout<<"\n Enter the value of the NODe which has to be deleted : ";
cin>>val;
ptr = STArt;
if(ptr -> data == val)
{
 STArt = DELete_beg(STArt);
 return STArt;
}
else
{
 while(ptr -> data != val)
 ptr = ptr -> NEXt;
 ptr -> PREv -> NEXt = ptr -> NEXt;
 ptr -> NEXt -> PREv = ptr -> PREv;
 free(ptr);
 return STArt;
}
}
struct NODe *DELete_list(struct NODe *STArt)
{
struct NODe *ptr;
ptr = STArt;
while(ptr -> NEXt != STArt)
 STArt = DELete_end(STArt);
free(STArt);
return STArt;
}
//end of circular doubly linked list
//**********************************************************************************************************************
//**********************************************************************************************************************
//QUEUES
//--------------------------------------------------------------------------------------------------------------------------------------------
//-------------------------------------------------------------------------------------------------------------------------------------------------
	#define MAX 10 // Changing this value will change length of array
int queue[MAX];
int front = -1, rear = -1;
void insert(void);
int delete_element(void);
int peek(void);
void display(void);
	void insert()
{
int num;
cout<<"\n Enter the number to be inserted in the queue : ";
cin>>num;
if(rear == MAX-1)
cout<<"\n OVERFLOW";
else if(front == -1 && rear == -1)
front = rear = 0;
else
rear++;
queue[rear] = num;
}
int delete_element()
{
int val;
if(front == -1 || front>rear)
{
cout<<"\n UNDERFLOW";
return -1;
}
else
{
val = queue[front];
front++;
if(front > rear)
front = rear = -1;
return val;
}
}
int peek()
{
if(front==-1 || front>rear)
{
cout<<"\n QUEUE IS EMPTY";
return -1;
}
else
{
return queue[front];
}
}
void display()
{
int i;
cout<<"\n";
if(front == -1 || front > rear)
cout<<"\n QUEUE IS EMPTY";
else
{
for(i = front;i <= rear;i++)
cout<<"\t"<< queue[i];
}
}
//--------------------------------------------------------------------------------------------------------------------------------------------
//-------------------------------------------------------------------------------------------------------------------------------------------------

//stack using array  functions
int n,st[5], Top=-1;
void PUSH(int st[], int val)
{
if(Top == n-1)
{
cout<<"\n STACK OVERFLOW";
}
else
{
Top++;
st[Top] = val;
}
}
int POP(int st[])
{
int val;
if(Top == -1)
{
cout<<"\n STACK UNDERFLOW";
return -1;
}
else
{
val = st[Top];
Top--;
return val;
}
}
void DISPLAY(int st[])
{
int i;
if(Top == -1)
cout<<"\n STACK IS EMPTY";
else
{
for(i=Top;i>=0;i--)
cout<<"\n"<<st[i];
cout<<"\n"; // Added for formatting purposes
}
}
int PEEK(int st[])
{
if(Top == -1)
{
cout<<"\n STACK IS EMPTY";
return -1;
}
else
return (st[Top]);
}
//stack using array functions end
//stack using linked list
struct stack
{
int data;
struct stack *next;
};
struct stack *top = NULL;
struct stack *push(struct stack *top, int val)
{
struct stack *ptr;
ptr = (struct stack*)malloc(sizeof(struct stack));
ptr -> data = val;
if(top == NULL)
{
ptr -> next = NULL;
top = ptr;
}
else
{
ptr -> next = top;
top = ptr;
}
return top;
}
struct stack *display(struct stack *top)
{
struct stack *ptr;
ptr = top;
if(top == NULL)
cout<<"\n STACK IS EMPTY";
else
{
while(ptr != NULL)
{
cout<<"\n"<< ptr -> data;
ptr = ptr -> next;
}
}
return top;
}
struct stack *pop(struct stack *top)
{
struct stack *ptr;
ptr = top;
if(top == NULL)
cout<<"\n STACK UNDERFLOW";
else
{
top = top -> next;
cout<<"\n The value being deleted is:"<< ptr -> data;
free(ptr);
}
return top;
}
int peek(struct stack *top)
{
if(top==NULL)
return -1;
else
return top ->data;
}
//stack using linked list end
void main()
{
   int y;
  while(1){
  cout<<"Enter the choice:\n1.stack\n2.queue\n3.linkedlist\n4.EXIT"<<endl;
  cin>>y;
  switch(y)
  {
    //stack
    case 1:
    {
      int u;
      cout<<"Enter the choice:\n1.stack uisng array\n2.stack using linked list\n3.MAIN\n4.EXIT"<<endl;
      cin>>u;
      switch(u)
      {          //stack
	 case 1://stack using array
	 {
	   int val, option;
do
{
cout<<"\n *****MAIN MENU*****";
cout<<"\n 1. PUSH";
cout<<"\n 2. POP";
cout<<"\n 3. PEEK";
cout<<"\n 4. DISPLAY";
cout<<"\n 5. EXIT";
cout<<"\n Enter your option: ";
cin>>option;
switch(option)
{
case 1:
cout<<"\n Enter the number to be pushed on stack: ";
cin>>val;
PUSH(st, val);
break;
case 2:
val = POP(st);
if(val != -1)
cout<<"\n The value deleted from stack is:"<< val;
break;
case 3:
val = PEEK(st);
if(val != -1)
cout<<"\n The value stored at top of stack is:"<<val;
break;
case 4:
DISPLAY(st);
break;
case 5:
exit(0);
case 6:
main();
}
}while(option != 7);

       }//end of stack using array
	 case 2:
	 {   //stack using linked list
	 int val, option;
do
{
cout<<"\n *****MAIN MENU*****";
cout<<"\n 1. PUSH";
cout<<"\n 2. POP";
cout<<"\n 3. PEEK";
cout<<"\n 4. DISPLAY";
cout<<"\n 5. EXIT";
cout<<"\n 6. MAIN";
cout<<"\n Enter your option: ";
cin>>option;
switch(option)
{
case 1:
cout<<"\n Enter the number to be pushed on stack: ";
cin>>val;
top = push(top, val);
break;
case 2:
top = pop(top);
break;
case 3:
val = peek(top);
if (val != -1)
cout<<"\n The value at the top of stack is:"<< val;
else
cout<<"\n STACK IS EMPTY";
break;
case 4:
top = display(top);
break;
case 5:
exit(0);
case 6:
main();
}
}while(option != 6);

	 }//end of stack uisng linked list
	 case 3:
	 main();
	 case 4:
	 exit(0);
	 }//stack end
	 case 2:
	 {//linked list types
	 int t;
	 cout<<"Enter the choice:\n1.Single linked list\n2.Doubly linked list\n3.Circular linked list\n4.Circular doubly linked list\n5.exit\n6.Main"<<endl;
	 cin>>t;
	 switch(t)
	 {//switch of types of linked list
	   case 1:
	  {//single linked  list
	  int option;
clrscr();
do
{
 cout<<"\n\n *****MAIN MENU *****";
 cout<<"\n 1: Create a list";
 cout<<"\n 2: Display the list";
 cout<<"\n 3: Add a NODE at the beginning";
 cout<<"\n 4: Add a NODE at the end";
 cout<<"\n 5: Add a NODE before a given NODE";
 cout<<"\n 6: Add a NODE after a given NODE";
 cout<<"\n 7: Delete a NODE from the beginning";
cout<<"\n 8: Delete a NODE from the end";
cout<<"\n 9: Delete a given NODE";
cout<<"\n 10: Delete a NODE after a given NODE";
cout<<"\n 11: Delete the entire list";
cout<<"\n 12: Sort the list";
cout<<"\n 13: EXIT";
cout<<"\n 14:MAIN";
cout<<"\n\n Enter your option : ";
cin>>option;
switch(option)
{
case 1: Start = Create_ll(Start);
cout<<"\n LINKED LIST CREATED";
break;
case 2: Start = Display(Start);
break;
case 3: Start = Insert_beg(Start);
break;
case 4: Start = Insert_end(Start);
break;
case 5: Start = Insert_before(Start);
break;
case 6: Start = Insert_after(Start);
break;
case 7: Start = Delete_beg(Start);
break;
case 8: Start = Delete_end(Start);
break;
case 9: Start = Delete_NODE(Start);
break;
case 10: Start = Delete_after(Start);
break;
case 11: Start = Delete_list(Start);
cout<<"\n LINKED LIST DELETED";
break;
case 12: Start = sort_list(Start);
break;
case 13:
exit(0);
case 14:
main();
}
}while(option !=14);

	  }//end of singly linked list
	   case 2:
	   {//doubly
	   int option;
clrscr();
do
{
cout<<"\n\n *****MAIN MENU *****";
cout<<"\n 1: Create a list";
cout<<"\n 2: Display the list";
cout<<"\n 3: Add a node at the beginning";
cout<<"\n 4: Add a node at the end";
cout<<"\n 5: Add a node before a given node";
cout<<"\n 6: Add a node after a given node";
cout<<"\n 7: Delete a node from the beginning";
cout<<"\n 8: Delete a node from the end";
cout<<"\n 9: Delete a node before a given node";
cout<<"\n 10: Delete a node after a given node";
cout<<"\n 11: Delete the entire list";
cout<<"\n 12: EXIT";
cout<<"\n\n Enter your option : ";
cin>>option;
switch(option)
{
case 1: start = create_ll(start);
cout<<"\n DOUBLY LINKED LIST CREATED";
break;
case 2: start = display(start);
break;
case 3: start = insert_beg(start);
break;
case 4: start = insert_end(start);
break;
case 5: start = insert_before(start);
break;
case 6: start = insert_after(start);
break;
case 7: start = delete_beg(start);
break;
case 8: start = delete_end(start);
break;
case 9: start = delete_before(start);
break;
case 10: start = delete_after(start);
break;
case 11: start = delete_list(start);
cout<<"\n DOUBLY LINKED LIST DELETED";
break;
}
}while(option != 12);

	   }

	   case 3:
	   {//circular linked list
	   int option;
 clrscr();
 do
 {
cout<<"\n\n *****MAIN MENU *****";
cout<<"\n 1: Create a list";
cout<<"\n 2: Display the list";
cout<<"\n 3: Add a NOde at the beginning";
cout<<"\n 4: Add a NOde at the end";
cout<<"\n 5: Delete a NOde from the beginning";
cout<<"\n 6: Delete a NOde from the end";
cout<<"\n 7: Delete a NOde after a given NOde";
cout<<"\n 8: Delete the entire list";
cout<<"\n 9: EXIT";
cout<<"\n10: MAIN";
cout<<"\n\n Enter your option : ";
cin>>option;
switch(option)
{
case 1: STart = CReate_cll(STart);
cout<<"\n CIRCULAR LINKED LIST CREATED";
break;
case 2: STart = DIsplay(STart);
break;
case 3: STart = INsert_beg(STart);
break;
case 4: STart = INsert_end(STart);
break;
case 5: STart = DElete_beg(STart);
break;
case 6: STart = DElete_end(STart);
break;
case 7: STart = DElete_after(STart);
break;
case 8: STart = DElete_list(STart);
cout<<"\n CIRCULAR LINKED LIST DELETED";
break;
case 9:
exit(0);
case 10:
main();
}
 }while(option !=10);
	   }//end of circular linked list
	 case 4:
	 {//circular double linke list
	 int option;
do
{
 cout<<"\n\n *****MAIN MENU *****";
 cout<<"\n 1: Create a list";
 cout<<"\n 2: Display the list";
 cout<<"\n 3: Add a NODe at the beginning";
 cout<<"\n 4: Add a NODe at the end";
 cout<<"\n 5: Delete a NODe from the beginning";
 cout<<"\n 6: Delete a NODe from the end";
 cout<<"\n 7: Delete a given NODe";
 cout<<"\n 8: Delete the entire list";
 cout<<"\n 9: EXIT";
 cout<<"\n 10: MAIN";
 cout<<"\n\n Enter your option : ";
cin>>option;
switch(option)
{
case 1: STArt = CREate_ll(STArt);
cout<<"\n CIRCULAR DOUBLY LINKED LIST CREATED";
break;
case 2: STArt = DISplay(STArt);
break;
case 3: STArt = INSert_beg(STArt);
break;
case 4: STArt = INSert_end(STArt);
break;
case 5: STArt = DELete_beg(STArt);
break;
case 6: STArt = DELete_end(STArt);
break;
case 7: STArt = delete_NODe(STArt);
break;
case 8: STArt = DELete_list(STArt);
cout<<"\n CIRCULAR DOUBLY LINKED LIST DELETED";
break;
case 9:
exit(0);
case 10:
main();
}
}while(option != 10);

	 }//end of circular double linked list
	 case 5:
	 exit(0);
	 case 6:
	 main();
	 }//end of switch of types of linked list
		 }//end of linked list types
     case 3:
	{//queue start
	int option, val;
do
{
cout<<"\n\n ***** MAIN MENU *****";
cout<<"\n 1. Insert an element";
cout<<"\n 2. Delete an element";
cout<<"\n 3. Peek";
cout<<"\n 4. Display the queue";
cout<<"\n 5. EXIT";
cout<<"\n 6. Main";
cout<<"\n Enter your option :";
cin>>option;
switch(option)
{
case 1:
insert();
break;
case 2:
val = delete_element();
if (val != -1)
cout<<"\n The number deleted is : "<< val;
break;
case 3:
val = peek();
if (val != -1)
cout<<"\n The first value in queue is :"<< val;
break;
case 4:
display();
break;
}
}while(option != 6);

	}//end of queue
      }//types switch case

    }//stack end
  }//while end
  getch();
  }