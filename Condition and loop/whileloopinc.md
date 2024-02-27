+++ title = "While Loop in C" weight = 4 description = "Looping is repeating a specific set of commands until conditions are not completed. We have different types of loop in C." keywords = "Loops in C, for loop in C, for loop in C, while loop in C, do while loop in C" +++



### While loop
 In **while loop**, the loop’s body will run until and unless the condition is true. You must write conditions first before statements.So,it is entry control loop. This loop checks conditions on every iteration. If the condition is true, the code inside {} is executed, if the condition is false, then the loop stops.
 ```c
 while(condition){  
       //statement(s);  
      // Increment (++) or Decrement (--) Operation;  
}
```
- A while loop evaluates the condition inside the parenthesis ().
- If the condition is true, the code inside {} is executed.
- The condition is re-checked until the condition is false.
- When the condition is false, the loop stops.

### Example 1: To Print 1 To 10 Using While Loop
```c
#include <stdio.h>

int main() {
    int i = 1;
    while (i <= 10) {
        printf("%d\n", i);
        i++;
    }
    return 0;
}
```
{{% notice %}}**Note**: Do not forget to increase the variable used in the condition. Otherwise, the loop will never end and becomes an infinite loop.{{% /notice %}}

### Example 2
```c
#include <stdio.h>

int main() {
    int i = 1; // Initialization
    
    printf("Counting from 1 to 5 using a while loop:\n");
    while (i <= 5) { // Condition
        printf("%d\n", i);
        i++; // Increment
    }

    return 0;
}

```
### Example 3  Sum of n Natural Numbers Using While Loop.
```c
#include <stdio.h>

int main() {
    int n, sum = 0, i = 1;

    printf("Enter a positive integer n: ");
    scanf("%d", &n);

    while (i <= n) {
        sum += i; // displaying the sum of numbers from 1 to n
        i++; // Incrementing 
    }

    printf("The sum of first %d natural numbers = %d\n", n, sum);

    return 0;
}
```
### Example 4 To print Number from 50 to 100 Using While loop.
 #include <stdio.h>

int main() {
    int i = 50;
    
    while (i <= 100) {
        if (i % 2 == 0) {
            printf("%d\n", i);
        }
        i++;
    }

    return 0;
}


