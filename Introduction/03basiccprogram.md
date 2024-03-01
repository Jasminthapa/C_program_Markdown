+++
title = "Basic C Programming Examples"
weight = 3
description = "Explore basic C programs, including a Hello World program, printing a name, and performing basic calculations such as addition, subtraction, multiplication, and division. Understand the syntax and structure of C programs with detailed explanations."
keywords = "C programming, Hello World in C, printing name in C, basic calculation in C, C program structure, C syntax"
+++
### Basic C program
- Basically here is the program to print a simply hello world in the C.
```c
#include<stdio.h>
void main() { 
   printf("Hello World!"); 
}
```
### Basic C Program Explained
- We need to use #include<stdio.h>inoder to provides functions like printf() for output and scanf() for input, allowing you to display messages to the user and read input from the keyboard.
- int main() is the starting point where the execution of your program begins.
- Every program starts with a main function.
- The curly braces {} represent the beginning and the ending of a block of code.
- Each code statement must end with a semicolon.
### Basic C Program For Printing Name

Certainly! Here's a simple C program that prints out a name:
```c
#include <stdio.h>
int main() {
        char name[] = "Sadikshya subedi";
    // Print the name
    printf("My name is: %s\n", name);
    return 0;
}
```

## C program for Basic Calculation
- Performing addition, subtraction, multiplication, and division in C.
//This program execute division if second no isn't zero.
```c
int main() {
    float num1, num2;
    float sum, difference, product,division;
    // Taking user input
    printf("Enter first number: ");
    scanf("%f", &num1);
    printf("Enter second number: ");
    scanf("%f", &num2);
    // Performing addition, subtraction, and multiplication and division
    sum = num1 + num2;
    difference = num1 - num2;
    product = num1 * num2;
    division=num1/num2;
    printf("Addition: %f", sum);
    printf("Subtraction: %f", difference);
    printf("Multiplication: %f",product);
    printf("division is %f",division);
    return 0;
}

```


