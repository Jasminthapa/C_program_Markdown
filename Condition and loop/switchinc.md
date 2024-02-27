+++ title = "Switch Case in C" weight = 6 description = "Learn switch case in C. A Switch case is used to execute the code block based on the condition. The syntax of switch statements is cleaner and much easier to read and write." keywords = "switch case C, C switch case, switch case in C, string switch case C, switch case" +++

### Switch Case IN C

Switch statement allows a variable to be tested for equality against a list of value.Each value is a case,and the variable being switched on is checked for each switch case.A Switch case is used to execute the code block based on the condition
It is similar to if... else ladder.Only the difference is that it tests only for the true value.The switch case tests only for equality.
It's syntax is given by: 
```c
switch(expression) {
    case value1:
        // statements
        break;
    case value2:
        // statements
        break;
    case value3:
        // statements
        break;
    default:
       // default statements
}
```
### How does switch-case statement work in C
- The expression is evaluated once and compared with each case value.
- If expression matches with case value1, the statements of case value1 are executed. Similarly, case value 2 will be executed if the expression matches case value2. If the expression matches the case value3, the statements of case value3 are executed.
- The break keywords tell C to exit the switch statement because the statements in the case block are finished.
- If there is no match, default statements are executed.
### Replace If Else If With Switch In C
Here you can see the same program using if else if and switch in C.

### Example Using If Else If
This example prints the day name based on the numeric day of the week using a if else if.
```c
#include <stdio.h>

int main() {
    int day;

    printf("Enter a number  : ");
    scanf("%d", &day);

    if (day == 1) {
        printf("Monday\n");
    } else if (day == 2) {
        printf("Tuesday\n");
    } else if (day == 3) {
        printf("Wednesday\n");
    } else if (day == 4) {
        printf("Thursday\n");
    } else if (day == 5) {
        printf("Friday\n");
    } else if (day == 6) {
        printf("Saturday\n");
    } else if (day == 7) {
        printf("Sunday\n");
    } else {
        printf("Invalid input! Please enter a number between 1 and 7.\n");
    }

    return 0;
}
```
### Example 1
This is a program to find out the day of a week.
```c
#include <stdio.h>

int main() {
    int dayOfWeek = 5;

    switch (dayOfWeek) {
        case 1:
            printf("Day is Sunday.\n");
            break;
        case 2:
            printf("Day is Monday.\n");
            break;
        case 3:
            printf("Day is Tuesday.\n");
            break;
        case 4:
            printf("Day is Wednesday.\n");
            break;
        case 5:
            printf("Day is Thursday.\n");
            break;
        case 6:
            printf("Day is Friday.\n");
            break;
        case 7:
            printf("Day is Saturday.\n");
            break;
        default:
            printf("Invalid Weekday.\n");
    }

    return 0;
}
```
### Example 2  Switch  Case On Strings
This example prints the day name based on the numeric day of the week using a switch case.
```c
#include <stdio.h>

int main() {
    int day;

    printf("Enter a number : ");
    scanf("%d", &day);

    switch (day) {
        case 1:
            printf("Monday\n");
            break;
        case 2:
            printf("Tuesday\n");
            break;
        case 3:
            printf("Wednesday\n");
            break;
        case 4:
            printf("Thursday\n");
            break;
        case 5:
            printf("Friday\n");
            break;
        case 6:
            printf("Saturday\n");
            break;
        case 7:
            printf("Sunday\n");
            break;
        default:
            printf("Invalid input!.\n");
    }

    return 0;
}
```
### Example 3
This is a program determines the division of a student using switch case.
```c
#include <stdio.h>

int main() {
    int marks;

    printf("Enter the marks obtained by the student : ");
    scanf("%d", &marks);    
    int division = marks / 10;
    switch (division) {
        case 10:
        case 9:
            printf("Division: Distinction\n");
            break;
        case 8:
            printf("Division: First Class\n");
            break;
        case 7:
            printf("Division: Second Class\n");
            break;
        case 6:
            printf("Division: Pass Class\n");
            break;
        default:
            printf("Division: Fail\n");
    }

    return 0;
}
```