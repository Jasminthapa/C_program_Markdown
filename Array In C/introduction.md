+++
title = "Introduction to Array in C"
weight = 2
description = "Learn about arrays in C, their types, advantages,disadvantages of Array ,declaration of Array, and examples."
keywords = "C arrays, single-dimensional array, multi-dimensional array, advantages and disadvantages of arrays in C"
+++

### Introduction to Array
Array is a group of similar datatype that share a common name. It allows us to store data items stored at contiguous memory locations.The array is the simplest data structure where each data element can be randomly accessed by using its index number.  It makes easier to manage and manipulate a large set of data.It is static data type i.e it has a fixed size in memory.

Suppose we have 1000 of data of students.We can define 100 scanf() to store value.But if we use array we can simply write num[100] ,which can store 100 data with  process.

{{% notice info% %}}
**Note**:It makes code easier and faster.{{% /notice% %}}
### Types of array
- Single dimensional array
- Multi dimensional array
### Advantages Of Array
- Multiple data items can be stored by single name.
- makes program short and hence easy to debug.
-  Use less code to the access the data.
### Declaration of C Array
We can declare array by following syntax:
```c
type arrayName [ arraySize ];
```
### Program Without array
In the given example without using arrays, individual variables (data_point_1, data_point_2, data_point_3,data_point_4,data_point_5 etc.) are used to store each data point.
```
#include <stdio.h>

int main() {
    
    int data_point_1 = 10;
    int data_point_2 = 20;
    int data_point_3 = 30;
    int data_point_4 = 40;
    int data_point_5 = 50;
   

    // Performing operations
    int sum = data_point_1 + data_point_2 + data_point_3+data_point_4+data_point_5;
    
    int count = 3;  // Number of data points

    // Calculating average
    float average = (float)sum / count;

    // Displaying result
    printf("Average: %.2f\n", average);

    return 0;
}
```
### Program Using Array
Using arrays, a single array (data_points) is used to store all the data points.
```c
#include <stdio.h>

int main() {
    // Using an array with larger data
    int data_points[] = {10, 20, 30, 40, 50, 60, 70, 80, 90, 100};
   
    // Performing operations
    int sum = 0;
    int count = sizeof(data_points) / sizeof(data_points[0]);
    for (int i = 0; i < count; i++) {
        sum += data_points[i];
    }
    
    // Calculating average
    float average = (float)sum / count;

    // Displaying result
    printf("Average: %.2f\n", average);

    return 0;
}
```

### Disadvantage Of Array
- allocated memory can't  be increased or decreased if once declared.
- If the array size is declared larger than necessary, it can lead to memory wastage. If we allocate less memory, it will create problem.

