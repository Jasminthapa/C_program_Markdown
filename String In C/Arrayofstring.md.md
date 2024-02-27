+++
title = "Array of Strings in C"
weight = 2
description = "Learn how to use a 2D character array to store a list of strings in C."
keywords = "C programming, array of strings, 2D character array, string manipulation"
+++

### An Array Of String In C
An Array is the simplest Data Structure in C that stores homogeneous data in contiguous memory locations.So,2-D character can be used to store list of name's string.Eg:
```c
char name[5][30];
```
### Example 
```c
#include <stdio.h>
#include <string.h>

int main() {    
    char strings[][20] = {
        "Cow",
        "Buffalo",
        "Cat"
    };//string   
    for (i = 0; i < 3; ++i) {
        printf("String %d: %s\n", i + 1, strings[i]);
    }
    return 0;
}
```
### To read names of 5 person and display whose name start with a.
```c
#include <stdio.h>
#include <string.h>

int main() {
    char name[5][30];
    int i;

    printf("Enter any five names\n");

    for (i = 0; i < 5; i++) {
        gets(name[i]);
        strlwr(name[i]);
    }

    printf("Names are:\n");

    for (i = 0; i < 5; i++) {
        puts(name[i]);
    }

    printf("Names beginning with 'a' are:\n");

    for (i = 0; i < 5; i++) {
        if (name[i][0] == 'a') {
            printf("%s\n", name[i]);
        }
    }

    return 0;
}
```

