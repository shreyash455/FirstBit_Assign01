1. Write a C program to add two integers and display the result

#include<stdio.h>
int main()
{
	int a,b;
	
	printf("Enter a number for a & b \n");
	scanf("%d%d",&a,&b);
	
	printf("Addition of %d & %d is %d",a,b,(a+b));
	
	return 0;
}

2. Write a C program to find the area of a circle.

#include<stdio.h>
int main()
{
	int r;
	float area;
	printf("Enter a radius \n");
	scanf("%d",&r);
	area=3.14 * r * r;
	 printf("Area of circle is: %.2f\n",area );
	
	return 0;
}

3. Write a C program to convert temperature from Celsius to Fahrenheit using the
formula:
F = (C *9/5) + 32

#include <stdio.h>
int main(void)
{
    int c;
    float f;

    printf("Enter a degree Celsius: ");
    scanf("%d", &c);

    f = c * 9.0f / 5.0f + 32.0f;

    printf("Converted degree into Fahrenheit is %.2f\n", f);

    return 0;
}

4. Write a C program to swap two numbers using a temporary third variable.

#include <stdio.h>
int main(void)
{
    int a, b, temp;

    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);

    printf("Before swap: a = %d, b = %d\n", a, b);

    temp = a;
    a    = b;
    b    = temp;

    printf("After  swap: a = %d, b = %d\n", a, b);
    return 0;
}

5. Write a C program to input five numbers and find their average.
6. 
