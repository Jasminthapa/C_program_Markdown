+++
title = "Pointer Arithmetic in C"
weight = 2
description = "Explore pointer arithmetic in C, including addition, subtraction, increment, decrement, and comparison. Understand how pointer arithmetic works with examples for better comprehension."
keywords = "C programming, pointer arithmetic, pointer addition, pointer subtraction, increment pointer, decrement pointer, comparison pointer"
+++

### Pointer Arithmetic
Pointer arithmetic is a feature in C that allows you to perform arithmetic operations on pointers.Following arithmetic operations are possible on the pointer in C language:
- Addition
- Subtraction
- Increment
- Decrement
- Comparison

### C Pointer Addition
We can add a value to the pointer variable.Addition any number from a pointer will give an address.
The following is the formula for adding the pointer::
```c
new_address= current_address + (number * size_of(data type))  
```
### Example
```c
#include<stdio.h>  
int main(){  
int number=70;        
int *p;//pointer to int      
p=&number;//stores the address of number variable        
printf("Address of p variable is %u \n",p);        
p=p+5;   //adding 5 to pointer variable    
printf("After adding 5: Address of p variable is %u \n",p);       
return 0;  
}  
```
### C Pointer Subtraction
We can subtract a value to the pointer variable.Subtraction any number from a pointer will give an address.The following is the formula for subtracting the pointer:
```c
new_address= current_address - (number * size_of(data type))  
```
### Example
```c
#include<stdio.h>  
int main(){  
int number=70;        
int *p;//pointer to int      
p=&number;//stores the address of number variable        
printf("Address of p variable is %u \n",p);        
p=p-5;   //subtracting 5 to pointer variable    
printf("After subtracting 5: Address of p variable is %u \n",p);       
return 0;  
}
```
### Increment Pointer
This pointer will start pointing to the immediate next location.This pointer will start pointing to the immediate next location.
The following is the formula for incrementing the pointer:
```c
new_address= current_address + i * size_of(data type)  
```
### Example
```c
#include<stdio.h>  
int main(){  
int num=90;        
int *ptr;//pointer to int      
ptr=&num;//stores the address of number variable        
printf("Address of ptr variable is %u \n",ptr);        
ptr=++ptr;        
printf("After increment: Address of ptr variable is %u \n",ptr);       
return 0;  
}
```
### For Array
```c
#include <stdio.h>

int main() {
    int arr[] = {0,1, 2, 3, 4, 5};
    int *ptr = &arr[1]; // Pointing to the third element (index 2)

    printf("Original value: %d at address %p\n", *ptr, (void*)ptr);

    // Incrementing the pointer to move to the next element
    ptr++;

    printf("After incrementing: %d at address %p\n", *ptr, (void*)ptr);

    return 0;
}
```
### Decrement pointer
This pointer will start pointing to the immediate previous location.This pointer will start pointing to the immediate next location.
The following is the formula for decrementing the pointer:
```c
new_address= current_address + i * size_of(data type)  
```
### Example

```c
#include<stdio.h>  
int main(){  
int num=90;        
int *ptr;//pointer to int      
ptr=&num;//stores the address of number variable        
printf("Address of ptr variable is %u \n",ptr);        
ptr=--ptr;        
printf("After increment: Address of ptr variable is %u \n",ptr);       
return 0;  
}
```
### For Array
```
#include <stdio.h>

int main() {
    int arr[] = {0, 1, 2, 3, 4, 5};
    int *ptr = &arr[2]; // Pointing to the third element (index 2)

    printf("Original value: %d at address %p\n", *ptr, (void*)ptr);

    // Decrementing the pointer to move to the previous element
    ptr--;

    printf("After decrementing: %d at address %p\n", *ptr, (void*)ptr);

    return 0;
}
```
### Comparision Pointer
We can compare the two pointers by using the comparison operators in C. We can implement this by using all operators in C >, >=, <, <=, ==, !=.  It returns true for the valid condition and returns false for the unsatisfied condition. 
### Example
```c
#include <stdio.h>

int main() {
    int arr[5] = {5, 10, 15, 20, 25};

    // Pointers to array elements
    int *ptr1 = &arr[3];  // points to the third element (15)
    int *ptr2 = &arr[6];  // points to the fifth element (25)

    // Compare pointers
    if (ptr1 == ptr2) {
        printf("ptr1 and ptr2 point to the same location.\n");
    } else {
        printf("ptr1 and ptr2 do not point to the same location.\n");
    }

    // Compare addresses
    if (ptr1 < ptr2) {
        printf("ptr1 comes before ptr2 in memory.\n");
    } else {
        printf("ptr1 does not come before ptr2 in memory.\n");
    }

    return 0;
}
```
