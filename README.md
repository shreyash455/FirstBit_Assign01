# FirstBit_Assign01
Assignment No.1
1. Write a program to check whether a number is even or odd.

#include <stdio.h>
void  main() 
{
    int n=5;
    if(n%2==0)
    {
        printf("Number is even");
    }
    else
    {
        printf("Number is odd");
    }
}

2. Write a program to check given 3 digit number is pallindrome or not.

#include <stdio.h>
void  main() 
{
    int n=828,r1,r2,r3,rev;
    int q;
    r1=n%10;
    q=n/10;
    r2=q%10;
    q=q/10;
    r3=q%10;
    
    rev=r1*100+r2*10+r3;
    if(rev==n)
    {
        printf("palindrome");
    }
    else
    {
        printf("No palindrome");
    }
}

6. Write a program to check whether a given character is uppercase or lowercase.

#include <stdio.h>
int main()
{
	char n = 'a';
	if(n>='A' && n<='Z')
	{
		printf("UpperCase");
	}
	else
	{
		printf("LowerCase");
	}
	
	return 0;
}






ClASS WORK::::::::::::::::::::::::
..................................nested if else..................................
#include <stdio.h>

void main()
{
    char ch='5';
    if(ch>='a'&&ch<='z' || ch>='A'&&ch<='Z')
    {
        printf("it is alphabate");
    }
    else
    {
        if(ch>='0'&&ch<='9')
        {
            printf("it is no.");
        }
        else
        {
            printf("it is symbol");
        }
    }
    
}
