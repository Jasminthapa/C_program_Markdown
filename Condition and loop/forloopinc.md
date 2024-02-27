+++ title = "For Loop in C" weight = 3 description = "Learn about for loop and how to use for loop in C" keywords = "for loop in C, C for loop, infinite loop in C" +++

### For Loop
For loop is a looping control statement structure that allows mention initial and final condition and the loop increment/decrement inside its expression.This is the most common type of loop. You can use for loop to run a code block multiple times according to the condition.
The syntax of for loop is:
```c
for(initialization; condition; increment/decrement){
            statements;
}
```
Here,
- Initialization is executed (one time) before the execution of the code block.
- Condition defines the condition for executing the code block.
- Increment/Decrement is executed (every time) after the code block has been executed.
```c
#include <stdio.h>

int main() {
    int num,i;
    unsigned long long factorial = 1;

    printf("Enter a positive integer: ");
    scanf("%d", &num);

    if (num <= 0) {
        printf("Error: Factorial is defined only for positive integers.\n");
    } else {
        for ( i = 1; i <= num; ++i) {
            factorial *= i;
        }

        printf("Factorial of %d = %llu\n", num, factorial);
    }

    return 0;
}
```
### Example-2
The following program is used to find the fibonacci Series. 
```c
#include <stdio.h>

int main() {
    int num, first = 0, second = 1, next,i=0;

    printf("Enter the number of terms in the Fibonacci series: ");
    scanf("%d", &num);

    printf("Fibonacci Series: ");

    for ( i = 0; i < num; ++i) {
        if (i <= 1)
            next = i;
        else {
            next = first + second;
            first = second;
            second = next;
        }
        printf("%d ", next);
    }

    printf("\n");
    return 0;
}
```
### Example 3  Displaying a countdown from 10 to 1
  ```c
  #include <stdio.h>

int main() {
    int i;
    printf("Countdown from 10 to 1:\n");
    for ( i = 10; i >= 1; --i) {
        printf("%d ", i);
    }
    printf("\n");
    return 0;
}
```
### Example- 4
- Printing a 1 using nested for loops
```c
#include <stdio.h>

int main() {
    int rows = 5;
    int i ; 
	int j;

    printf("Printing a pattern:\n");
    for ( i = 1; i <= rows; ++i) {
        for ( j = 1; j <= i; ++j) {
            printf("1 ");
        }
        printf("\n");
    }
    return 0;
}
```
