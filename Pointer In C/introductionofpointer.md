+++
title = "Introduction to Pointers in C"
weight = 1
description = "Understand pointers in C programming, including their declaration, initialization, pointer operators, reference operator, dereference operator, types of pointers (void, null, double), and examples for better comprehension."

keywords = "C programming, pointers in C, C pointer declaration, pointer initialization, pointer operators, reference operator, dereference operator, void pointer, null pointer, double pointer"
+++
### Introduction
- Pointers are special variables that store memory addresses of other variables.
- They provide direct access to memory locations, enabling efficient memory management and control.
-  We use the asterisk (*) operator to declare a pointer variable i.e
```c
int *ptr;
```
It signifies **ptr** is a **pointer variable** and it can store the address of integer data type.
### **Pointer Declaration**
General form is:
```c
Datatype *variable_name;
```
- datatype refers to type of data.
- variable name refers  to the name of pointer variable.
- * is used to declare a pointer.
### Pointer initialization
- We use the ampersand (&) operator to get the address of a variable and assign it to a pointer.
```c
int num;
ptr = &num;
```
### Example-1
#include <stdio.h>

int main() {
    // Declare a variable
    int num = 12;

    // Declare a pointer and initialize it with the address of the variable
    int *ptr = &num;

    // Accessing the value through the pointer
    printf("Value of num: %d\n", num);
    printf("Value of num using pointer: %d\n", *ptr);

    // Modifying the value through the pointer
    *ptr = 11;
    printf("Updated value of num: %d\n", num);

    return 0;
}

### Pointer Operator
The pointer operator is used to manipulate and work with pointers in a programming language.There are two special pointer operators and they are * and &. The operator ‘&’ is called ‘address’ of operand
and the operator ‘*’ is called the ‘value pointed by’
that address.
### Reference Operator (&):
The address that locates a variable within memory is
what we call a reference to that variable. This
reference to a variable can be obtained by preceding
the identifier of a variable with ampersand (&) sign
known as reference operator.syntax is given by:
```c
int x = 10;
int *ptr = &x; // ptr now contains the memory address of x
```
### Example
```c
#include<stdio.h>

 int main ()

{

int y=20;

printf(" value of y is %d\n", x);

printf(" Address of y:%u\n", &x);

int *ptr;

ptr= &x; //referencing to x

printf(" Address stored in ptr: %u\n" , ptr);

printf(" value pointed by ptr: %d\n" , *ptr); 
return 0;
}
```

### Dereference operator (*):
 This operator is used to access the value stored at the memory address held by a pointer.
Using a pointer, we can directly access the value stored in
the variable which it points to. To do this we simply have to
proceed the pointer identifier with an asterisk (*) sign
which acts as the reference operator .Thus ‘&’ and ‘*’
operators have complimentary as opposite meaning. A
variable reference with & can be dereference with *.Syntax is given by:
```c
int x = *ptr; // x now contains the value stored at the memory address ptr
```
### Example
```c
#include<stdio.h>

int main ()

{

int x=15;

printf(" value of x is %d\n", x);

printf(" Address of x:%u\n", &x);

int *ptr;

ptr= &x; //referencing to x

printf(" Address stored in ptr: %u\n" , ptr);

printf(" value pointed by ptr: %d\n" , *ptr); //dereferencing
return 0;

}
```
### Types Of Pointer
- void pointer
- Null pointer
- Double pointer

### void pointer
- A pointer that can point to objects of any  data type.
- We can assign the address of any data type to the void pointer, and a void pointer can be assigned to any type of the pointer without performing any explicit typecasting.
- It is often used in generic programming.

### Syntax of void pointer
```
void *pointer name; `
```
### Example
```
#include <stdio.h>  
int main()  
{  
   int x=80;  
   void *ptr;  
   ptr=&x;  
   printf("Value after pointed by ptr pointer : %d",*ptr);  
   return 0;  
} 
``` 
{{% notice info %}} Note:As we already know that the void pointer cannot be dereferenced, so the above code will give the compile-time error because we are printing the value of the variable pointed by the pointer 'ptr' directly. {{% /notice %}}
SO ,in oder to remove the error the program can be written as:
### Example
we typecast the void pointer to the integer pointer by using the statement given below:
```c
(int*)ptr;
```
value of variable is printed by:
```c
*(int*)ptr;
```

```c
#include <stdio.h>  
int main()  
{  
   int a=90;  
   void *ptr;  
   ptr=&a;  
   printf("Value which is pointed by ptr pointer : %d",*(int*)ptr);  
    return 0;  
}  
```
### Example 2
```c
#include <stdio.h>

int main() {
    int intValue = 412;
    float floatValue = 4.14159;
    char charValue = 'A';

    void *ptr; // void pointer

    // Pointing the void pointer to an integer variable
   ptr = &intValue;
    printf("Value of integer pointed to by void pointer: %d\n", *((int *)ptr));

    // Pointing the void pointer to a float variable
   ptr = &floatValue;
    printf("Value of float pointed to by void pointer: %f\n", *((float *)ptr));

    // Pointing the void pointer to a character variable
   ptr = &charValue;
    printf("Value of character pointed to by void pointer: %c\n", *((char *)ptr));

    return 0;
}
```
### Null Pointer
A Null Pointer is a pointer that does not point to any memory location.If a NULL value is assigned to the pointer, then it is considered as a Null pointer.It is a special constant value often represented as **NULL**.
```c
#include <stdio.h>

int main() {
    int *nullPointer = NULL;  // Declaration of a null pointer     
     printf("Value at nullPointer: %u\n", nullPointer);

    // Checking if the pointer is NULL before dereferencing
    if (nullPointer == NULL) {
        printf("The pointer is NULL\n");
    } else {
        printf("Value at nullPointer: %d\n", *nullPointer); // This line won't be executed in this example
    }

    return 0;
}
```
### Double Pointer
In C, a double pointer is a pointer that points to another pointer.It is used when dealing with dynamic memory allocation or when you need to modify a pointer from within a function. 
### Example
Here,**ptr2 is used to access the value pointed to by ptr1.
```c
#include <stdio.h>

int main() {
    int num = 100;
    int *ptr1 = &num;   // Pointer to an integer
    int **ptr2 = &ptr1; // Double pointer, pointing to the address of ptr1

    // Accessing the value using ptr1
    printf("Value using ptr1: %d\n", *ptr1);

    // Accessing the value using ptr2 (double pointer)
    printf("Value using ptr2: %d\n", **ptr2);

    // Modifying the value using ptr2
    **ptr2 = 99;

    // Accessing the modified value using ptr1
    printf("Modified value using ptr1: %d\n", *ptr1);

    return 0;
}
```














