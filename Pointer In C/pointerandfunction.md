+++
title = "Pointer and Function in C"
weight = 4
description = "Understand how to use function pointers in C programming. Learn about the declaration, calling functions through pointers, and practical examples including swapping values, mathematical operations, and displaying marks."
keywords = "C programming, function pointers, declaration of function pointer, calling function through pointer, swap using function pointer, mathematical operations with function pointer"
+++


### Pointer And Function
A **pointer** is a variable that stores the memory address of another variable. In programming, pointers provide a way to access and manipulate the memory directly. 
A **function** is a self-contained block of code that performs a specific task.
A **function pointer** points to the memory address, where the function's code is stored. We can get the address of memory by using the function pointer.
### Declaration of a Function Pointer

```c
return type (*ptr_name)(type1, type2…);  
```
For example:
```c
int (*) ptr(int);
``` 
*ptr is a pointer that points to a function which returns an int value.
### Calling a function through a function pointer

Suppose we declare a function as given below:
```c
float function(int , int);   // Declaration of a function.  
```
Now,we call the function in usual way by:
```c
result = function(x, y); 
```
Calling a function using a function pointer is given below:
```c 
result = (*fptr)( x , y);    // Calling a function using function pointer.
```  
Or
```c
result = fptr(a , b);
```
### Example using Function Pointer To Display Marks Of Ram.
```
 #include <stdio.h>
void marks(int x)
{
    printf("Ram got %d marks in science.\n", x);
}

int main()
{
    void (*ptr1)(int) = marks;
    ptr1(20);
    return 0;
}
```

### To add and subtract using function pointer.
```
#include <stdio.h>

int add(int, int);
int subtract(int, int);
int multiply(int, int);
int divide(int, int);

int main() {
    int a, b;
    int (*ptr)(int, int);
    int result;

    printf("Enter the values of a and b : ");
    scanf("%d %d", &a, &b);

    // Addition
    ptr = add;
    result = (*ptr)(a, b);
    printf("Value after addition is : %d\n", result);

    // Subtraction
    ptr = subtract;
    result = (*ptr)(a, b);
    printf("Value after subtraction is : %d\n", result);

    // Multiplication
    ptr = multiply;
    result = (*ptr)(a, b);
    printf("Value after multiplication is : %d\n", result);

    // Division
   ptr = divide;
    result = (*ptr)(a, b);
    printf("Value after division is : %d\n", result);

    return 0;
}

int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}

int multiply(int a, int b) {
    return a * b;
}

int divide(int a, int b) {
    if (b != 0) {
        return a / b;
    } else {
        printf("Error: Division by zero\n");
        return 0;
    }
}
  
```
### Example: to Swap Values Of Two Variables Using Function Pointer.
```c

#include <stdio.h>

void swap(int * p , int * q)

{

int temp;
temp = *p;
*p = *q;
*q=temp;
}

int main ()
{
int x,y;
printf("Enter the values of x and y : " );
scanf("%d%d",&x,&y);
printf("Before swap, value of x = %d and y = %d \n", x, y );
swap(&x,&y);
printf("After swap, value of x = %d and y= %d \n", x, y);
return 0;
}
```
