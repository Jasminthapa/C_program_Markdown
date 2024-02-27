+++
title = "Data Types in C"
weight = 4
description = "Understand the various data types in C programming, including fundamental data types like int, float, double, and char. Explore examples of using built-in types and derived data types such as arrays, structures, and unions."
keywords = "C programming, data types in C, fundamental data types, derived data types"
+++

### Data Types in C
As explained in the Variables chapter, a variable in C must be a specified data type, and you must use a format specifier inside the printf() function to display it:The data type specifies what type of value will be stored by the variable. Each variable has its data type.C supports following data types
- int
- float
- double
- char
- bool
```c
#include<stdio.h>
int main()
{
//create variables
int num=5;
char letter="D";
// print variables
printf("%d",num);
printf("c",letter);
}
```
### Built-In Types
In C language, there is the type of values that can be represented and manipulated. The data type classification is as given below:
### Fundamental datatype
These are the basic datatypes are used in c. Primary data types are the basic building blocks for representing different kinds of values. There are diffrent kinds of fundamental datatype:
1) int
2) char
3) float
4) double

| Data Type          | Description                                                | Example                     |
|---------------------|------------------------------------------------------------|-----------------------------|
| `int`               | Used for representing integers (whole numbers).             | `int number = 42;`          |
| `char`              | Used for representing individual characters.               | `char letter = 'A';`        |
| `float`             | Used for representing single-precision floating-point numbers. | `float pi = 3.14;`         |
| `double`            | Used for representing double-precision floating-point numbers. | `double price = 9.99;`     |
1) **Integer datatype**

Integer data types are used to store whole number.In C, the signed are used to  and unsigned modifiers are used to store both positive and negative values and  unsinged are store only non-negative values.

| Data Type                 | Description                                               | Example                                   |
|---------------------------|-----------------------------------------------------------|-------------------------------------------|
| `short int` or `signed short int` | Represents a short range of signed integers.               | `short int temperature = -10;`            |
| `unsigned short int`      | Represents non-negative short integers.                    | `unsigned short int count = 100;`         |
| `int` or `signed int`     | Represents signed integers within a specific range.        | `int age = 25;`                            |
| `long` or `signed long int`| Represents a wider range of signed integers.               | `long population = 7000000000L;`          |
| `unsigned long int`       | Represents non-negative long integers.                     | `unsigned long int distance = 1500;`      |
2) **Floating data type**

store fractional part and its value.

| Data Type      | Description                                      | Example                     |
|-----------------|--------------------------------------------------|-----------------------------|
| `float`         | Single-precision floating-point number.          | `float pi = 3.14;`         |
| `double`        | Double-precision floating-point number.          | `double price = 9.99;`     |
| `long double`   | Extended precision floating-point number.        | `long double bigValue = 123456789.987654321;` |
3) Double Datatype
 Double datatype is used to represent double-precision floating-point numbers. It is a 64-bit data type.It provides greater precision than the float data type.

4) Character Datatype

| Data Type            | Description                                  | Example                       |
|-----------------------|----------------------------------------------|-------------------------------|
| `signed char`        | Signed character type, can represent positive or negative values. | `signed char temperature = -5;` |
| `unsigned char`      | Unsigned character type, represents only non-negative values.      | `unsigned char count = 100;`   |

### Derived datatype
The data type which are created using the already exisiting primitive and fundamental types are known as derived data types.Examples:
1) Array,
2) Structure,
3) union.

| Derived Data Type | Description                                              | Example                                   |
|-------------------|----------------------------------------------------------|-------------------------------------------|
| **Arrays**        | Collection of elements of the same data type in a fixed-size sequence. | `int numbers[5] = {1, 2, 3, 4, 5};`       |
| **Structures**    | User-defined type grouping variables under a single name. | `struct Person { char name[50]; int age; };` |
| **Unions**        | Similar to structures, but all members share the same memory location. | `union Value { int intValue; float floatValue; char stringValue[20]; };` |






