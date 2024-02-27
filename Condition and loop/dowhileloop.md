+++ title = "Do While Loop in C" weight =5  description = "Looping is repeating a specific set of commands until conditions are not completed. Learn to use do while loop in C" keywords = "C do while loop, do while loop in C." ++

### Do While Loop
Do while loop is used to run a block of code multiple times. The loop’s body will be executed first, and then the condition is tested.It executes block of statements at least for once.
- It is an exit controlled loop.It checks the condition at the bottom of the loop.
The syntax of do while loop is:
```c
do{
    statement1;
    statement2;
    .
    .
    .
    statementN;
}
```
- First, it runs statements, and finally, the condition is checked.
- If the condition is true, the code inside {} is executed.
- The condition is re-checked until the condition is false.
- When the condition is false, the loop stops.
{{% /notice %}}In a do-while loop, the statements will be executed at least once time, even if the condition is false. It is because the statement is executed before checking the condition. {{% /notice %}}
### Example 1: To Print 1 To 10 Using Do While Loop
```c 
#include <stdio.h>

int main() {
    int i = 1;
    do {
        printf("%d\n", i);
        i++;
    } while (i <= 10);

    return 0;
}
```
### Example 2 To Print 1 To 10 Using Do While Loop
```c
#include <stdio.h>

int main() {
    int i = 1;
    do {
        printf("%d\n", i);
        i++;
    } while (i <= 10);

    return 0;
}
```
### Example 3: Display Sum of n Natural Numbers Using Do While Loop
```c
#include <stdio.h>

int main() {
    int total = 0;
    int n = 20; 
    int i = 1;

    do {
        total = total + i;
        i++;
    } while (i <= n);

    printf("Total is %d\n", total);

    return 0;
}
```


