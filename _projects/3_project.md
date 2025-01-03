---
layout: page
title: Temperature Converter
description: A simple program to convert temperatures between Celsius and Fahrenheit.
tags: C, Beginner, Utility
importance: 3
category: education
img:
---

This project is a simple utility program implemented in C. It allows users to convert temperatures between Celsius and Fahrenheit using a text-based interface.

### Features:
- Converts Celsius to Fahrenheit.
- Converts Fahrenheit to Celsius.
- Interactive user-friendly interface.

### Code Snippet:
```c
#include <stdio.h>

void celsiusToFahrenheit() {
    double celsius;
    printf("Enter temperature in Celsius: ");
    scanf("%lf", &celsius);
    printf("Temperature in Fahrenheit: %.2lf\n", celsius * 9 / 5 + 32);
}

void fahrenheitToCelsius() {
    double fahrenheit;
    printf("Enter temperature in Fahrenheit: ");
    scanf("%lf", &fahrenheit);
    printf("Temperature in Celsius: %.2lf\n", (fahrenheit - 32) * 5 / 9);
}

int main() {
    int choice;
    printf("1. Celsius to Fahrenheit\n2. Fahrenheit to Celsius\nEnter your choice: ");
    scanf("%d", &choice);

    if (choice == 1) {
        celsiusToFahrenheit();
    } else if (choice == 2) {
        fahrenheitToCelsius();
    } else {
        printf("Invalid choice!\n");
    }

    return 0;
}
