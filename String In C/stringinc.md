+++
title = "String Handling in C"
weight = 1
description = "Learn about strings, string I/O statements, and commonly used string handling functions in C. Examples include strlen, strrev, strcat, strlwr, strupr, strcmp, and strcpy."
keywords = "C programming, strings, string handling functions, string I/O statements, strlen, strrev, strcat, strlwr, strupr, strcmp, strcpy"
+++


### Introduction
Strings are array of characters (i.e. character array  is known as string). A string is a sequence of characters that is treated as a single data item.

Syntax for declaring strings:
```c
char stringname [size];
```
```c
char name[20];
```
Initialization of string:
**Strings can be initialized as:**
```c
char name[] ['R', 'A', 'M', "0"], or, we equivalently can write as:
```
 we equivalently can write as:
 ```
 char[]="Ram"
 ```
### Example Program to enter a string from user and display it.
 ```c
 #include <stdio.h>

int main() {
    char n[20];

    printf("Enter any string from the keyboard\n");
    scanf("%s", n);

    printf("The entered string is: %s\n", n);
    return 0;
}
 ```
 ### String I/O statements
 The **gets()** and **puts()** are used for input and output of strings.
|  Operator Symbol   |  purpose  | syntax  |
| ----------- | ------------- | ------------- |
|  `gets`  |     stands for get string.It reads a string from keyboard.  |gets(variable name);  |
|  `puts`  |  For stands for put string.It displays a string on display.| puts(variable name or string data); |
### Example:Gets And Puts In String
```c
#include <stdio.h>

int main() {
    char n[20];

    printf("Enter any string from the keyboard\n");
   gets(n);

    printf("The entered string is: %s\n", n);
    puts(n);
    return 0;
}
```
### String Handling functions

String handling functions in C are a set of standard functions provided by the C Standard Library for manipulating strings.The string handling functions are defined in a header file called string.h. Whenever we want to use any string handling function we must include the header file called string.h.i.e.
```c
#include <string.h>
```
Few commonly used string handling functions are discussed below:

|  builtin functions   |  syntax  | Description  |
| ----------- | ------------- | ------------- |
|  `strlen()`  | strlen(string1)     |  returns total number of characters in string1 |
|  `strrev()`  | strrev(string1)    |It reverses the value of string1   |
|  `strcat()`  | strcat(string1,string2) |Appends string2 to string1  |
|  `strlwr`  |   strlwr(string1)  |  Converts all the characters of string1 to lower case.  |
|  `strupr`  |    strupr(string1) |  Converts all the characters of string1 to upper case |
|  `strcmp`  | strcmp(string1, string2)    |Returns 0 if string1 and string2 are the same,less than 0 if string1 <string2; greater than 0 if string1>string2  |
|  `strcpy`  |     strcpy(string1, string2) |Copies string2 value into string1  |

### Strlen()
It is used to returns the lenghth of given string.It excludes NULL character.
```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[] = "Hello, World!";
    size_t length = strlen(str);

    printf("Length of the string: %zu\n", length);

    return 0;
}
```
### strrev()
strrev() is a function in C used to reverse the characters in a string.
```c
#include <stdio.h>
#include <string.h>
 
int main()
{
    char str[50] = "thulotechnology";
 
    printf("The given string is =%s\n", str);
 
    printf("After reversing string is =%s", strrev(str));
 
    return 0;
}
```

### Strcpy()
It is used to copy the content of one string to another string.It takes two parameters copy string and source string.The data in the source is copied to destination.
```c
#include <stdio.h>
#include <string.h>

int main() {
    char source[] = "Hello";
    char destination[20];

    strcpy(destination, source);

    printf("Copied string: %s\n", destination);

    return 0;
}
```
### strcmp()
It  comapares two strings to find out wheather they are same or different. It returns 0 if string1 and string2 are the same,-1 if string1 <string2; 1 if string1>string2. 

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str1[] = "apple";
    char str2[] = "banana";

    int result = strcmp(str1, str2);

    printf("Comparison result: %d\n", result);

    return 0;
}
```
### strcat()
It concatenates two strings and returns the concatenated string.
#include <stdio.h>
#include <string.h>
int main()
{
     char s1[10] = "John";
     char s2[10] = "Doe";
     strcat(s1,s2);
     printf("Output string after concatenation: %s", s1);
     return 0;
}
### strupr()
The strupr( ) function is used to converts a given string to uppercase.It returns the modified string obtained after converting the characters of the given string str to uppercase.
```c
 #include<stdio.h>
#include<string.h> 
int main()
{
    char str[ ] = "thulo technology is the best";
    //converting the given string into uppercase.
    printf("%s\n", strupr (str));
    return 0;
}
```
### Strlwr()
The strupr( ) function is used to converts a given string to uppercase. 
```c
#include<stdio.h>
#include<string.h>
 
int main()
{
    char str[ ] = "Thulo Technology Is The Best";
    //converting the given string into uppercase.
    printf("%s\n", strlwr (str));
    return 0;
}
```






  





