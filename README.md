# simple_calculator
is a calculator code that does what you want


#include <stdlib.h>
#include <stdio.h>
#include <math.h>


int collection(int number1,int number2)
{
	return	number1 + number2;
}


int extraction(int number1,int number2)
{
	return number1 - number2;
}


int impact(int number1,int number2)
{
	return number1*number2;
}


float divide(int number1,int number2)
{
	return (float)number1 / number2;
}


double square_root(double number1)
{
	return sqrt(number1);		
}
	

double exponents(double number1,double number2)
{
	return pow(number1,number2);
}


int main()
{
	
int number1,number2,calculator;
	
printf("-------contents-------\n");
printf("\n1-collection");
printf("\n2-extraction");
printf("\n3-impact");
printf("\n4-divide");
printf("\n5-square_root");
printf("\n6-exponents");
printf("\n-----------------------");
printf("\nwhat do you want to do?\n");
scanf("%d",&calculator);
	
switch(calculator)
	{
		case 1:
			printf("Please enter two numbers:");
			scanf("%d%d",&number1,&number2);
			collection(number1,number2);
			printf("result:%d",collection(number1,number2));
			break;
		case 2:
			printf("Please enter two numbers:");
			scanf("%d%d",&number1,&number2);
			extraction(number1,number2);
			printf("result:%d",extraction(number1,number2));
			break;
		case 3:
			printf("Please enter two numbers:");
			scanf("%d%d",&number1,&number2);
			impact(number1,number2);
			printf("result:%d",impact(number1,number2));
			break;
		case 4:
			printf("Please enter two numbers:");
			scanf("%d%d",&number1,&number2);
			divide(number1,number2);
			printf("result:%.2f",divide(number1,number2));
			break;
		case 5:
			printf("Please enter number:");
			scanf("%d",&number1);
			if(number1 < 0)
			{
			printf("Square roots of negative numbers cannot be calculated!!");
			}
			else
			{	
			double result = square_root((double)number1);
			printf("result:%.2f",result);
			}
			break;
		case 6:
			double base,expo;
			printf("enter the base value:");
			scanf("%lf",&base);
			printf("enter exponent value:");
			scanf("%lf",&expo);
			exponents(base,expo);
			printf("result:%.2f",exponents(base,expo));
			break;
		default :
			printf("You entered the wrong number!!!");
			break;
	}	
	return 0;
}
