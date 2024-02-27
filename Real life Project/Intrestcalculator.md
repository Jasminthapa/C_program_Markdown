+++
title = "Simple Interest Calculator in C"
weight = 1
description = "A basic C program to calculate simple interest. Input the principal amount, rate of interest, and time period to get the simple interest."
keywords = "C programming, simple interest, financial calculation, interest calculator"
+++
### To Find Simple Intrest

```c
#include <stdio.h>

int main() {
    float principal, rate, time;

    // Input principal amount, rate of interest, and time period
    printf("Enter the principal amount: ");
    scanf("%f", &principal);

    printf("Enter the rate of interest (per annum): ");
    scanf("%f", &rate);

    printf("Enter the time period (in years): ");
    scanf("%f", &time);

    // Calculate and display simple interest
    float simple_interest = (principal * rate * time) / 100;
    printf("\nSimple Interest: %.2f\n", simple_interest);

    return 0;
}
```