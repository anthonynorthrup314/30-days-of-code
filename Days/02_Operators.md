# Day 2: Operators

## Details

Challenge link: [https://www.hackerrank.com/challenges/30-operators](https://www.hackerrank.com/challenges/30-operators)

**Objective**

In this challenge, you'll work with arithmetic operators. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-operators/tutorial) tab for learning materials and an instructional video!

**Task**

Given the meal price (base cost of a meal), tip percent (the percentage of the meal price being added as tip), and tax percent (the percentage of the meal price being added as tax) for a meal, find and print the meal's total cost.

**Note:** Be sure to use precise values for your calculations, or you may end up with an incorrectly rounded result!

**Input Format**

There are ***`3`*** lines of numeric input:
The first line has a double, ***`mealCost`*** (the cost of the meal before tax and tip).
The second line has an integer, ***`tipPercent`*** (the percentage of ***`mealCost`*** being added as tip).
The third line has an integer, ***`taxPercent`*** (the percentage of ***`mealCost`*** being added as tax).

**Output Format**

Print the total meal cost, where ***`totalCost`*** is the rounded integer result of the entire bill (***`mealCost`*** with added tax and tip).

**Sample Input**

```plaintext
12.00
20
8
```

**Sample Output**

```plaintext
15
```

**Explanation**

Given:

***`mealCost = 12`***, ***`tipPercent = 20`***, ***`taxPercent = 8`***

Calculations:

***`tip = 12 * (20 / 100) = 2.4`***

***`tax = 12 * (8 / 100) = 0.96`***

***`totalCost = mealCost + tip + tax = 12 + 2.4 + 0.96 = 15.36`***

***`round(totalCost) = 15`***

We round ***`totalCost`*** to the nearest dollar (integer) and then print our result, ***`15`***.

## Progress

- Completed: 1
    - [C](#c)
- TODO: 22
    - C++
    - C++14
    - C#
    - Clojure (Up next...)
    - Erlang
    - Go
    - Haskell
    - Java 7
    - Java 8
    - JavaScript (Node.js)
    - Kotlin
    - Lua
    - Objective-C
    - Perl
    - PHP
    - Pypy 2
    - Pypy 3
    - Python 2
    - Python 3
    - Ruby
    - Scala
    - Swift

## Solutions

### C

```c
#include <assert.h>
#include <limits.h>
#include <math.h>
#include <stdbool.h>
#include <stddef.h>
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

char* readline();

// Complete the solve function below.
void solve(double meal_cost, int tip_percent, int tax_percent) {
    double tip = meal_cost * tip_percent / 100;
    double tax = meal_cost * tax_percent / 100;
    double totalCost = meal_cost + tip + tax;
    printf("%d\n", (int)round(totalCost));
}

int main()
{
    char* meal_cost_endptr;
    char* meal_cost_str = readline();
    double meal_cost = strtod(meal_cost_str, &meal_cost_endptr);

    if (meal_cost_endptr == meal_cost_str || *meal_cost_endptr != '\0') { exit(EXIT_FAILURE); }

    char* tip_percent_endptr;
    char* tip_percent_str = readline();
    int tip_percent = strtol(tip_percent_str, &tip_percent_endptr, 10);

    if (tip_percent_endptr == tip_percent_str || *tip_percent_endptr != '\0') { exit(EXIT_FAILURE); }

    char* tax_percent_endptr;
    char* tax_percent_str = readline();
    int tax_percent = strtol(tax_percent_str, &tax_percent_endptr, 10);

    if (tax_percent_endptr == tax_percent_str || *tax_percent_endptr != '\0') { exit(EXIT_FAILURE); }

    solve(meal_cost, tip_percent, tax_percent);

    return 0;
}

char* readline() {
    size_t alloc_length = 1024;
    size_t data_length = 0;
    char* data = malloc(alloc_length);

    while (true) {
        char* cursor = data + data_length;
        char* line = fgets(cursor, alloc_length - data_length, stdin);

        if (!line) { break; }

        data_length += strlen(cursor);

        if (data_length < alloc_length - 1 || data[data_length - 1] == '\n') { break; }

        size_t new_length = alloc_length << 1;
        data = realloc(data, new_length);

        if (!data) { break; }

        alloc_length = new_length;
    }

    if (data[data_length - 1] == '\n') {
        data[data_length - 1] = '\0';
    }

    data = realloc(data, data_length);

    return data;
}

```

Reference: [https://en.cppreference.com/w/c/numeric/math/round](https://en.cppreference.com/w/c/numeric/math/round)
