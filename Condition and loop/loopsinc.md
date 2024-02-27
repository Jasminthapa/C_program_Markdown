+++
title = "Loops in C"
weight = 2
description = "Looping is repeating a specific set of commands until conditions are not completed. We have different types of loop in C."
keywords = "Loops in C, for loop in C, for loop in C, while loop in C, do while loop in C"
+++

### Loops In C
In Programming, loops are used to repeat a block of code until certain conditions are not completed. For, e.g., if you want to print your name 100 times, then rather than typing print("your name"); 100 times, you can use a loop.
There are different types of loop in Dart. They are:
- For loop
- While Loop
- Do While Loop

{{% /notice info %}} 
**Note**: The primary purpose of all loops is to repeat a block of code. 
{{% /notice %}}
### Print Your Name 10 Times Without Using Loop
```c
#include <stdio.h>

int main() {
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
    printf("John Doe\n");
}
```

### Example to Print your name using loop
 
```c
#include <stdio.h>

int main() {
	int i;
    for (i = 0; i < 10; i++) {
        printf("John Doe\n");
    }
    return 0;
}


```

{{% notice info %}}
 **Note**: Loops are helpful because they reduce errors, save time, and make code more readable.
  {{% /notice %}}

