+++ title = "Conditions in C" weight = 1 description = "Use conditions to control the flow of the C program. Learn if condition, else condition, if else if condition,nested if etc." keywords = "control flow in C, conditions in C, if condition in C, if else in C,nested if, decision making in C" +++ 
### Conditions In C
When you write a computer program, you need to be able to tell the computer what to do in different situations. With conditions, you can control the flow of the dart program.In C programming, conditions are expressions that evaluate to true or false and are used to control the flow of a program . Conditions are fundamental in making decisions within a program, allowing certain blocks of code to execute based on whether the condition evaluates to true or false.Suppose you need to execute a specific code when a particular situation is true. In that case, you can use conditions in C. 
### Types Of Condition
Conditional in C are:
-  single if condition
- if.... else 
- else if ladder
- nested if.. else 
### single if condition
It is used to execute the code if condition is either true or false. If the condition is true,the program is executed.If condition is  false, the code block is skipped, and program execution continues after the if statement.
c
if (condition) {
    // Code to be executed if the condition is true
}

*Example:*
Here in this program  determine if a person can vote based on their age:
```c

#include <stdio.h>

int main() {
    int age;

    printf("Enter your age: ");
    scanf("%d", &age);

    if (age >= 18) {
        printf("You are eligible to vote!\n");
    } 

    return 0;
}
```
### If-Else Condition
It is used to execute true or false.If the result of the condition is true, then the body of the if-condition is executed. Otherwise, the body of the else-condition is executed.It execute two condition either true or false.
**Syntax**
```c
if(condition){
statements;
}else{
statements;
}
```
### Example-1
```c
#include <stdio.h>

int main() {
    int number;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (number > 0) {
        printf("The number is positive.\n");
    } else {
        printf("The number is negative.\n");
    }
    return 0;
}
```

### Example-2
Here,you can learn the person can vote or not using if else condition.
```c
#include <stdio.h>

int main() {
    int age;

    printf("Enter your age: ");
    scanf("%d", &age);

    if (age >= 18) {
        printf("You are eligible to vote.\n");
    } else {
        printf("You are not eligible to vote yet.\n");
    }

    return 0;
}
```

### If-Else-If Condition
When you have multiple if conditions, then you can use if-else-if. You can learn more in the example below. When you have more than two conditions, you can use if, else if, else in dart.
**Syntax**
```c
if(condition1){
statements1;
}else if(condition2){
statements2;
}else if(condition3){
statements3;
}
.....
.....
.....
else(conditionN){
statementsN;
}
```

### Example-1
```c
#include <stdio.h>

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    if (num > 0) {
        printf("The number is positive.\n");
    } else if (num < 0) {
        printf("The number is negative.\n");
    } else {
        printf("The number is zero.\n");
    }

    return 0;
}
```

### Example-2
```c
#include <stdio.h>

int main() {
    int noOfMonth = 5;

    // Check the number of the month
    if (noOfMonth == 1) {
        printf("The month is jan\n");
    } else if (noOfMonth == 2) {
        printf("The month is feb\n");
    } else if (noOfMonth == 3) {
        printf("The month is march\n");
    } else if (noOfMonth == 4) {
        printf("The month is april\n");
    } else if (noOfMonth == 5) {
        printf("The month is may\n");
    } else if (noOfMonth == 6) {
        printf("The month is june\n");
    } else if (noOfMonth == 7) {
        printf("The month is july\n");
    } else if (noOfMonth == 8) {
        printf("The month is aug\n");
    } else if (noOfMonth == 9) {
        printf("The month is sep\n");
    } else if (noOfMonth == 10) {
        printf("The month is oct\n");
    } else if (noOfMonth == 11) {
        printf("The month is nov\n");
    } else if (noOfMonth == 12) {
        printf("The month is dec\n");
    } else {
        printf("Invalid option given.\n");
    }

    return 0;
}
```

### Example-3 Find Greatest Number Among 3 Numbers
```c
#include <stdio.h>

int main() {
    int num1 = 1200;
    int num2 = 1000;
    int num3 = 150;

    if (num1 > num2 && num1 > num3) {
        printf("Num 1 is greater: i.e %d\n", num1);
    } else if (num2 > num1 && num2 > num3) {
        printf("Num 2 is greater: i.e %d\n", num2);
    } else if (num3 > num1 && num3 > num2) {
        printf("Num 3 is greater: i.e %d\n", num3);
    }

    return 0;
}
```

### nested if.. else
Simply,if a loop is inside another loop is called nested.Nested if-else statements in C involve having an if statement inside another if or else block.
```c
#include <stdio.h>

int main() {
    int num = 15;

    if (num >= 0) {
        if (num == 0) {
            printf("The number is zero.\n");
        } else {
            printf("The number is positive.\n");
        }
    } else {
        printf("The number is negative.\n");
    }

    return 0;
}
```
