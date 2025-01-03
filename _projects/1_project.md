---
layout: page
title: Simple Calculator
description: A basic calculator program implemented in C to perform addition, subtraction, multiplication, and division.
tags: C, Programming, Beginner
importance: 1
category: education
img: 
---

This project implements a simple calculator in C, allowing users to perform basic arithmetic operations. It demonstrates the use of control structures and user input handling in C.

```c
#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    switch (operator) {
        case '+': result = num1 + num2; break;
        case '-': result = num1 - num2; break;
        case '*': result = num1 * num2; break;
        case '/': result = num2 != 0 ? num1 / num2 : 0; break;
        default: printf("Invalid operator!\n"); return 1;
    }

    printf("Result: %.2lf\n", result);
    return 0;
}
```