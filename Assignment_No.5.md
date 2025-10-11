1. Print a solid square pattern
Input: n = 4
Output:

* * * *
* * * *
* * * *
* * * *

#include<stdio.h>
void main()
{
	int i,j;
	for(i=1;i<=4;i++)
	{
	    for(j=1;j<=4;j++)
	    {
	    	printf("* ");
    	}
    	printf("\n");
	}
}


2. Print a right-angled triangle pattern
Input: n = 5
Output:
*
**
***
****
*****

#include <stdio.h>
void rightAngledTriangle(int n) {
	int i,j;
    for ( i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++)
            printf("*");
        printf("\n");
    }
}

int main() {
    int n = 5;
    rightAngledTriangle(n);
    return 0;
}


3. Print an inverted right-angled triangle pattern
Input: n = 5
Output:

*****
****
***
**
*

#include <stdio.h>

void invertedRightTriangle(int n) {
	int i, j;
    for (i = n; i >= 1; i--) {
        for (j = 1; j <= i; j++)
            printf("*");
        printf("\n");
    }
}

int main() {
    int n = 5;
    invertedRightTriangle(n);
    return 0;
}
