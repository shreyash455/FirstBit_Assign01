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
