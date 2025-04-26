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
#include <stdio.h>

int main() {
    // Step 1: Declare variables
    int M, N;

    // Step 2 & 3: Input M and N
    printf("Enter the starting value M: ");
    scanf("%d", &M);
    printf("Enter the ending value N: ");
    scanf("%d", &N);

    // Step 4–7: Loop through M to N and print even numbers
    printf("Even numbers from %d to %d are:\n", M, N);
    for (int i = M; i <= N; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }
    }

    printf("\n"); // newline for clean output
    return 0;
}

## OUTPUT:
Enter the starting value M: 10
Enter the ending value N: 20
Even numbers from 10 to 20 are:
10 12 14 16 18 20

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
#include <stdio.h>

int main() {
    // Step 1: Declare variable
    int rows;

    // Step 2: Input number of rows
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    // Step 3–5: Loop to print the triangle pattern
    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n"); // Move to next line after each row
    }

    return 0;
}


## OUTPUT:
Enter the number of rows: 5
* 
* * 
* * * 
* * * * 
* * * * * 





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
#include <stdio.h>

// Step 1: Declare functions
void add(int a, int b);
void subtract(int a, int b);

int main() {
    // Step 3: Declare variables and read input
    int num1, num2;
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    // Step 4: Call functions
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}

// Step 2: Define addition function
void add(int a, int b) {
    int sum = a + b;
    printf("Addition of %d and %d is: %d\n", a, b, sum);
}

// Step 2: Define subtraction function
void subtract(int a, int b) {
    int diff = a - b;
    printf("Subtraction of %d and %d is: %d\n", a, b, diff);
}


## OUTPUT:
Enter two numbers: 15 8
Addition of 15 and 8 is: 23
Subtraction of 15 and 8 is: 7

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
#include <stdio.h>

int main() {
    // Step 1: Declare variables
    int num, digit, sum = 0;

    // Step 2: Input number
    printf("Enter a number: ");
    scanf("%d", &num);

    // Step 3: For loop to iterate through each digit
    for (int temp = num; temp > 0; temp /= 10) {
        digit = temp % 10;  // Step 4: Extract rightmost digit
        if (digit % 2 != 0) {  // Step 5: Check if digit is odd
            sum += digit;      // Add to sum
        }
    }

    // Step 6: Print the sum of odd digits
    printf("Sum of odd digits = %d\n", sum);

    return 0;
}


## OUTPUT:
Enter a number: 54879
Sum of odd digits = 21




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
#include <stdio.h>

// Step 2: Declare the function
void fact();

int main() {
    // Step 3: Call the fact() function
    fact();
    return 0;
}

// Step 4: Define the fact() function
void fact() {
    int i, N;
    long long factorial = 1;  // Use long long for larger factorials

    // Step 4b: Read input
    printf("Enter a positive integer: ");
    scanf("%d", &N);

    // Check for valid input
    if (N < 0) {
        printf("Factorial is not defined for negative numbers.\n");
        return;
    }

    // Step 4c: Calculate factorial
    for (i = 1; i <= N; i++) {
        factorial *= i;
    }

    // Step 4d: Print result
    printf("Factorial of %d is: %lld\n", N, factorial);
}


## OUTPUT:
Enter a positive integer: 5
Factorial of 5 is: 120

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
