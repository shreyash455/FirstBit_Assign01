1 Print numbers from 1 to 10
Output: 1 2 3 4 5 6 7 8 9 10 by using loop in c

#include <stdio.h>
int main() {
    for (int i = 1; i <= 10; i++) {
        printf("%d ", i);
    }
    return 0;
}

2 Print table for given number.
Input: n = 5
Output: 5 10 15 20 25 30 35 40 45 50

#include <stdio.h>
int main() {
    int n,i;
    printf("Enter a number: ");
    scanf("%d", &n);

    for ( i = 1; i <= 10; ++i) 
	{
        printf("%d ", n * i);
    }
    return 0;
}

3 Sum of numbers in given range.
Find sum of numbers from start to end.
Input: start = 1, end = 5
Output: 15

#include <stdio.h>
int main() {
    int start = 1, end = 5, sum = 0,i;

    for ( i = start; i <= end; ++i)
        sum += i;

    printf("%d", sum);   // Output: 15
    return 0;
}
