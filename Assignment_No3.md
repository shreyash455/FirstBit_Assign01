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

4 Check the given number is prime or not.
Input: n = 7
Output: Prime

#include <stdio.h>

int main() {
    int n = 7,i;
    int isPrime = 1;          

    if (n < 2)               
        isPrime = 0;
    else {
            for ( i = 2; i * i <= n; ++i) {
            if (n % i == 0) { 
                isPrime = 0;
                break;
            }
        }
    }

    printf("%s\n", isPrime ? "Prime" : "Not Prime");
    return 0;
}

5 Check the given number is Armstrong number or not..
Input: n = 153
Output: Armstrong
#include <stdio.h>

int main() {
    int n = 153;
    int a = n / 100;        // hundreds
    int b = (n / 10) % 10;  // tens
    int c = n % 10;         // units

    if (a*a*a + b*b*b + c*c*c == n)
        printf("Armstrong\n");
    else
        printf("Not Armstrong\n");

    return 0;
}

6.Check the given number is Perfect number or not.
Input: n = 28
Output: Perfect

""""""""""""""""A perfect number is a positive integer that is equal to the sum of all its proper positive divisors (that is, all positive divisors excluding the number itself).
Example:
Divisors of 28 (excluding 28) → 1, 2, 4, 7, 14
Sum → 1 + 2 + 4 + 7 + 14 = 28 → Perfect number."""""""""""""""""""""

#include <stdio.h>
int main() {
    int n = 28;
    int sum = 0;

    for (int i = 1; i < n; i++) {
        if (n % i == 0)      // i is a proper divisor
            sum += i;
    }

    if (sum == n)
        printf("Perfect\n");
    else
        printf("Not Perfect\n");

    return 0;
}

7 Find factorial of given number.
Input: n = 5
Output: 120

#include <stdio.h>
unsigned long long factorial(int n) {
    return (n <= 1) ? 1 : n * factorial(n - 1);
}

int main() {
    int n = 5;
    printf("%llu\n", factorial(n));  // 120
    return 0;
}

8 Check the given number is Strong number or not.
Input: n = 145
Output: Strong

✅ Example:
145
1! + 4! + 5! = 1 + 24 + 120 = 145 → Strong number ✅

#include <stdio.h>
int main() {
    int n = 145;
    int original = n;
    int sum = 0;

    while (n > 0) {
        int digit = n % 10;
        int fact = 1;

        // factorial of digit
        for (int i = 1; i <= digit; ++i)
            fact *= i;

        sum += fact;
        n /= 10;
    }

    if (sum == original)
        printf("Strong\n");
    else
        printf("Not Strong\n");

    return 0;
}


9 Check the given number is Palindrome number or not.
Input: n = 121
Output: Palindrome

#include <stdio.h>
int main() {
    int n = 121;
    int original = n;
    int reversed = 0;

    while (n > 0) {
        int digit = n % 10;
        reversed = reversed * 10 + digit;
        n /= 10;
    }

    if (reversed == original)
        printf("Palindrome\n");
    else
        printf("Not Palindrome\n");

    return 0;
}

10 Find Sum of first and last digit of given number.
Input: n = 12345
Output: 6 (1 + 5)
