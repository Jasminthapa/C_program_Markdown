+++
title = "Pointer and Array in C"
weight = 3
description = "Learn how to use pointers with arrays in C programming. Understand the relationship between 1-D and 2-D arrays and pointers. Examples provided for practical comprehension."
keywords = "C programming, pointers and arrays, array pointers, 1-D array pointer, 2-D array pointer, relationship between array and pointer"
+++

### Pointer And Array
Not only a pointer to a single variable.We can also point the whole array using pointers.Using array pointer we can easily manipulate the multi dimensional array.
```c
#include <stdio.h>

int main() {
  int myNumbers[5] = {5, 10, 15, 20,25};
  int (*p)[n];

  for (i = 0; i < 5; i++) {
    printf("%d\n", *(n+i));
  }//defrencing the value

  return 0;
}
```
Here,pointer p points the entire array n.
### Relationship between Array and Pointer
An array is a block of sequential data.In most contexts,array names decay to pointers.We can use pointer to access elements of array.
### Relationship between 1-D array and Pointer
A pointer represents the base address of the array.If n is a 1-D array,then:
- Address of the first array element can be expressed as &n[0] or simply n.
- Address of the second array element can be expressed as &n[1] or simply n+1.
- Address of the third  array element can be expressed as &n[2] or simply n+2.
Address of the (i+1) array element can be expressed as &n[i] or simply n+i.
### To Display Address and Value of 1-D array Using Pointer
```c
#include <stdio.h>

int main() {
    int numbers[5],i;

    // Accepting five numbers from the user
    printf("Enter five numbers:\n");
    for (i = 0; i < 5; ++i) {
        printf("Number %d: ", i + 1);
        scanf("%d", &numbers[i]);
    }

    // Displaying values and addresses using pointers
    printf("\nValues and addresses of the array:\n");
    for (i = 0; i < 5; ++i) {
        int *ptr = &numbers[i];
        printf("Value at address %p: %d\n", (void*)ptr, *ptr);
    }

    return 0;
}

```
### Example Sum of 5 numbers using pointer
```c
#include<stdio.h>

int main()

{

int i, n[5],sum=0;

printf("Enter the five numbers");

for ( i=0;i<5;i++)

{

scanf("%d",n+i);

sum =sum+ *(n+i);

}

printf("the sum is %d",sum);

return 0;

}
```
### Relationship between 2-D array and Pointer
- Address of the element in the first row and first column can be expressed as &matrix[0][0] or simply matrix.
- Address of the element in the second row and first column can be expressed as &matrix[1][0] or simply matrix + 1.
- Address of the element in the first row and second column can be expressed as &matrix[0][1] or simply (*matrix) + 1.
- Address of the element in the second row and second column can be expressed as &matrix[1][1] or simply (*(matrix + 1)) + 1.
- Generalizing, the address of the element in the (i+1) row and (j+1) column can be expressed as &matrix[i][j] or simply (*(matrix + i)) + j.

### Example-1:To Display Value and Address of 2-D array Using Pointer
```c
#include <stdio.h>

int main() {
    // Declare a 2D array
    int matrix[3][4];

    // Get user input for matrix elements
    printf("Enter elements for the 3x4 matrix:\n");
    for (int i = 0; i < 3; ++i) {
        for (int j = 0; j < 4; ++j) {
            printf("Enter element at position [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }

  
    printf("\nUsing pointers with addresses and values:\n");
    for (int i = 0; i < 3; ++i) {
        for (int j = 0; j < 4; ++j) {
            // Calculate the memory address using pointers
            int *ptr = &matrix[i][j];
            printf("Address: %p, Value: %2d\n", (void*)ptr, *ptr);
        }
    }

    return 0;
}

```







