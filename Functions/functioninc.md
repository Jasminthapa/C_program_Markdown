+++ title = "Function in C" 
weight = 1
description = "Learn about functions in C, including advantages, syntax, and examples. Explore programs using functions to print names, find the sum of two numbers, and calculate simple interest." 
keywords = "functions in C, function syntax, function examples, C programming, snake case, function parameters, function arguments." +++
### Function In C
In this tutorial, you will learn about functions in C. Functions are the block of code that performs a specific task.Function are the sub routine to the main program. Function provides encapsulation. They are created when some statements are repeatedly occurring in the program. The function helps reusability of the code in the program.
{{ %notice info %}} 
**Note:**The main objective of the function is DRY(Don’t Repeat Yourself).
{{% /notice %}}
### Function Advantages
- Avoid Code Repetition.
- Easy to divide the complex program into smaller parts.
- Helps to write a clean code.
- Easier to debug,understand by breaking code  into manageable chunks.

### Syntax
```c
returntype functionName(parameter1,parameter2, ...){
  // function body
}
```
- **Return type**: It tells you the function output type. It can be void, String, int, double, etc. If the function doesn’t return anything, you can use int as the return type.

- **Function Name**: You can name functions by almost any name. Always follow a lowerCamelCase naming convention like void printName().

- **Parameters**: Parameters are the input to the function, which you can write inside the bracket (). Always follow a lowerCamelCase naming convention for your function parameter.

### Example 1:Program using Function That Prints Name.
This is a simple program that prints name using function. The name of function is printName().
```c
#include <stdio.h>

// Function definition outside main function
void printName(){
  printf("My name is Raj Sharma. I am from function.\n");
}

// Main function
int main(){
  // Calling the function
  printName();
  return 0;
}
```
### Example 2:Program using Function To Find Sum of Two Numbers
This function finds the sum of two numbers. Here, the function accepts two parameters. i.e., num1 and num2, and the return type is void.
```c
#include <stdio.h>

// Function definition 
void add(int num1, int num2){
  int sum = num1 + num2;
  printf("The sum is %d\n", sum); 
}

// Main function
int main(){
  add(40, 20); // Calling the add function with arguments 10 and 20
  return 0;
}
```
### Example 3:Program using Function That Find Simple Interest.
This function finds simple interest from principal, time and rate and display result.
```c
#include <stdio.h>

// Function definition for calculating simple interest
void calculateInterest(double principal, double rate, double time) {
  double interest = principal * rate * time / 100;
  printf("Simple interest is %lf\n", interest);
}
// Main function
int main() {
  double principal = 5000;
  double time = 3;
  double rate = 3;
  calculateInterest(principal, rate, time); // Calling the calculateInterest function
  return 0;
}
```
### Key Points
- You should follow the snakecase naming convention while naming function.
- You should follow the lowercase naming convention while naming function parameters.

### About snakecase
Name should start with lower-case, and every second word’s  are seprated by underscore.Technically, this naming convention is called snakecase.

### Function Paramaters Vs Arguments
**Parameter**:Parameter is the name and data type you define as an input for your function.
**Argument** is the actual value that you passed in.
```c
#include <stdio.h>

// Function definition for adding two numbers and printing the sum
void add(int num1, int num2){
  int sum;
  sum = num1 + num2;
  printf("The sum is %d\n", sum); 
}

// Main function
int main(){
  // Calling the add function with arguments 10 and 20
  add(10, 20);
  return 0;
}
```
Here in **add(int num1, int num2)**, num1 and num2 are **parameters** and in **add(10, 20)**, 10 and 20 are **arguments**.
