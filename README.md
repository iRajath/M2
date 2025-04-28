# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:

```c
#include <stdio.h>

int main(void)
{
    int M, N;

    printf("Enter the starting number (M): ");
    scanf("%d", &M);

    printf("Enter the ending number (N): ");
    scanf("%d", &N);

    if (M > N)
    {
        printf("Error: Starting number must be less than or equal to ending number.\n");
        return 1;
    }

    printf("Even numbers between %d and %d are:\n", M, N);

    int start = (M % 2 == 0) ? M : M + 1;

    for (int i = start; i <= N; i += 2)
    {
        printf("%d ", i);
    }

    printf("\n");
    return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/985d834b-9ed1-4077-b1f3-3408a6f1e9ab)









## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:

```c
#include <stdio.h>

int main(void)
{
    int rows;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (int i = rows; i >= 1; i--)
    {
        for (int j = 1; j <= i; j++)
        {
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/18f33476-6d17-4449-96c4-8bdb0525cbec)




## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:

```c
#include <stdio.h>

void add(int a, int b);
void subtract(int a, int b);

int main(void)
{
    int num1, num2;

    printf("Enter first number: ");
    scanf("%d", &num1);

    printf("Enter second number: ");
    scanf("%d", &num2);

    add(num1, num2);
    subtract(num1, num2);

    return 0;
}

void add(int a, int b)
{
    printf("Addition result: %d\n", a + b);
}

void subtract(int a, int b)
{
    printf("Subtraction result: %d\n", a - b);
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/d2a97529-da60-421a-9c43-0636800b8946)





## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:

```c
#include <stdio.h>

int main(void)
{
    int number, digit, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &number);

    for (; number != 0; number /= 10)
    {
        digit = number % 10;
        if (digit % 2 != 0)
        {
            sum += digit;
        }
    }

    printf("Sum of odd digits: %d\n", sum);

    return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/d45b965d-5c9f-4028-bdad-88234a9f8a47)



## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:

```c
#include <stdio.h>

void fact();

int main(void)
{
    fact();
    return 0;
}

void fact()
{
    int i, N;
    long int fact = 1;

    printf("Enter a positive integer: ");
    scanf("%d", &N);

    for (i = 1; i <= N; i++)
    {
        fact *= i;
    }

    printf("Factorial of %d = %ld\n", N, fact);
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/2ae37068-4770-4432-8c1b-70949f87de95)

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
