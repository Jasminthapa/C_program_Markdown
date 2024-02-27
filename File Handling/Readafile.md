
+++
title = "Read File in C"
weight = 3
description = "In this section, you will learn how to read a file in the C programming language. The C program demonstrates how to open a file named 'test.txt' and read its content using the 'fscanf' function."
keywords = "read file in C, file handling in C, fscanf function in C, C programming language"
+++

### Introduction To File Handling
File handling is an important part of any programming language. In this section, you will learn how to read the file in a C programming language.
### Read File In C
To read from a file, you can use the r mode:
Assume that you have a file named test.txt in the same directory of your C program.
```c
Welcome to test.txt file.
This is a test file.
```
Now you can read the file using fscanf.
```c
#include <stdio.h>

int main() {
    FILE *filePointer;
    char data[100]; // Adjust the size based on your needs

    // Open the file for reading
    filePointer = fopen("test.txt", "r");

    // Check if the file opened successfully
    if (filePointer == NULL) {
        printf("Error opening the file.\n");
        return 1; // Exit with an error code
    }

    // Read data from the file
    while (fscanf(filePointer, "%s", data) != EOF) {
        // Print the read data
        printf("%s\n", data);
    }

    // Close the file
    fclose(filePointer);

    return 0; // Exit successfully
}
```


