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

3. Write a program to check whether a given year is a leap year.

#include <stdio.h>
void main() {
int year=2004;
if(year%4==0 && year%100!=0 || year%400==0)
{
   printf("is a leap year");
}
else
{
   printf("not a leap year");   
}
}

4. Write a program to check whether a given character is a vowel or consonant.

#include <stdio.h>

void main() {
char ch='5';

if(ch>='a' && ch<='z')
{
    if(ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u')
    printf("vowel");
    else
    printf("consonant");
}
else
printf("this is not a alphabate");
}

5. Write a program to check whether a person is eligible to vote (age ≥ 18).

#include <stdio.h>

void main() {
int age =24;
if(age>=18)
printf("eligible for vote:::");
else
printf("not eligible for vote:::");
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

7. Calculating total salary based on basic. If basic <=5000 da, ta and hra will be
10%,20% and 25% respectively otherwise da, ta and hra will be 15%,25% and 30%
respectively.

#include <stdio.h>

void main() {
double salary = 6000;
double da,ta,hra,ts;
ts=salary+da+ta+hra;
if(salary<=5000)
{
    da=salary*0.1;
    ta=salary*0.2;
    hra=salary*0.25;
    printf("print if part");
}
else
{
    da=salary*0.15;
    ta=salary*0.25;
    hra=salary*0.30;
    printf("total salary");
}
}


:::::::::::::::::::::::ClASS WORK::::::::::::::::::::::::
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
