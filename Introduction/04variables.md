+++
title = "Variables in C"
weight = 4
description = "Variables are containers used to store value in the program.Learn about variables, data types, and constants in C programming. Understand naming conventions for variables in C."
keywords = "variables in C, data types in C, C constants, naming conventions in C,types of variables in C"
+++
### Variables 
- A variable in a program is a name given to memory loctaion that stores the value which can change throughout the program.
- Simply, a variable is just a container which stores value.For eg:

```c
int num = 10;
```
Here num is a variable of integer type with integer value 10
Simply,syntax of variables can be declared as
Datatype variablename1,variablename2,.....;
For eg: 
- Variable can be String or numeric.

### Variable Types
- int:Used for storing whole numbers.e.g:10, -10, 996
- float:Used for storing decimal numbers with single precision.E.g.10.0, -10.2, 85.698 etc.
- double:Used for storing decimal numbers with double precision.E.g.3.14159, 4.3335 etc.
char:Used for storing individual characters.E.g.'A','B'etc.
- Bool:Used for storing true or false values.E.g. true, false [Only stores true or false values]


### Example

```c
#include <stdio.h>

int main() {
    // Declaring Variables
    char name[] = "John";
    char address[] = "USA";
    int age = 20;
    float height = 5.9;
    _Bool isMarried = 0; // 0 represents false in C

    // Printing variables value
    printf("Name is %s\n", name);
    printf("Address is %s\n", address);
    printf("Age is %d\n", age);
    printf("Height is %.2f\n", height); // %.2f for two decimal places
    printf("Married Status is %s\n", isMarried ? "true" : "false");

    return 0;
}
```
{{% notice info %}}**Note**:Here \n is used for next line.
{{% /notice %}}

### Rules for writting variables In C**
- Must begin with alphabets or an underscore.
- The lowercase and uppercase are different.For eg:name and Name is different.
- Keywords can't be as variable name.
- White space should be avoided between variables names.But we can use underscore to join.
- Only 31 characters are significant.

### C Constant
Constant is the type of variable whose value never changes. In programming, changeable values are mutable and unchangeable values are immutable. Sometimes, you don’t need to change the value once declared. Like the value of PI=3.14, it never changes. To create a constant in C, you can use the #define keyword.
```c 
#include <stdio.h>

#define PI 3.1
int main() {
    printf("Value of PI: %f\n", PI);
 return 0;
}
```
## Naming Convention For Variables In C
It is a good habit to follow the naming convention.  Variables, the variable name should start with lower-case_letter, and use underscores to seprate the words.Technically, this naming convention is called snake_case.
For eg:
```c
 char full_name;
int global_variable;
```
