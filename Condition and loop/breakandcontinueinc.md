+++ title = "Break and Continue in C" weight = 6 description = "Learn how to use break and continue in C." keywords = "break in C, continue in C, break and continue in C." +++

### C Break and Continue
In this tutorial, you will learn about the
 **break and continue** in C. While working on loops, we need to skip some elements or terminate the loop immediately without checking the condition. In such a situation, you can use the break and continue statement.

 ### Break Statement
 Sometimes you will need to break out of the loop immediately without checking the condition. You can do this using break statement.The break statement terminates the execution of an iterative statements before its completion.It stops the loop immediately, and the program's control moves outside the loop.
 ```c
 break;
 ```
 ### Example 1: Break In C For Loop
 ```c
 #include <stdio.h>
int main() 
{
int i;
    for ( i = 1; i <= 10; i++) {
        if (i == 6) {
            break; // Exit the loop when i equals to  6
        }
        printf("%d ", i);
    }
    printf("\nLoop exited due to 'break' statement.\n");
    return 0;
}
```
Here,Loop exited due to 'break' statement.
### Example-2 Negative For Loop
Here, the loop condition is true until the value of i is more than or equal to 1. However, the break says to go outside the loop when the value of i becomes 7.
```c
#include <stdio.h>

int main() {
    int i;
    for ( i = 10; i >= 1; i--) {
        if (i == 7) {
            break;
        }
        printf("%d ", i);
    }
    return 0;
}
```
### Example 3: Break In C While Loop
This C program utilizes a while loop that starts with i = 1 and continues as long as i is less than or equal to 10. Inside the loop, there's an if statement checking if i is equal to 7. If i reaches 7, the break statement is executed, causing an immediate exit from the loop
```c
#include <stdio.h>

int main() {
    int i = 1;
    while (i <= 10) {
        if (i == 7) {
            break;
        }
        printf("%d\n", i);
        i++;
    }

    return 0;
}
```
### Example 4: Break In Switch Case
    We already learn in C switch case, it is important to add break keyword in switch statement. This example prints the month name based on the number of the month using a switch case.

```c
#include <stdio.h>

int main() {
    int noOfMonth = 6;
    switch (noOfMonth) {
        case 1:
            printf("Selected month is January.\n");
            break;
        case 2:
            printf("Selected month is February.\n");
            break;
        case 3:
            printf("Selected month is March.\n");
            break;
        case 4:
            printf("Selected month is April.\n");
            break;
        case 5:
            printf("Selected month is May.\n");
            break;
        case 6:
            printf("Selected month is June.\n");
            break;
        case 7:
            printf("Selected month is July.\n");
            break;
        case 8:
            printf("Selected month is August.\n");
            break;
        case 9:
            printf("Selected month is September.\n");
            break;
        case 10:
            printf("Selected month is October.\n");
            break;
        case 11:
            printf("Selected month is November.\n");
            break;
        case 12:
            printf("Selected month is December.\n");
            break;
        default:
            printf("Invalid month.\n");
            break;
    }

    return 0;
}
```
### Continue Statement
Sometimes you will need to skip an iteration for a specific condition. You can do this utilizing continue statement.

The continue statement skips the current iteration of a loop. It will bypass the statement of the loop. It does not terminate the loop but rather continues with the next iteration. Here is the syntax of continue statement:
```c
continue;
```
### Example 1: Continue In C
```c
#include <stdio.h>


int main() {
	int i;
    for (i = 1; i <= 10; i++) {
        if (i == 5) {
            continue;
        }
        printf("%d\n", i);
    }

    return 0;
}
```
### Example 2: Continue In For Loop C
Here, the loop condition is true until the value of i is less than 10. However, the continue says to go to the next iteration of the loop when the value of i becomes 4.

```c
#include <stdio.h>
int main(){

int i = 0;

while (i < 10) {
  if (i == 4) {
    i++;
    continue;
  }
  printf("%d\n", i);
  i++;
}
}
```
### Break and continue In C

```c
#include <stdio.h>

int main() {
    // Example using break and continue in a loop
    printf("Example using break and continue in a loop:\n");
    
    // Loop from 1 to 10
    int i;
    for (i = 1; i <= 10; i++) {
        // If the number is 5, use continue to skip printing it
        if (i == 5) {
            printf("Skipping printing of number 5 using continue...\n");
            continue;
        }
        
        // If the number is 8, use break to exit the loop
        if (i == 8) {
            printf("Breaking out of the loop at number 8 using break...\n");
            break;
        }
        
        // Print the current number
        printf("%d\n", i);
    }

    return 0;
}

```


