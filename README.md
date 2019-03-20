#include<stdio.h>
#include<stdlib.h>

#define MAX 5000
void sort();
void insert();
void display();
void totaldistance();
int a[MAX];
int rear = -1;
int front = -1;
void main()
{
	int choice;
	while(1)
	{
	printf("\nEnter your choice:\n");
	printf("\n1. Inserting items in queue");
	printf("\n2. Displaying inserted items");
	printf("\n3. Total distance travelled");
	printf("\n4. Exit\n");
	printf("\n Your choice is: ");
	scanf("%d",&choice);
	switch(choice)
	{
		case 1:
			insert();
			break;
		
		case 2:
			display();
			break;
		
		case 3:
			totaldistance();
			break;
			
		case 4:
			exit(1);
		default:
			printf("/nPlease choose among 1,2,3");
	}
    }
}

void insert()
{
    int add_items;
    if (rear == MAX-1)
    printf("Queue can't take more elements \n");
    else
    {
        if (front == - 1)
        front = 0;
        printf("Insert the element in queue : ");
        scanf("%d", &add_items);
        rear = rear + 1;
        a[rear] = add_items;
    }
}

void display()
{
    int i,item;
    if (front == - 1)
        printf("Queue is empty,please insert some elements: \n");
    else
    {
        printf("Inserted elements in the queue are : \n");
        for (i=front;i<=rear;i++)
        printf("%d ",a[i]);
        printf("\n");
    }
}
