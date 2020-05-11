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

- Completed: 8
    - [C](#c)
    - [C++](#c-1)
    - [C++14](#c14)
    - [C#](#c-2)
    - [Clojure](#clojure)
    - [Erlang](#erlang)
    - [Go](#go)
    - [Haskell](#haskell)
- TODO: 15 (order matches HackerRank)
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

### C++

```cpp
#include <bits/stdc++.h>

using namespace std;

// Complete the solve function below.
void solve(double meal_cost, int tip_percent, int tax_percent) {
    double tip = meal_cost * tip_percent / 100;
    double tax = meal_cost * tax_percent / 100;
    double totalCost = meal_cost + tip + tax;
    cout << round(totalCost) << endl;
}

int main()
{
    double meal_cost;
    cin >> meal_cost;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    int tip_percent;
    cin >> tip_percent;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    int tax_percent;
    cin >> tax_percent;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    solve(meal_cost, tip_percent, tax_percent);

    return 0;
}
```

Reference: [http://www.cplusplus.com/reference/cmath/round/](http://www.cplusplus.com/reference/cmath/round/)

### C++14

```cpp
#include <bits/stdc++.h>

using namespace std;

// Complete the solve function below.
void solve(double meal_cost, int tip_percent, int tax_percent) {
    double tip = meal_cost * tip_percent / 100;
    double tax = meal_cost * tax_percent / 100;
    double totalCost = meal_cost + tip + tax;
    cout << round(totalCost) << endl;
}

int main()
{
    double meal_cost;
    cin >> meal_cost;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    int tip_percent;
    cin >> tip_percent;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    int tax_percent;
    cin >> tax_percent;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    solve(meal_cost, tip_percent, tax_percent);

    return 0;
}
```

Reference: [http://www.cplusplus.com/reference/cmath/round/](http://www.cplusplus.com/reference/cmath/round/)

### C#

```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {

    // Complete the solve function below.
    static void solve(double meal_cost, int tip_percent, int tax_percent) {
        double tip = meal_cost * tip_percent / 100;
        double tax = meal_cost * tax_percent / 100;
        double total_cost = meal_cost + tip + tax;
        Console.WriteLine(Math.Round(total_cost));
    }

    static void Main(string[] args) {
        double meal_cost = Convert.ToDouble(Console.ReadLine());

        int tip_percent = Convert.ToInt32(Console.ReadLine());

        int tax_percent = Convert.ToInt32(Console.ReadLine());

        solve(meal_cost, tip_percent, tax_percent);
    }
}
```

Reference: [https://docs.microsoft.com/en-us/dotnet/api/system.math.round](https://docs.microsoft.com/en-us/dotnet/api/system.math.round)

### Clojure

```clojure
; Complete the solve function below.
(defn solve [meal_cost tip_percent tax_percent]
    (def tip (* meal_cost (/ tip_percent 100)))
    (def tax (* meal_cost (/ tax_percent 100)))
    (def total_cost (+ meal_cost tip tax))
    (println (Math/round total_cost))
)

(def meal_cost (Double/parseDouble (clojure.string/trim (read-line))))

(def tip_percent (Integer/parseInt (clojure.string/trim (read-line))))

(def tax_percent (Integer/parseInt (clojure.string/trim (read-line))))

(solve meal_cost tip_percent tax_percent)
```

References:

- Math operations:
    - `*`: [https://clojuredocs.org/clojure.core/*](https://clojuredocs.org/clojure.core/*)
    - `/`: [https://clojuredocs.org/clojure.core/_fs](https://clojuredocs.org/clojure.core/_fs)
    - `+`: [https://clojuredocs.org/clojure.core/+](https://clojuredocs.org/clojure.core/+)
- Rounding:
    - [https://clojure.org/reference/java_interop](https://clojure.org/reference/java_interop)
    - [https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#round-double-](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#round-double-)

### Erlang

```erlang
-module(solution).
-export([main/0]).

% Complete the solve function below.
solve(Meal_cost, Tip_percent, Tax_percent) ->
    Tip = Meal_cost * Tip_percent / 100,
    Tax = Meal_cost * Tax_percent / 100,
    Total_cost = Meal_cost + Tip + Tax,
    io:fwrite("~B~n", [round(Total_cost)]),
    ok.

main() ->
    {Meal_cost, _} = string:to_float(string:chomp(io:get_line(""))),

    {Tip_percent, _} = string:to_integer(string:chomp(io:get_line(""))),

    {Tax_percent, _} = string:to_integer(string:chomp(io:get_line(""))),

    solve(Meal_cost, Tip_percent, Tax_percent),

    ok.
```

Reference: [https://erlang.org/doc/man/erlang.html#round-1](https://erlang.org/doc/man/erlang.html#round-1)

### Go

```go
package main

import (
    "bufio"
    "fmt"
    "io"
    "os"
    "math"
    "strconv"
    "strings"
)

// Complete the solve function below.
func solve(meal_cost float64, tip_percent int32, tax_percent int32) {
    tip := meal_cost * float64(tip_percent) / 100.0
    tax := meal_cost * float64(tax_percent) / 100.0
    total_cost := meal_cost + tip + tax
    fmt.Println(math.Round(total_cost))
}

func main() {
    reader := bufio.NewReaderSize(os.Stdin, 1024 * 1024)

    meal_cost, err := strconv.ParseFloat(readLine(reader), 64)
    checkError(err)

    tip_percentTemp, err := strconv.ParseInt(readLine(reader), 10, 64)
    checkError(err)
    tip_percent := int32(tip_percentTemp)

    tax_percentTemp, err := strconv.ParseInt(readLine(reader), 10, 64)
    checkError(err)
    tax_percent := int32(tax_percentTemp)

    solve(meal_cost, tip_percent, tax_percent)
}

func readLine(reader *bufio.Reader) string {
    str, _, err := reader.ReadLine()
    if err == io.EOF {
        return ""
    }

    return strings.TrimRight(string(str), "\r\n")
}

func checkError(err error) {
    if err != nil {
        panic(err)
    }
}
```

References:

- [https://tour.golang.org/basics/13](https://tour.golang.org/basics/13)
- [https://golang.org/pkg/math/#Round](https://golang.org/pkg/math/#Round)

### Haskell

```haskell
{-# LANGUAGE FlexibleInstances, UndecidableInstances, DuplicateRecordFields #-}

module Main where

import Control.Monad
import Data.Array
import Data.Bits
import Data.List
import Data.List.Split
import Data.Set
import Debug.Trace
import System.Environment
import System.IO
import System.IO.Unsafe

-- Complete the solve function below.
solve meal_cost tip_percent tax_percent = do
    let tip = meal_cost * fromIntegral(tip_percent) / 100.0
        tax = meal_cost * fromIntegral(tax_percent) / 100.0
        total_cost = meal_cost + tip + tax
        in print (round total_cost)

main :: IO()
main = do
    meal_cost <- readLn :: IO Double

    tip_percent <- readLn :: IO Int

    tax_percent <- readLn :: IO Int

    solve meal_cost tip_percent tax_percent
```

References:

- [http://zvon.org/other/haskell/Outputsyntax/letQexpressions_reference.html](http://zvon.org/other/haskell/Outputsyntax/letQexpressions_reference.html)
- [https://www.haskell.org/tutorial/numbers.html](https://www.haskell.org/tutorial/numbers.html)
- [https://wiki.haskell.org/Converting_numbers#](https://wiki.haskell.org/Converting_numbers)
- [http://www.happylearnhaskelltutorial.com/1/output_other_things.html#s7.7](http://www.happylearnhaskelltutorial.com/1/output_other_things.html#s7.7)
