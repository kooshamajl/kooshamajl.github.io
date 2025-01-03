---
layout: page
title: Number Guessing Game
description: A fun game implemented in C where the player guesses a randomly chosen number.
tags: C, Game, Beginner
importance: 2
category: education
img: 
---

This game challenges players to guess a number randomly chosen by the computer. It's a simple yet engaging way to practice control structures and random number generation in C.


```C
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, guess, attempts = 0;
    srand(time(0)); // Seed for random number generation
    number = rand() % 100 + 1; // Random number between 1 and 100

    printf("Guess the number (between 1 and 100):\n");
    do {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess > number) {
            printf("Too high!\n");
        } else if (guess < number) {
            printf("Too low!\n");
        } else {
            printf("Congratulations! You guessed the number in %d attempts.\n", attempts);
        }
    } while (guess != number);

    return 0;
}
```