+++ title = "Types Of Functions in C" 
weight = 2 
description = "Explore different types of functions in C, including examples of functions with no parameters and no return type, functions with parameters and no return type, functions with no parameters and return type, and functions with parameters and return type."
 keywords = "types of functions in C, functions with parameters, functions with return type, functions with no return type." +++


### Types Of Function
Functions are the block of code that performs a specific task. Here are different types of functions:
- No Parameter And No Return Type
- Parameter And No Return Type
- No Parameter And Return Type
- Parameter And Return Type
### Function With No Parameter And No Return Type
In this function, you do not pass any parameter and no return type.Here is an example of it.
### Example 1: No Parameter & No Return Type
Here printName() is a function which prints name on screen.
```c
#include <stdio.h>
void main() {
  printName();
}

void printName() {
  printf("My name is John Doe.");
  ;
}
```
### Example 2: No Parameter & No Return Type
Here printPrimeMinisterName() is a function which prints prime minister name on screen.
```c
#include <stdio.h>
void printPrimeMinisterName() {
  printf("John Doe.\n");
}
void main() {
  printf("Function With No Parameter and No Return Type\n");
  printPrimeMinisterName();
}
```
### Function With Parameter And No Return Type
In this function, you do pass the parameter and expect no return type. Here is an example of it:
### Example 1: Parameter & No Return Type
Here, in this example printSum() takes two integer parameters a and b and calculates their sum.
```c
#include <stdio.h>

// Function with parameters and no return type
void printSum(int a, int b) {
    int sum = a + b;
    printf("The sum of %d and %d is: %d\n", a, b, sum);
}

int main() {
    int num1 = 10;
    int num2 = 20;

    // Calling the function
    printSum(num1, num2);

    return 0;
}
```
### Example 2: No Parameter & No Return Type
Here circleArea() is a function which returns area of a circle.

Here 
```c
#include<stdio.h>

void circleArea();
// function prototype

 int main() // Main function

{

circleArea();
return 0;

}

void circleArea() //user defined function

{

float area;

float radius;

printf("Enter the radius : \n");

scanf("%f",&radius);

area = 3.14 * radius * radius ;

printf("Area of Circle is %f",area);

}
```
### Function With Parameter And No Return Type
Here calculateRectangleArea() is a function which returns area of a rectangle.
```c
#include <stdio.h>

void calculateRectangleArea(int length, int width) {
    int area = length * width;
    printf("The area of the rectangle is: %d\n", area);
}

int main() {
    int rectLength = 5;
    int rectWidth = 10;

    // Function call with parameters
    calculateRectangleArea(rectLength, rectWidth);

    return 0;
}
```
### Function With Parameter And Return Type

```c
#include <stdio.h>

float circleArea(int);

 int main()

{

int radius;

float a;

printf("Enter the radius of the circle ");

scanf("%d",&radius);

a = circleArea(radius);

printf("\n Area of Circle is %f ",a);
return 0;

}

float circleArea(int r)

{

float area;

area = 3.14 * r * r;

return(area);

}

```








