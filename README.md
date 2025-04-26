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
int main() 
{
    int M, N, i;
    printf("Enter the values of M and N: ");
    scanf("%d%d", &M, &N);
    printf("Even numbers from %d to %d are:\n", M, N);
    for (i = M; i <= N; i++) 
    {
        if (i % 2 == 0)
        {
            printf("%d ", i);
        }
    }
    return 0;
}

```
## OUTPUT:


![image](https://github.com/user-attachments/assets/a7bb16b8-f3c9-4a97-9902-1cd7e4100809)








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
int main() 
{
    int i, j, rows;
    printf("Enter the number of rows: ");
    scanf("%d", &rows);
    for (i = 1; i <= rows; i++) 
    {
        for (j = 1; j <= i; j++)
        {
            printf("* ");
        }
        printf("\n"); 
    }
    return 0;
}

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/964a0bd4-fab4-45e0-9b3f-6df5fea5d7d2)




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
void add(int num1, int num2)
{
    int sum = num1 + num2;
    printf("Sum: %d\n", sum);
}
void subtract(int num1, int num2)
{
    int difference = num1 - num2;
    printf("Difference: %d\n", difference);
}
int main()
{
    int a, b;
    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);
    add(a, b);
    subtract(a, b);
    return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/7bbf1064-6700-49f9-bf60-3c5d3749b48a)





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
int main() 
{
    int number, digit, sumOfOdds = 0;
    printf("Enter an integer: ");
    scanf("%d", &number);
    if (number < 0)
    {
        number = -number;
    }
    for (; number > 0; number /= 10) 
    {
        digit = number % 10;
        if (digit % 2 != 0) 
        {
            sumOfOdds += digit;
        }
    }
    printf("Sum of odd digits: %d\n", sumOfOdds);
    return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/b541f9df-f408-4440-8f61-ebbe9c077471)



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
long long fact();
int main() 
{
    long long factorial = fact();
    printf("Factorial = %lld\n", factorial);
    return 0;
}
long long fact() 
{
    int i, n;
    long long factorial = 1;
    printf("Enter a non-negative integer: ");
    scanf("%d", &n);
    if (n < 0) 
    {
        printf("Error! Factorial of a negative number doesn't exist.\n");
        return 1; 
    } 
    else
    {
        for (i = 1; i <= n; i++) 
        {
            factorial *= i;
        }
        return factorial;
    }
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/4d94853a-49d0-4baf-ac47-59ee9bf5242c)


## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
