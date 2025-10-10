1. Print armstrong numbers in the given range 1 to n.

#include <stdio.h>
#include <math.h>
int main() {
    int i,n, num, original, sum, digits;

    printf("Enter the upper limit (n): ");
    scanf("%d", &n);

    printf("Armstrong numbers from 1 to %d are:\n", n);

    for ( i = 1; i <= n; i++) {
        original = i;
        num = i;
        digits = 0;
        sum = 0;

        // Count number of digits
        while (num != 0) {
            num /= 10;
            digits++;
        }

        num = original;

        // Calculate sum of digits^digits
        while (num != 0) {
            int rem = num % 10;
            sum += pow(rem, digits);
            num /= 10;
        }

        if (sum == original) {
            printf("%d\n", original);
        }
    }

    return 0;
}


2. Print prime numbers in the given range 1 to n.

#include <stdio.h>
#include <stdbool.h>
int main() {
    int n,num,i;
    printf("Enter the upper limit (n): ");
    scanf("%d", &n);

    printf("Prime numbers from 1 to %d are:\n", n);

    for (num = 2; num <= n; num++) {
        bool isPrime = true;

        // Check divisibility up to sqrt(num)
        for (i = 2; i * i <= num; i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime) {
            printf("%d ", num);
        }
    }

    printf("\n");
    return 0;
}


3. Print perfect numbers in the given range 1 to n.

#include <stdio.h>
int main() {
    int n,i,num;
    printf("Enter the upper limit (n): ");
    scanf("%d", &n);

    printf("Perfect numbers from 1 to %d are:\n", n);

    for (num = 2; num <= n; ++num) {
        int sum = 1;                 // 1 is always a proper divisor
        for (i = 2; i * i <= num; ++i) {
            if (num % i == 0) {
                sum += i;
                if (i * i != num)    // avoid adding the square root twice
                    sum += num / i;
            }
        }
        if (sum == num)
            printf("%d\n", num);
    }
    return 0;
}


4. Print strong numbers in the given range 1 to n.
#include <stdio.h>
int main(void) {               
    int n,num,i;
    printf("Enter the upper limit (n): ");
    if (scanf("%d", &n) != 1 || n < 2) {   // basic input check
        puts("Invalid input.");
        return 0;
    }

    for (num = 2; num <= n; ++num) {   // declare loop vars in-place
        int sum = 1;
        for (i = 2; i * i <= num; ++i) {
            if (num % i == 0) {
                sum += i;
                if (i * i != num)
                    sum += num / i;
            }
        }
        if (sum == num)
            printf("%d\n", num);
    }
    return 0;
}



5. Write a menu driven program to take a number for user and perform operations as follows.

Press 1.To check number is even or odd.
2.To check number is prime or not.
3.To check number is pallindrome or not.
4.To check number is positive, negative or zero.
5.To reverse a number.
6.To find sum of digits.

#include <stdio.h>
#include <stdbool.h>
int i;
/* ---------- utility functions ---------- */
bool isPrime(int n) {
    if (n < 2) return false;
    for ( i = 2; i * i <= n; ++i)
        if (n % i == 0) return false;
    return true;
}

bool isPalindrome(int n) {
    int orig = n, rev = 0;
    while (n) { rev = rev * 10 + n % 10; n /= 10; }
    return orig == rev;
}

int reverse(int n) {
    int rev = 0;
    while (n) { rev = rev * 10 + n % 10; n /= 10; }
    return rev;
}

int sumDigits(int n) {
    int s = 0; 
    n = n < 0 ? -n : n;          /* handle negatives */
    while (n) { s += n % 10; n /= 10; }
    return s;
}

/* ---------- driver ---------- */
int main(void) {
    int choice, num;

    while (1) {
        puts("\n========== MENU ==========");
        puts("1. Even or Odd");
        puts("2. Prime or Not");
        puts("3. Palindrome or Not");
        puts("4. Positive / Negative / Zero");
        puts("5. Reverse the Number");
        puts("6. Sum of Digits");
        puts("0. Exit");
        printf("Enter choice: ");
        if (scanf("%d", &choice) != 1) break;

        if (choice == 0) { puts("Good-bye!"); break; }
        if (choice < 1 || choice > 6) { puts("Invalid choice, try again."); continue; }

        printf("Enter an integer: ");
        scanf("%d", &num);

        switch (choice) {
            case 1:
                printf("%d is %s\n", num, (num % 2 == 0) ? "EVEN" : "ODD");
                break;
            case 2:
                printf("%d is %s\n", num, isPrime(num) ? "PRIME" : "NOT PRIME");
                break;
            case 3:
                printf("%d is %s\n", num, isPalindrome(num) ? "PALINDROME" : "NOT PALINDROME");
                break;
            case 4:
                if (num > 0)       printf("%d is POSITIVE\n", num);
                else if (num < 0)  printf("%d is NEGATIVE\n", num);
                else               printf("Number is ZERO\n");
                break;
            case 5:
                printf("Reversed: %d\n", reverse(num));
                break;
            case 6:
                printf("Sum of digits: %d\n", sumDigits(num));
                break;
        }
    }
    return 0;
}
