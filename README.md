#include<stdio.h>
int stack[100],x,n,i,top;
void push()
{
        if(top>=n-1)
        {
               printf("enter over flow occure\n");
        }
        else
        {
                printf("enter a value to be pushed\n");
                scanf("%d",&x);
                top++;
                stack[top]=x;
        }
}
void pop()
{
        if(top<=-1)
        {
                printf("enter under flow occure\n");
        }
        else
        {
                printf("the poped element is %d\n", stack[top]);
                top--;
        }
}
void display()
{
        if(top>=0)
        {
                printf("the elements in the stack is\n");
                for (i=top;i>=0;i--)
                       printf("%d",stack[i]);
                        printf("press next choice\n");
                }
                else
                {
                        printf("stack is empty");
                }
}
void main()
{
        int choice=0;
        int top=-1;
        while(choice<4)
      printf("enter the size of stack");
      scanf("%d",&n);
      printf("the stack operations is");
      printf("\n\t-----------------");
      printf("enter 1-push\n,2-pop\n");
      printf("enter 3-display\n");
      printf("enter the choice");
      scanf("%d",&choice);
      switch(choice)
      {
              case 1:
                      push();
                      break;
              case 2:
                      pop();
                      break;
              case 3:
                      display();
                      break;
              default:
                      printf("enter wrong choice");
      }
}
