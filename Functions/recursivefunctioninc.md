+++ title = "Recursive Function in C" 
weight = 3 description = "Learn about recursive functions in C with examples. Explore factorial calculation, sum of n natural numbers, and reversing a number using recursion."
 keywords = "recursive function in C, factorial using recursion, sum of natural numbers using recursion, reverse a number using recursion." +++
 {{ %notice info %}}
 **Note**:
Recursive functions simplify code structure, enhance readability and reuse of code.
{{% /notice %}}


### Recursive Function
 It is a programming method in which function call itself.
Two important condition must be satisfied by
any recursive function and they are:
- Each time a function call itself, it must be
closer to the solution.
- There must be decision criteria for
stopping the process which is also called base
criteria.
### Example 1: Factorial of a Number Using Recursion
```c
#include <stdio.h>

long int fact(int n);

int main()

{

int n;

printf("Enter a positive number: ");

scanf("%ld", &n);

printf("Factorial of %d = %ld", n, fact(n));

return 0;

}

long int fact(int n)

{

if (n >= 1)

return n*fact(n-1);

else

return 1;

}
### **Example 2: Sum of n natural number using recursion**
```c
 #include <stdio.h>

int sum (int num);

int main()

{

int num, result;

printf("Enter the number: ");

scanf("%d", &num);

result = sum (num);

printf("Sum of %d natural number is %d\n", num, result);

return 0;

}

int sum (int num)

{

if (num != 0)

{

return (sum (num-1)+num);

}

else

{

return 0;

}

}
```
### Example: reverse a given number using recursive function

#include<stdio.h>

int revFunct(int num);

int main(){

int num,revNum;

printf("Enter any number: \n");

scanf("%d",&num);

revNum=revFunct(num);

printf("After reverse the number is :%d \n",revNum);

return 0;

}

int rev=0,rem;

revFunct(int num){

if(num){

rem=num%10;

rev=rev*10+rem;

revFunct(num/10);

}

else

return rev;
}