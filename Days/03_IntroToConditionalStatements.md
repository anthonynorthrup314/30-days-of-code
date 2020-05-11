# Day 3: Intro To Conditional Statements

## Details

Challenge link: [https://www.hackerrank.com/challenges/30-conditional-statements](https://www.hackerrank.com/challenges/30-conditional-statements)

**Objective**

In this challenge, we're getting started with conditional statements. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-conditional-statements/tutorial) tab for learning materials and an instructional video!

**Task**

Given an integer, ***`n`***, perform the following conditional actions:

- If ***`n`*** is odd, print `Weird`
- If ***`n`*** is even and in the inclusive range of ***`2`*** to ***`5`***, print `Not Weird`
- If ***`n`*** is even and in the inclusive range of ***`6`*** to ***`20`***, print `Weird`
- If ***`n`*** is even and greater than ***`20`***, print `Not Weird`

Complete the stub code provided in your editor to print whether or not  is weird.

**Input Format**

A single line containing a positive integer, ***`n`***.

**Constraints**

- ***`1 <= n <= 100`***

**Output Format**

Print `Weird` if the number is weird; otherwise, print `Not Weird`.

**Sample Input 0**

```plaintext
3
```

**Sample Output 0**

```plaintext
Weird
```

**Sample Input 1**

```plaintext
24
```

**Sample Output 1**

```plaintext
Not Weird
```

**Explanation**

Sample Case 0: ***`n = 3`***

***`n`*** is odd and odd numbers are weird, so we print `Weird`.

Sample Case 1: ***`n = 24`***

***`n > 20`*** and ***`n`*** is even, so it isn't weird. Thus, we print `Not Weird`.

## Progress

- Complete: 1
    - [Java 7](#java-7)
- TODO: 36
    - BASH
    - C
    - C++ (Up next...)
    - C++14
    - C#
    - Clojure
    - Common Lisp (SBCL)
    - D
    - Elixir
    - Erlang
    - F#
    - Fortran
    - Go
    - Groovy
    - Haskell
    - Java 8
    - JavaScript (Node.js)
    - Julia
    - Kotlin
    - Lua
    - Objective-C
    - OCaml
    - Octave
    - Pascal
    - Perl
    - PHP
    - Python 2
    - Python 3
    - R
    - Racket
    - Ruby
    - Rust
    - Scala
    - Swift
    - Tcl
    - VB.NET

## Solutions

### Java 7

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int N = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        if (N % 2 == 1 || (N >= 6 && N <= 20))
            System.out.println("Weird");
        else
            System.out.println("Not Weird");

        scanner.close();
    }
}
```

Reference: [https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op1.html](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op1.html)
