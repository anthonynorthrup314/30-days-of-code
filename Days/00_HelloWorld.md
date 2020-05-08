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
    - [BASH](#bash)
    - [C](#c)
    - [C++](#c-1)
    - [C#](#c-2)
    - [Clojure](#clojure)
    - Common Lisp (SBCL)
    - [D](#d)
    - [Erlang](#erlang)
    - [Go](#go)
    - [Groovy](#groovy)
    - [Haskell](#haskell)
    - [Java 7](#java-7)
    - [Java 8](#java-8)
    - JavaScript (Node.js)
    - [Lua](#lua)
    - [Objective-C](#objective-c)
    - [OCaml](#ocaml)
    - [Pascal](#pascal)
    - [Perl](#perl)
    - [PHP](#php)
    - [Python 2](#python-2)
    - [Python 3](#python-3)
    - [Ruby](#ruby)
    - [Scala](#scala)
- TODO:
    - Ada
    - C++14
    - COBOL (Up next...)
    - CoffeeScript
    - Elixir
    - F#
    - Fortran
    - Julia
    - Kotlin
    - Pypy 2
    - Pypy 3
    - Racket
    - Rust
    - Swift
    - Tcl
    - VB.NET

## Solutions

### BASH

```bash
read inputString # get a line of input from stdin and save it to our variable

# Your first line of output goes here
echo 'Hello, World.'

# Write the second line of output
echo $inputString
```

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

Reference: [https://www.tutorialspoint.com/c_standard_library/c_function_printf.htm](https://www.tutorialspoint.com/c_standard_library/c_function_printf.htm)

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

### Clojure

```clojure
; Enter your code here. Read input from STDIN. Print output to STDOUT
;
(def input-string (read-line))
(println "Hello, World.")
(println input-string)
```

Reference:

- [https://clojuredocs.org/clojure.core/println](https://clojuredocs.org/clojure.core/println)
- [https://clojuredocs.org/clojure.core/read-line](https://clojuredocs.org/clojure.core/read-line)

### Common Lisp (SBCL)

```lisp
;; Enter your code here. Read input from STDIN. Print output to STDOUT
(let ((input-string (read-line)))
    (write-line "Hello, World.")
    (write-line input-string)
    (force-output))
```

Reference: [http://www.sbcl.org/manual/](http://www.sbcl.org/manual/)

### D

```d
/* Enter your code here. Read input from STDIN. Print output to STDOUT */
import std.stdio;

void main()
{
    string input_string = readln();
    writeln("Hello, World.");
    writeln(input_string);
}
```

Reference: [https://dlang.org/phobos/std_stdio.html#.readln](https://dlang.org/phobos/std_stdio.html#.readln)

### Erlang

```erlang
% Enter your code here. Read input from STDIN. Print output to STDOUT
% Your class should be named solution

-module(solution).
-export([main/0]).

main() ->
    InputString = io:get_line(""),
    io:fwrite("Hello, World.~n"),
    io:fwrite("~s~n", [InputString]).

```

Reference:

- [https://erlang.org/doc/man/io.html#fwrite-1](https://erlang.org/doc/man/io.html#fwrite-1)
- [https://erlang.org/doc/man/io.html#get_line-1](https://erlang.org/doc/man/io.html#get_line-1)

### F#

```fsharp
//Enter your code here. Read input from STDIN. Print output to STDOUT
open System
let inputString = Console.ReadLine()
printfn "Hello, World."
printfn "%s" inputString
```

Reference: [https://www.tutorialspoint.com/fsharp/fsharp_basic_io.htm](https://www.tutorialspoint.com/fsharp/fsharp_basic_io.htm)

### Go

```go
package main
import (
    "bufio"
    "fmt"
    "os"
)

func main() {
    //Enter your code here. Read input from STDIN. Print output to STDOUT
    reader := bufio.NewReader(os.Stdin)
    input_string, _ := reader.ReadString('\n')
    fmt.Println("Hello, World.")
    fmt.Println(input_string)
}
```

Reference: [https://riptutorial.com/go/example/30034/read-input-from-console](https://riptutorial.com/go/example/30034/read-input-from-console)

### Groovy

```groovy
//Enter your code here. Read input from STDIN. Print output to STDOUT
def inputString = System.in.newReader().readLine()
println "Hello, World."
println inputString
```

Reference: [https://code-maven.com/groovy-read-from-stdin](https://code-maven.com/groovy-read-from-stdin)

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

### JavaScript (Node.js)

```js
function processData(inputString) {
    // This line of code prints the first line of output
    console.log("Hello, World.");
    
    // Write the second line of output that prints the contents of 'inputString' here.
    console.log(inputString);
}


process.stdin.resume();
process.stdin.setEncoding("ascii");
_input = "";
process.stdin.on("data", function (input) {
    _input += input;
});

process.stdin.on("end", function () {
   processData(_input);
});
```

### Lua

```lua
-- Enter your code here. Read input from STDIN. Print output to STDOUT
input_string = io.read("*line")
print("Hello, World.")
print(input_string)
```

Reference: [https://www.lua.org/pil/21.1.html](https://www.lua.org/pil/21.1.html)

### Objective-C

```objectivec
//Enter your code here. Read input from STDIN. Print output to STDOUT
int main() {
    @autoreleasepool {
        char input_string[105];
        scanf("%[^\n]", input_string);
        printf("Hello, World.\n");
        printf("%s\n", input_string);
        return 0;
    }
}
```

Note: This is the code from the [C](#c) solution above, but with a surrounding `@autoreleasepool{ }`. According to [https://www.hackerrank.com/environment/sample-problem/objc](https://www.hackerrank.com/environment/sample-problem/objc) we should avoid using NSLog, so there's no point in using NSString, or really, any actual Objective-C functionality.

### OCaml

```ocaml
(* Enter your code here. Read input from STDIN. Print output to STDOUT *)
let input_string = read_line ()
in
    let () = print_string "Hello, World." in
    let () = print_newline () in
    let () = print_string input_string in
        print_newline ();;
```

Reference: [https://caml.inria.fr/pub/docs/oreilly-book/html/book-ora027.html](https://caml.inria.fr/pub/docs/oreilly-book/html/book-ora027.html)

### Pascal

```pascal
(* Enter your code here. Read input from STDIN. Print output to STDOUT *)

Var InputString : String;

Begin
    ReadLn(InputString);
    WriteLn('Hello, World.');
    WriteLn(InputString);
End.
```

Reference:

- [https://www.freepascal.org/docs-html/rtl/system/readln.html](https://www.freepascal.org/docs-html/rtl/system/readln.html)
- [https://www.freepascal.org/docs-html/rtl/system/read.html](https://www.freepascal.org/docs-html/rtl/system/read.html)

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

### Scala

```scala
object Solution {
    def main(args: Array[String]) {
        // Print "Hello, World."
        println("Hello, World.")

        // Read a string variable
        val s = scala.io.StdIn.readLine()

        // Print the value of the string variable
        println(s)
    }
}
```
