+++
title = "Write File in C"
weight = 4
description = "In this section, you will learn how to write to a file in the C programming language. The C program demonstrates how to create a file named 'test.txt', write some initial content, and add new content to the existing file."
keywords = "write file in C, file handling in C, fprintf function in C, C programming language"
+++

### Introduction
In this section, you will learn how to write file in C programming language by using File class and  method.
### Write File In C
Let’s create a file named test.txt in the same directory of your C program and write some text in it.
```c
#include <stdio.h>

int main() {
    // Declare a FILE pointer
    FILE *file;

    // Open the file in write mode ("w")
    file = fopen("test.txt", "w");

    // Check if the file was successfully opened
    if (file == NULL) {
        printf("Unable to open the file.\n");
        return 1; // Exit with an error code
    }

    // Write to the file
    fprintf(file, "Welcome to test.txt file.\n");
    printf("File written.\n");

    // Close the file when done
    fclose(file);

    return 0; // Exit successfully
}
```
{{% notice info %}}
**Note**: If you have already some content in **test.txt** file, then it will be removed and replaced with new content.
{{% /notice %}}
### Add New Content To Previous Content 
You can use **fprintf** to add new content to previous content. Assume that **test.txt** file already contains some text.
```c
Welcome to test.txt file.
```
Now, let's add new content to it.
```c
#include <stdio.h>

int main() {
    // Declare a FILE pointer
    FILE *file;

    // Open the file in append mode ("a")
    file = fopen("test.txt", "a");

    // Check if the file was successfully opened
    if (file == NULL) {
        printf("Unable to open the file for appending.\n");
        return 1; // Exit with an error code
    }

    // Add new content to the file
    fprintf(file, "This is new content added to the file.\n");
    printf("New content added to the file.\n");

    // Close the file when done
    fclose(file);

    return 0; // Exit successfully
}
```


 