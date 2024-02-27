+++
title = "Delete File in C"
weight = 5
description = "In this section, you will learn how to  use delete file in C programming language. You will learn how to delete file in C using File class and remove() method."
keywords = "Delete file in C, Delete file in C programming, Delete file in C programming language"
+++
### Introduction
In this section,you can use the remove function from the stdio.h library to delete a file. If you try to delete a file that does not exist, then it will throw an exception.
### Delete File In C
Assume that you have a file named test.txt in the same directory of your dart program. Now, let’s delete it.
```c
#include <stdio.h>

int main() {
    // Specify the file path
    const char* filePath = "test.txt";

    // Use the remove function to delete the file
    if (remove(filePath) == 0) {
        printf("File deleted successfully.\n");
    } else {
        perror("Error deleting file");
    }

    return 0;
}
```
{{% notice info %}}**Note** perror used to print an error message if necessary.{{% /notice %}}
### Delete File If Exists
You can use fopen() method to check if a file exists or not. If it exists, then you can delete it.
```c
#include <stdio.h>

int main() {
    const char *filename = "test.txt";

    // Check if the file exists
    FILE *file = fopen(filename, "r");
    if (file != NULL) {
        fclose(file); // Close the file if it exists

        // Delete the file
        if (remove(filename) == 0) {
            printf("File deleted.\n");
        } else {
            printf("Unable to delete the file.\n");
        }
    } else {
        printf("File does not exist.\n");
    }

    return 0;
}
```
