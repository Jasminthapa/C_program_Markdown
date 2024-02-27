+++
title = "Simple Expense Tracker in C"
weight = 2
description = "Build a basic expense tracker in C to record and display your spending. Learn how to input expenses, calculate the total, and display an expense summary."
keywords = "C programming, expense tracker, budgeting, financial management"
+++
### Introduction
An expense tracker is a tool that helps you record and categorize your spending so you can see where your money is going. This can be helpful for budgeting, saving money, and reaching your financial goals.
```c
#include <stdio.h>
#include <stdlib.h>

#define MAX_EXPENSES 100

float readExpenses(float expenses[], int *count, float *total) {
    char choice;

    do {
        printf("Enter expense: $");
        scanf("%f", &expenses[*count]);
        *total += expenses[*count];
        (*count)++;

        printf("Add another expense? (y/n): ");
        scanf(" %c", &choice);
    } while (choice == 'y' && *count < MAX_EXPENSES);

    return *total;
}

void displayExpenses(float expenses[], int count, float total) {
    int i;

    if (count > 0) {
        printf("\nExpense Summary:\n");
        printf("%-10s%-10s\n", "Expense", "Amount");

        for (i = 0; i < count; i++) {
            printf("%-10d$%-10.2f\n", i + 1, expenses[i]);
        }

        printf("\nTotal: $%.2f\n", total);
    } else {
        printf("\nNo expenses to display.\n");
    }
}

int main() {
    float expenses[MAX_EXPENSES];
    int count = 0;
    float total = 0;

    total = readExpenses(expenses, &count, &total);
    displayExpenses(expenses, count, total);

    return 0;
}
```
