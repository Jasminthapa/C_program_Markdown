+++ title = "User Input in C" weight = 8 description = "Instead of writing hard-coded values, you can use user input in C. It will make your program more dynamic. Learn to take a string, integer, or double user input." keywords = "user input C, how to take user input in C, C user input" +++


### User Input In C
Instead of writing hard-coded values, you can give input to the computer.It allows for  enabling customization, flexibility, and dynamic behavior. Programming language provide many built-in functions present in C header files.
Thr I/O functions that are used in C are:
1) scanf() and printf() functions
2) getschar() and putchar() functions
3) gets and puts

1) **scanf() and printf() functions**
- In C programming,scanf() and printf() functions are basic function .We can use them by using #include<stdio.h> directive.
**scanf()**  is used to get input from the user.Generally ,it is written as:
```c
scanf("%d",a);
```
**printf()** is used  to display message to user.Generally ,it is written as:
```c
printf("messaged to be display",variable1,variable2,...);
 Example :
 ```c
 #include <stdio.h>

int main() {
    // Declare variables to store user input
    int num;
    float floatingNumber;
    char character;
    //asked user enter an integer
    printf("Enter an integer: ");
    
    // Read integer input from the user and store it in the 'number' variable
    scanf("%d", &num);
    
    // ask user to enter a floating-point number
    printf("Enter a floating-point number: ");
    
    // Read floating-point input from the user and store it in the 'floatingNumber' variable
    scanf("%f", &floatingNumber);
    printf("You entered: \n");// to display it in proper way .
    printf("Integer: %d\n", num);
    printf("Floating-point number: %f\n", floatingNumber);
    return 0;
}
```
2) **getschar() and putchar() functions**

In C, getchar() and putchar() are functions used for character input and output, respectively.
- **getchar()** is a function in C that reads a single character and returns it as an integer representing the character's ASCII value.Syntax is given by:
```c 
int getchar(void);
```
example:
```c 
#include <stdio.h>

int main() {
    char c;
    
    printf("Enter a character: ");
    ch = getchar(); // Read a character from input
    
    printf("You entered: %c\n", ch);
    return 0;
}
```
**putchar()** is a function in C used to write a single character to the standard output.putchar() takes a single argument, character, which is an integer representing the character to be written.
Syntax is given as:
```c 
int putchar(int character);
```
```c
#include <stdio.h>

int main() {
    char c = 'D';

    printf("Using putchar(): ");
    putchar(c); 
    return 0;
}
```
{{% notice info %}} Note:It takes a single character as an argument and prints it to the console.{{% notice info %}}

3) **gets and puts**
In C programming,**gets()** and **puts()** are functions used for reading and writing strings to and from the standard input and output respectively.
```c
#include <stdio.h>
#define MAX_LENGTH 100 // Maximum length of the input string

int main() {
    char inputString[MAX_LENGTH];

    // Using gets() to read a string from the user
    printf("Enter a string: ");
    gets(inputString);

    // Using puts() to display the entered string
    printf("Entered string: ");
    puts(inputString);

    return 0;
}
```
Here,gets() reads a line of text.
- puts() prints a string .
### String User Input
They are used for storing textual user input. If you want to keep values like somebody’s name, address, description, etc., you can take string input from the user. One common method is using fgets() to read a line of text and store it into a character array.
Example:
```c
#include <stdio.h>
#define MAX_LENGTH 100 // Maximum length of the input string

int main() {
    char inputString[MAX_LENGTH];

    printf("Enter a string: ");
    fgets(inputString, sizeof(inputString), stdin);

    printf("Entered string: %s", inputString);

    return 0;
}
```
Here, 
- fgets() reads a line of text from the standard input and stores it in the inputString character array.
- sizeof(inputString) specifies the maximum number of characters that fgets() can read (to prevent buffer overflow).
- stdin is the standard input stream (the keyboard).
### Integer User Input

In C programming, you can take integer input from the user using the scanf() function.
```c 
#include <stdio.h>

int main() {
    int number;

    printf("Enter an integer: ");
    scanf("%d", &number);

    printf("Entered integer is : %d", number);

    return 0;
}
``` 
### Floating Point User Input
You can use float input if you want to get a numeric value from the user with the decimal point.E.g. 10.00, 10.5, -8.9 etc.
```c
#include <stdio.h>

int main() {
    double number;

    printf("Enter a floating number: ");
    scanf("%f", &number);

    printf("The entered number is %f\n", number);

    return 0;
}
```

{{% notice info %}}**Note**:&number is used to pass the address of the number variable to scanf() so that it can store the entered floating-point value in that memory location.
{{% /notice %}}



  
  


