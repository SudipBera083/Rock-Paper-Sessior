# Rock-Paper-Sessior
#I am just making a  game that exactly on the purpose of practice the code.
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>

typedef int PLAYER;
PLAYER you, computer;
int menue()
{
	int ch;
	printf("1.Rock\n2.Paper\n3.Sessior\n4.Exit\n");
	printf("Enter your choice:");
	scanf("%d",&ch);
	return ch;
}

int setup()
{
	level1:
	computer=rand()%4;
	if (computer==0)
	{
		goto level1;
	}
	    
	
	you=menue();
}

int logic()
{
	switch(you)
	{
		case 1:
			if(computer==1)
			{
				printf("MAtch Draw\n");
				
			}
			else if (computer==2)
			{
				printf("You Lose!\n");
			}
			else if(computer==3)
			{
				printf("You win!\n");
			}
			
			break;
		case 2:
			if(computer==1)
			{
				printf("You win !\n");
				
			}
			else if (computer==2)
			{
				printf("MAtch Draw\n");
			}
			else if(computer==3)
			{
				printf("You Lose!\n");
			}
			break;
		case 3:
			if(computer==1)
			{
				printf("you Lose!\n");
				
			}
			else if (computer==2)
			{
				printf("You Win!\n");
			}
			else if(computer==3)
			{
				printf("Match Draw!\n");
			}
			break;
		case 4:
			exit(0);
		default:
			printf("\nInvalid user input\n");
			break;
	}
}
int main()
{
	while(1)
	{
		system("cls");
	setup();
	logic();
	getch();
	}
	return 0;
}
