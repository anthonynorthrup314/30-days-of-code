# Day 0: Hello World

## Details

Challenge link: [https://www.hackerrank.com/challenges/30-hello-world](https://www.hackerrank.com/challenges/30-hello-world)

**Objective**

In this challenge, we review some basic concepts that will get you started with this series. You will need to use the same (or similar) syntax to read input and write output in challenges throughout HackerRank. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-hello-world/tutorial) tab for learning materials and an instructional video!

**Task**

To complete this challenge, you must save a line of input from stdin to a variable, print `Hello, World.` on a single line, and finally print the value of your variable on a second line.

You've got this!

**Note:** The instructions are Java-based, but we support submissions in many popular languages. You can switch languages using the drop-down menu above your editor, and the ***`inputString`*** variable may be written differently depending on the best-practice conventions of your submission language.

**Input Format**

A single line of text denoting ***`inputString`*** (the variable whose contents must be printed).

**Output Format**

Print `Hello, World.` on the first line, and the contents of ***`inputString`*** on the second line.

**Sample Input**

```plaintext
Welcome to 30 Days of Code!
```

**Sample Output**

```plaintext
Hello, World. 
Welcome to 30 Days of Code!
```

**Explanation**

On the first line, we print the string literal `Hello, World.`. On the second line, we print the contents of the ***`inputString`*** variable which, for this sample case, happens to be `Welcome to 30 Days of Code!`. If you do not print the variable's contents to stdout, you will not pass the hidden test case.

## Progress

- Completed:
    - [C](#c)
    - [C++](#c-1)
    - [C#](#c-2)
    - [Haskell](#haskell)
    - [Java 7](#java-7)
    - [Java 8](#java-8)
    - [Perl](#perl)
    - [PHP](#php)
    - [Python 2](#python-2)
    - [Python 3](#python-3)
    - [Ruby](#ruby)
- TODO:
    - Ada
    - BASH
    - C++14
    - Clojure: *Up next (HackerRank's ordering is strange)*
    - COBOL
    - CoffeeScript
    - Common Lisp (SBCL)
    - D
    - Elixir
    - Erlang
    - F#
    - Fortran
    - Go
    - Groovy
    - JavaScript (Node.js)
    - Julia
    - Kotlin
    - Lua
    - Objective-C
    - OCaml
    - Pascal
    - Pypy 2
    - Pypy 3
    - Racket
    - Rust
    - Scala
    - Swift
    - Tcl
    - VB.NET

## Solutions

### C

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
    // Declare a variable named 'input_string' to hold our input.
    char input_string[105]; 
    
    // Read a full line of input from stdin and save it to our variable, input_string.
    scanf("%[^\n]", input_string); 
    
    // Print a string literal saying "Hello, World." to stdout using printf.
    printf("Hello, World.\n");
    
    // Write a line of code here that prints the contents of input_string to stdout.
    printf("%s\n", input_string);
    
    return 0;
}
```

### C++

```c++
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main() {
    // Declare a variable named 'input_string' to hold our input.
    string input_string; 
    
    // Read a full line of input from stdin (cin) and save it to our variable, input_string.
    getline(cin, input_string); 
    
    // Print a string literal saying "Hello, World." to stdout using cout.
    cout << "Hello, World." << endl;

    // Write a line of code here that prints the contents of input_string to stdout.
    cout << input_string << endl;

    return 0;
}
```

### C#

```c#
using System;
using System.Collections.Generic;
using System.IO;

class Solution {
    static void Main(String[] args) {
        // Declare a variable named 'inputString' to hold our input.
        String inputString; 
        
        // Read a full line of input from stdin (cin) and save it to our variable, input_string.
        inputString = Console.ReadLine(); 
        
        // Print a string literal saying "Hello, World." to stdout using cout.
        Console.WriteLine("Hello, World.");
        
        // Write a line of code here that prints the contents of input_string to stdout.
        Console.WriteLine(inputString);
    }
}
```

### Haskell

```haskell
-- Enter your code here. Read input from STDIN. Print output to STDOUT
main = do
    inputString <- getLine
    putStrLn "Hello, World."
    putStrLn inputString
```

Reference: [http://learnyouahaskell.com/input-and-output](http://learnyouahaskell.com/input-and-output)

### Java 7

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
public class Solution {
    public static void main(String[] args) {
        // Create a Scanner object to read input from stdin.
        Scanner scan = new Scanner(System.in); 
        
        // Read a full line of input from stdin and save it to our variable, inputString.
        String inputString = scan.nextLine(); 

        // Close the scanner object, because we've finished reading 
        // all of the input from stdin needed for this challenge.
        scan.close(); 
      
        // Print a string literal saying "Hello, World." to stdout.
        System.out.println("Hello, World.");
      
        // Write a line of code here that prints the contents of inputString to stdout.
        System.out.println(inputString);
    }
}
```

### Java 8

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
public class Solution {
    public static void main(String[] args) {
        // Create a Scanner object to read input from stdin.
        Scanner scan = new Scanner(System.in); 
        
        // Read a full line of input from stdin and save it to our variable, inputString.
        String inputString = scan.nextLine(); 

        // Close the scanner object, because we've finished reading 
        // all of the input from stdin needed for this challenge.
        scan.close(); 
      
        // Print a string literal saying "Hello, World." to stdout.
        System.out.println("Hello, World.");
      
        // Write a line of code here that prints the contents of inputString to stdout.
        System.out.println(inputString);
    }
}
```

### Perl

```perl
my $inputString = <STDIN>; # get a line of input from stdin and save it to our variable

# Your first line of output goes here
print "Hello, World.\n";

# Write the second line of output
print "${inputString}\n";
```

Reference: [https://perlmaven.com/string-operators](https://perlmaven.com/string-operators)

### PHP

```php
<?php
$_fp = fopen("php://stdin", "r");

$inputString = fgets($_fp); // get a line of input from stdin and save it to our variable

// Your first line of output goes here
print("Hello, World.\n");

// Write the second line of output
print("{$inputString}\n");

fclose($_fp);
?>
```

Reference: [https://www.php.net/manual/en/language.operators.string.php](https://www.php.net/manual/en/language.operators.string.php)

### Python 2

```python
# Read a full line of input from stdin and save it to our dynamically typed variable, input_string.
inputString = raw_input()

# Print a string literal saying "Hello, World." to stdout.
print 'Hello, World.'

# Write a line of code here that prints the contents of input_string to stdout.
print inputString
```

### Python 3

```python
# Read a full line of input from stdin and save it to our dynamically typed variable, input_string.
input_string = input()

# Print a string literal saying "Hello, World." to stdout.
print('Hello, World.')

# Write a line of code here that prints the contents of input_string to stdout.
print(input_string)
```

### Ruby

```ruby
# Read a full line of input from stdin and save it to our dynamically typed variable, input_string.
input_string = gets

# Print a string literal saying "Hello, World." to stdout.
puts 'Hello, World.'

# Write a line of code here that prints the contents of input_string to stdout.
puts input_string
```
