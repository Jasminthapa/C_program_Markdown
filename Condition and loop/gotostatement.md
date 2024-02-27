+++ title = "Goto statement in C" weight = 7 description = "Learn how to use goto in C." keywords = "goto in C, jumping satement." +++
### Goto Statement In C
The goto statement transfers control directly to the statement with the specified label.It's syntax is 
```c
label:
......
Statement;
.....
goto label;
```
{{% notice info %}}:
**Note**The goto loop is used when there is complex nested loops or conditions and need to exit from multiple levels at once due to an error or specific condition, goto might be used to jump to a common error-handling section.
{{% /notice %}}
### Example-1
Inside the if statement, the program prints the value of i, increments i, and then jumps back to loop_start using goto until i reaches 5.When i becomes 5, the condition in the if statement becomes false, and the program continues executing after the loop.
```c
#include <stdio.h>

int main() {
    int i = 0;

    loop_start:
    if (i < 10) {
        printf("%d ", i);
        i++;
        goto loop_start; // Jump back to loop_start
    }

    printf("\nLoop ended.\n");
    
    return 0;
}
```
### Example-2
```c
#include <stdio.h>

int main() {
    int number;

    printf("Enter a number between 1 and 5: ");
    scanf("%d", &number);

    switch (number) {
        case 1:
            printf("You entered number 1.\n");
            break;
        case 2:
            printf("You entered number 2.\n");
            break;
        case 3:
            printf("You entered number 3.\n");
            break;
        case 4:
            printf("You entered number 4.\n");
            break;
        case 5:
            printf("You entered number 5.\n");
            break;
        default:
            printf("Invalid number entered.\n");
            goto label;
    }    

label:
    printf("Program execution has ended.\n");

    return 0;
}
```
