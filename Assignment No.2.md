2. Accept three sides of a triangle from the user and determine whether the triangle is
equilateral, isosceles, or scalene.

#include <stdio.h>
int main(void)
{
    int a, b, c;

    printf("Enter three sides of a triangle: ");
    if (scanf("%d %d %d", &a, &b, &c) != 3 || a <= 0 || b <= 0 || c <= 0) {
        printf("Invalid input.\n");
        return 1;
    }


    if (a + b <= c || a + c <= b || b + c <= a) {
        printf("Not a valid triangle.\n");
        return 1;
    }

    if (a == b && b == c)
        printf("Equilateral triangle.\n");
    else if (a == b || b == c || a == c)
        printf("Isosceles triangle.\n");
    else
        printf("Scalene triangle.\n");

    return 0;
}

3. Write a program to find greatest of three numbers using nested if-else.

#include <stdio.h>

int main() {
    int a, b, c;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    if (a >= b && a >= c)       printf("%d is greatest\n", a);
    else if (b >= c)            printf("%d is greatest\n", b);
    else                        printf("%d is greatest\n", c);

    return 0;
}

4. Ask the user to enter marks.
Then show the result based on these rules:
If marks are more than 75 → show "Distinction"
If marks are more than 65 → show "First Class"
If marks are more than 55 → show "Second Class"
If marks are 40 or more → show "Pass Class"
If marks are less than 40 → show "Fail"

#include <stdio.h>

int main() {
    int m;
    printf("Enter marks: ");
    scanf("%d", &m);

    if (m > 75)      printf("Distinction");
    else if (m > 65) printf("First Class");
    else if (m > 55) printf("Second Class");
    else if (m >=40) printf("Pass Class");
    else             printf("Fail");

    return 0;
}

5. Accept the price from user. Ask the user if he is a student (user may say y or n). If he
is a student and he has purchased more than 500 than discount is 20% otherwise
discount is 10%.But if he is not a student then if he has purchased more than 600
discount is 15% otherwise there is not discount.

#include <stdio.h>

int main() {
    double price, discount = 0;
    char student;

    printf("Enter purchase price: ");
    scanf("%lf", &price);

    printf("Are you a student? (y/n): ");
    scanf(" %c", &student);

    if (student == 'y' || student == 'Y') {
        if (price > 500)
            discount = 0.20;
        else
            discount = 0.10;
    } else {
        if (price > 600)
            discount = 0.15;
        else
            discount = 0.0;
    }

    printf("Discount: %.0lf%%\n", discount * 100);
    printf("Final amount: %.2lf\n", price * (1 - discount));

    return 0;
}

6. Accept a number and check if it is divisible by 3, 5, or both.
(Print "Divisible by 3 but not by 5" or "Divisible by 5 but not by 3" or "Divisible by
both" or” Divisible by None”)

#include <stdio.h>

int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);

    if (n % 3 == 0 && n % 5 == 0)
        printf("Divisible by both\n");
    else if (n % 3 == 0)
        printf("Divisible by 3 but not by 5\n");
    else if (n % 5 == 0)
        printf("Divisible by 5 but not by 3\n");
    else
        printf("Divisible by None\n");

    return 0;
}

7. Accept the age and check if the person is:
Child (age < 12),Teenager (12–19),Adult (20–59),Senior (60 and above)

#include <stdio.h>
int main() {
    int age;
    printf("Enter a age: ");
    scanf("%d", &age);

    if (age<12)
        printf("Child\n");
    else if (age>=12 && age<=19)
        printf("Teenager\n");
    else if (age>=20 && age<=59)
        printf("Adult\n");
    else
        printf("senior\n");

    return 0;
}
