
+++
title = "Open File in C"
weight = 3
description = "In this section, you will learn how to open a file in the C programming language using fopen(). You'll understand the general form of opening a file, various file opening modes, and a simple example demonstrating the file opening process in read mode."
keywords = "open file in C, file handling in C, fopen function in C, C programming language"
+++
### Introduction
In this section, you will learn how to open file in C programming language using fopen(). 
### General form of Opening a File.
```
FILE *pointer
Pointer=fopen("file name","mode")
```
### Example
Here's a simple C program that opens a file named "test.txt".
```c
#include <stdio.h>

int main() {
    // File pointer
    FILE *file;

    // Open the file in read mode ("r")
    file = fopen("test.txt", "r");

    // Check if the file is opened successfully
    if (file == NULL) {
        printf("Unable to open the file.\n");
        return 1;  // Return an error code
    } 

    // Close the file when done
    fclose(file);

    return 0; 
}
```
{{% notice info %}}Here r is used to open a file in read mode.You can even open file diffrent modes such as w,a,r+,w+ etcalso.{{% /notice %}}
### Diffrent File Opening Modes.
| Mode   | Meaning                                      | Details                                                                                       |
|--------|----------------------------------------------|-----------------------------------------------------------------------------------------------|
| `"r"`  | Read                                         | Opens the file for reading purpose.If file doesn't exist it returns NULL.                                                |
| `"w"`  | Write                                        | Opens the file for writing. If the file exists, it overwrites; if not, a new file is created.|
| `"a"`  | Append                                       | Opens the file for writing at the end. If the file does not exist, a new file is created.If file doesn't exist,a new file is created implicitly.     |
| `"r+"` | Read and Write                               | Opens the file for both reading and writing.                                |
| `"w+"` | Read and Write  | Opens the file for both reading and writing. If the file exists, it is truncated; if not, a new file is created.|
| `"a+"` |appends and read          | Opens the file for both reading and appending . Writing is done at the end.|
