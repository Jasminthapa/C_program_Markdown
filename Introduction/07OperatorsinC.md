+++
title = "Operators in C"
weight = 4
description = "Learn about operators in C programming, including arithmetic, increment and decrement, assignment, relational, logical, and conditional operators. Explore examples and understand the types of operators based on operands."
keywords = "C programming, operators in C, arithmetic operators, increment and decrement operators, assignment operators, relational operators, logical operators, conditional operators"
+++


### Operators In C
Operators are used to perform mathematical and logical operations on the variables. Each operation in C uses a symbol called the operator to denote the type of operation it performs. Before learning operators in the C, you must understand the following things.
- Operands : It represents the data.
- Operator : It represents how the operands will be processed to produce a value.

For eg: Suppose the given expression is 5 + 4. Here 5 and 4 are operands, and + is the operator.

### Types Of Operators
- Arithmetic Operators
- Increment and Decrement Operators
- Assignment Operators
- Logical Operators
- Relational Operators
- Conditional/Ternary Operators
  
#### Arithmetic Operators
Arithmetic operators are the most common types of operators. They perform operations like addition, subtraction, multiplication, division,modulus etc.
- **Addition (+)**: Adds two operands.
- **Subtraction (-)**: Subtracts one operand from another.
- **Multiplication (*)**: Multiplies two operands.
- **Division (/)**: Divides one operand by another.
- **Modulo or Remainder (%)**: Returns the remainder of division.

```c
#include <stdio.h>
int main() {
    // declaring two numbers
    int num1 = 20;
    int num2 = 3;
    
    // performing arithmetic calculation
    int sum = num1 + num2;       // addition
    int diff = num1 - num2;      // subtraction
    int mul = num1 * num2;       // multiplication
    double div = (double)num1 / num2;  // division
    int mod = num1 % num2;       // remainder
    // Printing info
    printf("The addition is %d.\n", sum);
    printf("The subtraction is %d.\n", diff);
    printf("The multiplication is %d.\n", mul);
    printf("The division is %.2f.\n", div); // %.2f specifies two decimal places
    printf("The modulus is %d.\n", mod);

    return 0;
}
```
### Increment and Decrement Operators
In C, increment is used to increased the value by 1 and decrement is used to decrease the value by 1.If ++ is used at the beginning, then it is a prefix. If it is used at last, then it is postfix.

 **Prefix and postfix Increment operator**
- In **prefix increment**,first value is increased by 1 and assinged it to the left side variable.
```c
int a=5;
b=++a
```

- In **Postfix Increment**,firstly,value is assinged to the left side variable and then operand is increased by 1.For example:
```c
int a=5;
b=a++
```
```c
#include <stdio.h>

int main() {
    int num = 10;
    int result;

    // Prefix increment operator
    result = ++num; // Increment 'num' by 1 before using its value
    printf("Prefix increment: num = %d, result = %d\n", num, result);

    num =20; // Reset num to 20

    // Postfix increment operator
    result = num++; // Use the value of 'num' and then increment it by 1
    printf("Postfix increment: num = %d, result = %d\n", num, result);

    return 0;
}
```
### **Prefix and Postfix Decrement Operator**
- In **Prefix Decrement**,firstly 1 is subtracted from the operand and result is assinged to the left side variable.For example:
```c
int a=6;
b=--a
```

- In **Postfix Decrement**,firstly,value is assinged to the left side variable and then operand is decreased by 1.For example:
```c
int a=5;
b=a--
```
Both can be represented in program as:
```c
#include <stdio.h>

int main() {
    int num = 8;
    int result;

    // Prefix decrement operator
    result = --num; // Decrement 'num' by 1 before using its value
    printf("Prefix decrement: num = %d, result = %d\n", num, result);

    num = 8; // Reset num to 8

    // Postfix decrement operator
    result = num--; // Use the value of 'num' and then decrement it by 1
    printf("Postfix decrement: num = %d, result = %d\n", num, result);

    return 0;
}
```
### Assignment operator
Assigns the result of an expression.
- **Simple Assignment Operator(=)**:Assigns the value of the right-hand operand to the left-hand operand.
- **Addition Assignment Operator(+=)**:Adds the value of the right-hand operand to the left-hand operand and assign the result to the left.
- **Subtraction Assignment Operator(-=)**:Subtracts the value of the right-hand operand from the left-hand operand and assign the result to the left.
-  **Multiplication Assignment Operator(*=)**: Multiply the left-hand operand by the value of the right-hand operand to the  left-hand operand.
- **Division Assignment Operator(/=)**: Divides the left-hand operand by the value of the right-hand operand.
- **Modulo Assignment Operator(%=)**:Computes the remainder of the division of the left-hand operand by the right-hand operand and assigns the result to the left-hand operand.
```c
#include <stdio.h>
int main() {
    int num = 11;
    num += 5; // Equivalent to: num = num + 5;
    printf("num after addition is: %d\n", num); 
    num -= 3; // Equivalent to: num = num - 3;
    printf("num after subtraction is: %d\n", num);
    num *= 2; 
    printf("num after multiplication is: %d\n", num);
    num /= 4; // Equivalent to: num = num / 4;
    printf("num after division is: %d\n", num);
    num %= 5; // Equivalent to: num = num % 5;
    printf("num after modulus is: %d\n", num);
    return 0;
}
```
#### Relational Operators:
 Compare two operands and return a boolean value (true or false) based on the comparison.
 - **Equal to (==)**: Checks if two operands are equal or not.
 - **Not equal to (!=)**: Checks if two operands are not equal.
 - **Greater than (>)**: Checks if the left operand is greater than the right.
 - **Less than (<)**: Checks if the left operand is less than the right.
 - **Greater than or equal to (>=)**: Checks if the left operand is greater than or equal to the right.
-  **Less than or equal to (<=)**: Checks if the left operand is less than or equal to the right.
Let's see an example of reltional operators.
```c
#include <stdio.h>

int main() {
    int a = 40;
    int b = 50;

    // Less than (<)
    if (a < b) {
        printf("a is less than b\n");
    } else {
        printf("a is not less than b\n");
    }

    // Greater than (>)
    if (a > b) {
        printf("a is greater than b\n");
    } else {
        printf("a is not greater than b\n");
    }

    // Less than or equal to (<=)
    if (a <= b) {
        printf("a is less than or equal to b\n");
    } else {
        printf("a is not less than or equal to b\n");
    }

    // Greater than or equal to (>=)
    if (a >= b) {
        printf("a is greater than or equal to b\n");
    } else {
        printf("a is not greater than or equal to b\n");
    }

    // Equal to (==)
    if (a == b) {
        printf("a is equal to b\n");
    } else {
        printf("a is not equal to b\n");
    }

    // Not equal to (!=)
    if (a != b) {
        printf("a is not equal to b\n");
    } else {
        printf("a is equal to b\n");
    }

    return 0;
}   
```
 #### Logical Operators
 Used to test one or more than one conditions to make decision.Basically there are three types of logical operators.
 - **Logical AND**:Returns true if all conditions are true.For eg:
 ```c
 #include <stdio.h>

int main()
{
    int a = 40, b = 20;
 
    if (a > 0 && b > 0) {
        printf("Both values are greater than 0\n");
    }
    else {
        printf("Both values are less than 0\n");
    }
    return 0;
}
```
 - **Logical OR (||)**:Return true if one of the conditions is true.
 ```c
 #include <stdio.h>
int main()
{
    int a = -100, b = 20;
 
    if (a > 0 || b > 0) {
        printf("Any one of the given value is "
               "greater than 0\n");
    }
    else {
        printf("Both values are less than 0\n");
    }
    return 0;
}
```
 - **Logical NOT (!)**:Return false if the result is true and vice versa.
 ```c
 #include <stdio.h>
int main()
{
    int a = 10, b = 20;
 
    if (!(a > 0 && b > 0)) {
                printf("Both values are greater than 0\n");
    }
    else {
        printf("Both values are less than 0\n");
    }
    return 0;
}
```
### Conditional/Ternary Operator(?:) 

 Evaluates an expression based on a condition and returns a value.
 ```c
 #include <stdio.h>
int main() {
    int number=3;   

    // Using conditional operator to check if the number is even or odd
    (number % 2 == 0) ? printf("%d is an even number.\n", number) : printf("%d is an odd number.\n", number);

    return 0;
}
```
### Types Of Operators On The Basis Of Operands
1. **Unary operators**- Those operators which only needs one operand .
Examples are:--(decrement),++(increment),+(unary plus),-(unary minus).
```c
x++;
a+=1;
```c
#include <stdio.h>

int main() {
    int num = 15;

    // Increment operator (++)
    printf("Initial value of num: %d\n", num);
    num++; // Increment num by 1
    printf("After increment: %d\n", num);

    // Decrement operator (--)
    num--; // Decrement num by 1
    printf("After decrement: %d\n", num);

    return 0;
}
```
2. **Binary operators**- Those operators which  needs two operand .For eg:
```c 
int c,a,b;
c=a+b;
```
```c
Here is  example:
#include <stdio.h>

int main() {
    int a = 50;
    int b = 20;

    // Addition
    int sum = a + b;
    printf("Sum: %d\n", sum);

    // Subtraction
    int difference = a - b;
    printf("Difference: %d\n", difference)
    return 0;
}
```
3. **Ternary operators**- In C programming, the ternary operator 
takes three operands.Syantax is given as:
```c
condition ? expression1 : expression2
```
In this case,condition is evaluated.If condition gives true result ,the expression1 will run and if condition is false,expression2 will run .
```c
#include <stdio.h>

int main() {
    int x = 40;
    int y = 50;

    //  using the ternary operator
    int max = (x > y) ? x : y;

    printf("The maximum value is: %d\n", max);

    return 0;
}
```
