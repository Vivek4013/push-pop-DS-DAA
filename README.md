# push-pop-DS-DAA 
#include<stdio.h>

#include<conio.h>

#include<stdlib.h>

void push(int,int);

void pop();

int top = -1;

int stack_arr[100];

void main()

{

 int max, item,choice,res;

 printf("Enter max size: ");

 scanf("%d",&max);

 while(1)

 {

     printf("\nEnter the choice:--- ");

     printf("\n1. push operation");

     printf("\n2.pop opertion");

     printf("\n3. Exit Operation\n");

     scanf("%d",&choice);

     switch(choice)

     {

         case 1 :

             printf("\nEnter the number want to insert in stack\n");

             scanf("%d",&item);

             push(max,item);

             break;

          case 2:

              pop();

              break;

        case 3: 

            exit(0);

            

           default:

                printf("Incorrect Choice");

    }

 }

 getch();

}

void push(int max,int item)

{

    if(top==max-1)

    {

        printf("\nstack overflow\n");

    }

    top=top+1;

    stack_arr[top]=item;

}

void pop()

{

    if(top==-1)

    {

        printf("\n stack underflow\n");

    }

    

    int item =stack_arr[top];

    printf("Item deleted: %d",item);

    top=top-1;

}
