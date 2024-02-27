+++
title = "Single Dimensional Array in C"
weight = 2
description = "Learn about single-dimensional arrays in C, their syntax,run time initialization and compile time initialization in C and examples."
keywords = "C arrays, single-dimensional array, array initialization in C"
+++
### Single Dimensional Array
 Single dimensional array uses only one subsript to specify a particular element of the array.Syntax of Single dimensional array is given by:
 ```c
 datatype arrayname[size];
 ```
 e.g:
 ```c
 float num[10];
 ```
 Here,float specifies datatype
 num specifies arrayname
 size specifies maximum no of elements.
 
{{% /notice% %}}num[0]is the first location of first elements.Size range from 0 to (n-1){{% /notice% %}}
### Initialization of 1-D Array
- Compile Time initialization
- Run Time initialization
### Compile Time initialization
Compile-time initialization refers to the process of assigning values to variables or data structures at compile time.This means that the values are known and set during the compilation phase of the program rather than when the program is executed.
We can initialize by:
```c
int myArray[] = {1, 2, 3, 4, 5};
```
### Example 
```c

#include <stdio.h>

// Compile-time initialization
const int compileTimeValue = 10;

int main() {
    // Runtime initialization
    int runtimeValue;

    printf("Enter a value: ");
    scanf("%d", &runtimeValue);

        int result = compileTimeValue + runtimeValue;

    printf("Compile-time value: %d\n", compileTimeValue);
    printf("Runtime value: %d\n", runtimeValue);
    printf("Result: %d\n", result);

    return 0;
}
```
### Run Time initialization
 Variable values are assigned during runtime, and the program performs its operations based on those values.
 ```c
 #include <stdio.h>

int main() {
    // Runtime initialization of a single-dimensional array
    
    int size;
    printf("Enter the size of the array: ");
    scanf("%d", &size);

    int myArray[size];

    printf("Enter %d integer values for the array:\n", size);

       int i = 0;
    while (i < size) {
        printf("Element %d: ", i + 1);
        scanf("%d", &myArray[i]);
        i++;
    }
    // Displaying the values in the array
    printf("Array values: ");
      i = 0;
    while (i < size) {
        printf("%d ", myArray[i]);
        i++;
    }

    return 0;
}

```
### Example To Display Largest Number In Given Array Using Single Dimensional Array.
```c
#include <stdio.h>

int main() {
    int i;
    // Declare and initialize a single-dimensional array
    int myArray[] = {10, 45, 23, 67, 12, 89, 34, 56, 78, 9};  
    int size = sizeof(myArray) / sizeof(myArray[0]); // Calculate the size of the array
    int largest = myArray[0]; // Assume the first element is the largest

    for ( i = 1; i < size; ++i) {
        if (myArray[i] > largest) {
            largest = myArray[i];
        }
    }
       printf("The largest number in the array is: %d\n", largest);
    return 0;
}
```
### Example 2 To Demonstrate Compile Time Initialization of 1-D Array.

```c
#include<stdio.h>  
int main(){      
int i=0;    
int marks[5]={20,30,40,50,60};//declaration and initialization of array    
 //traversal of array    
for(i=0;i<5;i++){      
printf("%d \n",marks[i]);    
}    
return 0;  
}
```
### Example 3 For Sorting an Array
```c
#include<stdio.h>    
void main ()    
{    
    int i, j,temp;     
    int a[10] = { 100, 90, 70, 102, 23, 44, 12, 88, 14, 13};     
    for(i = 0; i<10; i++)    
    {    
        for(j = i+1; j<10; j++)    
        {    
            if(a[j] > a[i])    
            {    
                temp = a[i];    
                a[i] = a[j];    
                a[j] = temp;     
            }     
        }     
    }     
    printf("Printing Sorted Element List ...\n");    
    for(i = 0; i<10; i++)    
    {    
        printf("%d\n",a[i]);    
    }    
} 
```


