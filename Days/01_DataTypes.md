# Day 1: Data Types

## Details

Challenge link: [https://www.hackerrank.com/challenges/30-data-types](https://www.hackerrank.com/challenges/30-data-types)

**Objective**

Today, we're discussing data types. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-data-types/tutorial) tab for learning materials and an instructional video!

**Task**

Complete the code in the editor below. The variables ***`i`***, ***`d`***, and ***`s`*** are already declared and initialized for you. You must:

1. Declare ***`3`*** variables: one of type int, one of type double, and one of type String.
1. Read ***`3`*** lines of input from stdin (according to the sequence given in the Input Format section below) and initialize your  variables.
1. Use the ***`+`*** operator to perform the following operations:
    1. Print the sum of ***`i`*** plus your int variable on a new line.
    1. Print the sum of ***`d`*** plus your double variable to a scale of one decimal place on a new line.
    1. Concatenate ***`s`*** with the string you read as input and print the result on a new line.

**Note:** If you are using a language that doesn't support using ***`+`*** for string concatenation (e.g.: C), you can just print one variable immediately following the other on the same line. The string provided in your editor must be printed first, immediately followed by the string you read as input.

**Input Format**

The first line contains an integer that you must sum with ***`i`***.
The second line contains a double that you must sum with ***`d`***.
The third line contains a string that you must concatenate with ***`s`***.

**Output Format**

Print the sum of both integers on the first line, the sum of both doubles (scaled to ***`1`*** decimal place) on the second line, and then the two concatenated strings on the third line.

**Sample Input**

```plaintext
12
4.0
is the best place to learn and practice coding!
```

**Sample Output**

```plaintext
16
8.0
HackerRank is the best place to learn and practice coding!
```

**Explanation**

When we sum the integers ***`4`*** and ***`12`***, we get the integer ***`16`***.
When we sum the floating-point numbers ***`4.0`*** and ***`4.0`***, we get ***`8.0`***.
When we concatenate HackerRank with `is the best place to learn and practice coding!`, we get `HackerRank is the best place to learn and practice coding!`.

**You will not pass this challenge if you attempt to assign the Sample Case values to your variables instead of following the instructions above and reading input from stdin.**

## Progress

- Completed: 19
    - [C](#c)
    - [C++](#c-1)
    - [C++14](#c-2)
    - [C#](#c-3)
    - [Go](#go)
    - [Java 7](#java-7)
    - [Java 8](#java-8)
    - [JavaScript (Node.js)](#javascript-nodejs)
    - [Julia](#julia)
    - [Perl](#perl)
    - [PHP](#php)
    - [Pypy 2](#pypy-2)
    - [Pypy 3](#pypy-3)
    - [Python 2](#python-2)
    - [Python 3](#python-3)
    - [Ruby](#ruby)
    - [Scala](#scala)
    - [Swift](#swift)
    - [VB.NET](#vbnet)

## Solutions

### C

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
    int i = 4;
    double d = 4.0;
    char s[] = "HackerRank ";

    
    // Declare second integer, double, and String variables.
    int i2;
    double d2;
    char s2[105];
    
    // Read and save an integer, double, and String to your variables.
    scanf("%d\n%lf\n%[^\n]", &i2, &d2, s2);
    
    // Print the sum of both integer variables on a new line.
    printf("%d\n", i + i2);
    
    // Print the sum of the double variables on a new line.
    printf("%.1lf\n", d + d2);
    
    // Concatenate and print the String variables on a new line
    // The 's' variable above should be printed first.
    printf("%s%s\n", s, s2);

    return 0;
}
```

References:

- [https://www.tutorialspoint.com/c_standard_library/c_function_scanf.htm](https://www.tutorialspoint.com/c_standard_library/c_function_scanf.htm)
- [https://www.tutorialspoint.com/c_standard_library/c_function_printf.htm](https://www.tutorialspoint.com/c_standard_library/c_function_printf.htm)

### C++

```cpp
#include <iostream>
#include <iomanip>
#include <limits>

using namespace std;

int main() {
    int i = 4;
    double d = 4.0;
    string s = "HackerRank ";

    
    // Declare second integer, double, and String variables.
    int i2;
    double d2;
    string s2;
    
    // Read and save an integer, double, and String to your variables.
    // Note: If you have trouble reading the entire string, please go back and review the Tutorial closely.
    cin >> i2 >> d2;
    cin.ignore();
    getline(cin, s2);
    
    // Print the sum of both integer variables on a new line.
    cout << (i + i2) << endl;
    
    // Print the sum of the double variables on a new line.
    cout << fixed << setprecision(1) << (d + d2) << endl;
    
    // Concatenate and print the String variables on a new line
    // The 's' variable above should be printed first.
    cout << s << s2 << endl;

    return 0;
}
```

References:

- [http://www.cplusplus.com/reference/istream/istream/operator%3E%3E/](http://www.cplusplus.com/reference/istream/istream/operator%3E%3E/)
- [http://www.cplusplus.com/reference/istream/istream/ignore/](http://www.cplusplus.com/reference/istream/istream/ignore/)
- [http://www.cplusplus.com/reference/iomanip/setprecision/](http://www.cplusplus.com/reference/iomanip/setprecision/)

### C++14

```cpp
#include <iostream>
#include <iomanip>
#include <limits>

using namespace std;

int main() {
    int i = 4;
    double d = 4.0;
    string s = "HackerRank ";

    
    // Declare second integer, double, and String variables.
    int i2;
    double d2;
    string s2;
    
    // Read and save an integer, double, and String to your variables.
    cin >> i2 >> d2;
    cin.ignore();
    getline(cin, s2);
    
    // Print the sum of both integer variables on a new line.
    cout << (i + i2) << endl;
    
    // Print the sum of the double variables on a new line.
    cout << fixed << setprecision(1) << (d + d2) << endl;
    
    // Concatenate and print the String variables on a new line
    // The 's' variable above should be printed first.
    cout << s << s2 << endl;

    return 0;
}
```

References:

- [http://www.cplusplus.com/reference/istream/istream/operator%3E%3E/](http://www.cplusplus.com/reference/istream/istream/operator%3E%3E/)
- [http://www.cplusplus.com/reference/istream/istream/ignore/](http://www.cplusplus.com/reference/istream/istream/ignore/)
- [http://www.cplusplus.com/reference/iomanip/setprecision/](http://www.cplusplus.com/reference/iomanip/setprecision/)

### C#

```csharp
using System;
using System.Collections.Generic;
using System.IO;

class Solution {
    static void Main(String[] args) {
        int i = 4;
        double d = 4.0;
        string s = "HackerRank ";

        
        // Declare second integer, double, and String variables.
        int i2;
        double d2;
        string s2;
        
        // Read and save an integer, double, and String to your variables.
        i2 = int.Parse(Console.ReadLine());
        d2 = double.Parse(Console.ReadLine());
        s2 = Console.ReadLine();
        
        // Print the sum of both integer variables on a new line.
        Console.WriteLine(i + i2);
        
        // Print the sum of the double variables on a new line.
        Console.WriteLine("{0:F1}", d + d2);
        
        // Concatenate and print the String variables on a new line
        // The 's' variable above should be printed first.
        Console.WriteLine(s + s2);
    }
}
```

References:

- [https://docs.microsoft.com/en-us/dotnet/api/system.int32.parse](https://docs.microsoft.com/en-us/dotnet/api/system.int32.parse)
- [https://docs.microsoft.com/en-us/dotnet/api/system.double.parse](https://docs.microsoft.com/en-us/dotnet/api/system.double.parse)
- [https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings)

### Go

```go
package main


import (
  "fmt"
  "os"
  "bufio"
  "strconv"
)

func main() {
  	var _ = strconv.Itoa // Ignore this comment. You can still use the package "strconv".
  
    var i uint64 = 4
    var d float64 = 4.0
    var s string = "HackerRank "

    scanner := bufio.NewScanner(os.Stdin)
    // Declare second integer, double, and String variables.
    var i2 uint64
    var d2 float64
    var s2 string
    
    // Read and save an integer, double, and String to your variables.
    if scanner.Scan() {
        i2, _ = strconv.ParseUint(scanner.Text(), 10, 64);
    }
    if scanner.Scan() {
        d2, _ = strconv.ParseFloat(scanner.Text(), 64);
    }
    if scanner.Scan() {
        s2 = scanner.Text();
    }
    
    // Print the sum of both integer variables on a new line.
    fmt.Println(i + i2);
    
    // Print the sum of the double variables on a new line.
    fmt.Printf("%.1f\n", d + d2);
    
    // Concatenate and print the String variables on a new line
    // The 's' variable above should be printed first.
    fmt.Println(s + s2);
}
```

References:

- [https://golang.org/pkg/bufio/#Scanner](https://golang.org/pkg/bufio/#Scanner)
- [https://golang.org/pkg/strconv/#ParseUint](https://golang.org/pkg/strconv/#ParseUint)
- [https://golang.org/pkg/strconv/#ParseFloat](https://golang.org/pkg/strconv/#ParseFloat)
- [https://golang.org/pkg/fmt/#Printf](https://golang.org/pkg/fmt/#Printf)
- [https://programming.guide/go/fmt-printf-reference-cheat-sheet.html](https://programming.guide/go/fmt-printf-reference-cheat-sheet.html)

### Java 7

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
	
    public static void main(String[] args) {
        int i = 4;
        double d = 4.0;
        String s = "HackerRank ";
		
        Scanner scan = new Scanner(System.in);

        /* Declare second integer, double, and String variables. */
        int i2;
        double d2;
        String s2;

        /* Read and save an integer, double, and String to your variables.*/
        // Note: If you have trouble reading the entire String, please go back and review the Tutorial closely.
        i2 = Integer.parseInt(scan.nextLine());
        d2 = Double.parseDouble(scan.nextLine());
        s2 = scan.nextLine();

        /* Print the sum of both integer variables on a new line. */
        System.out.println(i + i2);

        /* Print the sum of the double variables on a new line. */
        System.out.println(d + d2);
		
        /* Concatenate and print the String variables on a new line; 
        	the 's' variable above should be printed first. */
        System.out.println(s + s2);

        scan.close();
    }
}
```

References:

- [https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html#parseInt(java.lang.String)](https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html#parseInt(java.lang.String))
- [https://docs.oracle.com/javase/7/docs/api/java/lang/Double.html#parseDouble(java.lang.String)](https://docs.oracle.com/javase/7/docs/api/java/lang/Double.html#parseDouble(java.lang.String))

### Java 8

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
	
    public static void main(String[] args) {
        int i = 4;
        double d = 4.0;
        String s = "HackerRank ";
		
        Scanner scan = new Scanner(System.in);

        /* Declare second integer, double, and String variables. */
        int i2;
        double d2;
        String s2;

        /* Read and save an integer, double, and String to your variables.*/
        // Note: If you have trouble reading the entire String, please go back and review the Tutorial closely.
        i2 = Integer.parseInt(scan.nextLine());
        d2 = Double.parseDouble(scan.nextLine());
        s2 = scan.nextLine();
        
        /* Print the sum of both integer variables on a new line. */
        System.out.println(i + i2);

        /* Print the sum of the double variables on a new line. */
        System.out.println(d + d2);
		
        /* Concatenate and print the String variables on a new line; 
        	the 's' variable above should be printed first. */
        System.out.println(s + s2);

        scan.close();
    }
}
```

References:

- [https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html#parseInt-java.lang.String-](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html#parseInt-java.lang.String-)
- [https://docs.oracle.com/javase/8/docs/api/java/lang/Double.html#parseDouble-java.lang.String-](https://docs.oracle.com/javase/8/docs/api/java/lang/Double.html#parseDouble-java.lang.String-)


### JavaScript (Node.js)

```js
process.stdin.resume();
process.stdin.setEncoding('ascii');

var input_stdin = "";
var input_stdin_array = "";
var input_currentline = 0;

process.stdin.on('data', function (data) {
    input_stdin += data;
});

process.stdin.on('end', function () {
    input_stdin_array = input_stdin.split("\n");
    main();    
});

// Reads complete line from STDIN
function readLine() {
    return input_stdin_array[input_currentline++];
}

function main() {
    var i = 4
    var d = 4.0
    var s = "HackerRank "
    // Declare second integer, double, and String variables.
    var i2, d2, s2;

    // Read and save an integer, double, and String to your variables.
    i2 = parseInt(readLine());
    d2 = parseFloat(readLine());
    s2 = readLine();

    // Print the sum of both integer variables on a new line.
    console.log(i + i2);

    // Print the sum of the double variables on a new line.
    console.log((d + d2).toFixed(1));

    // Concatenate and print the String variables on a new line
    // The 's' variable above should be printed first.
    console.log(s + s2);
}
```

References:

- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt)
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseFloat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)

### Julia

```julia
i =  4
d = 4.0
s = "HackerRank"

# Declare second integer, double, and String variables.
    
# Read and save an integer, double, and String to your variables.
# Note: If you have trouble reading the entire string, please go back and review the Tutorial closely.
i2 = parse(Int, readline())
d2 = parse(Float32, readline())
s2 = readline()

# Print the sum of both integer variables on a new line.
println(i + i2)

# Print the sum of the double variables on a new line.
using Printf
@printf("%.1f\n", d + d2)

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
println(s, " ", s2)
```

References:

- [https://docs.julialang.org/en/v1/base/numbers/#Base.parse](https://docs.julialang.org/en/v1/base/numbers/#Base.parse)
- [https://docs.julialang.org/en/v1/manual/integers-and-floating-point-numbers/](https://docs.julialang.org/en/v1/manual/integers-and-floating-point-numbers/)
- [https://docs.julialang.org/en/v1/stdlib/Printf/](https://docs.julialang.org/en/v1/stdlib/Printf/)
    - *Note:* As mentioned in the link above, this uses `C`-style `printf` format string usage: [http://www.cplusplus.com/reference/cstdio/printf/](http://www.cplusplus.com/reference/cstdio/printf/)
- [https://docs.julialang.org/en/v1/manual/strings/#man-concatenation-1](https://docs.julialang.org/en/v1/manual/strings/#man-concatenation-1)

### Perl

```perl
$i = 4;
$d = 4.0;
$s = 'HackerRank ';
# Declare second integer, double, and String variables.

# Read and save an integer, double, and String to your variables.
$i2 = int <STDIN>;
$d2 = <STDIN>;
$s2 = <STDIN>;

# Print the sum of both integer variables on a new line.
printf "%d\n", ($i + $i2);

# Print the sum of the double variables on a new line.
printf "%.1f\n", ($d + $d2);

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
print ($s . $s2 . "\n");
```

References:

- [https://perldoc.perl.org/functions/int.html](https://perldoc.perl.org/functions/int.html)
- [https://www.geeksforgeeks.org/perl-automatic-string-to-number-conversion-or-casting/](https://www.geeksforgeeks.org/perl-automatic-string-to-number-conversion-or-casting/)
- [https://perldoc.perl.org/functions/printf.html](https://perldoc.perl.org/functions/printf.html)
    - *Note:* This uses the same formatting rules as `sprintf`: [https://perldoc.perl.org/functions/sprintf.html](https://perldoc.perl.org/functions/sprintf.html)

### PHP

```php
<?php
$handle = fopen ("php://stdin","r");
$i = 4;
$d = 4.0;
$s = "HackerRank ";
// Declare second integer, double, and String variables.

// Read and save an integer, double, and String to your variables.
$i2 = intval(fgets($handle));
$d2 = doubleval(fgets($handle));
$s2 = fgets($handle);

// Print the sum of both integer variables on a new line.
print(($i + $i2) . "\n");

// Print the sum of the double variables on a new line.
print(number_format($d + $d2, 1) . "\n");

// Concatenate and print the String variables on a new line
// The 's' variable above should be printed first.
print("{$s}{$s2}\n");

fclose($handle);
?>
```

References:

- [https://www.php.net/manual/en/function.intval.php](https://www.php.net/manual/en/function.intval.php)
- [https://www.php.net/manual/en/function.doubleval.php](https://www.php.net/manual/en/function.doubleval.php)
- [https://www.php.net/manual/en/function.number-format.php](https://www.php.net/manual/en/function.number-format.php)

### Pypy 2

```python
i = 4
d = 4.0
s = 'HackerRank '
# Declare second integer, double, and String variables.

# Read and save an integer, double, and String to your variables.
i2 = int(raw_input())
d2 = float(raw_input())
s2 = raw_input()

# Print the sum of both integer variables on a new line.
print (i + i2)

# Print the sum of the double variables on a new line.
print "{:.1f}".format(d + d2)

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
print (s + s2)
```

References:

- [https://docs.python.org/2.7/library/functions.html#int](https://docs.python.org/2.7/library/functions.html#int)
- [https://docs.python.org/2.7/library/functions.html#float](https://docs.python.org/2.7/library/functions.html#float)
- [https://docs.python.org/2.7/library/string.html#format-examples](https://docs.python.org/2.7/library/string.html#format-examples)

### Pypy 3

```python
i = 4
d = 4.0
s = 'HackerRank '
# Declare second integer, double, and String variables.

# Read and save an integer, double, and String to your variables.
i2 = int(input())
d2 = float(input())
s2 = input()

# Print the sum of both integer variables on a new line.
print(i + i2)

# Print the sum of the double variables on a new line.
print("{:.1f}".format(d + d2))

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
print(s + s2)
```

References:

- [https://docs.python.org/3/library/functions.html#int](https://docs.python.org/3/library/functions.html#int)
- [https://docs.python.org/3/library/functions.html#float](https://docs.python.org/3/library/functions.html#float)
- [https://docs.python.org/3/library/string.html#format-examples](https://docs.python.org/3/library/string.html#format-examples)

### Python 2

```python
i = 4
d = 4.0
s = 'HackerRank '
# Declare second integer, double, and String variables.

# Read and save an integer, double, and String to your variables.
i2 = int(raw_input())
d2 = float(raw_input())
s2 = raw_input()

# Print the sum of both integer variables on a new line.
print (i + i2)

# Print the sum of the double variables on a new line.
print "{:.1f}".format(d + d2)

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
print (s + s2)
```

References:

- [https://docs.python.org/2.7/library/functions.html#int](https://docs.python.org/2.7/library/functions.html#int)
- [https://docs.python.org/2.7/library/functions.html#float](https://docs.python.org/2.7/library/functions.html#float)
- [https://docs.python.org/2.7/library/string.html#format-examples](https://docs.python.org/2.7/library/string.html#format-examples)

### Python 3

```python
i = 4
d = 4.0
s = 'HackerRank '
# Declare second integer, double, and String variables.

# Read and save an integer, double, and String to your variables.
i2 = int(input())
d2 = float(input())
s2 = input()

# Print the sum of both integer variables on a new line.
print(i + i2)

# Print the sum of the double variables on a new line.
print("{:.1f}".format(d + d2))

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
print(s + s2)
```

References:

- [https://docs.python.org/3/library/functions.html#int](https://docs.python.org/3/library/functions.html#int)
- [https://docs.python.org/3/library/functions.html#float](https://docs.python.org/3/library/functions.html#float)
- [https://docs.python.org/3/library/string.html#format-examples](https://docs.python.org/3/library/string.html#format-examples)

### Ruby

```ruby
i = 4
d = 4.0
s = 'HackerRank '
# Declare second integer, double, and String variables.

# Read and save an integer, double, and String to your variables.
i2 = Integer(gets)
d2 = Float(gets)
s2 = gets

# Print the sum of both integer variables on a new line.
puts (i + i2)

# Print the sum of the double variables on a new line.
puts sprintf("%.1f", d + d2)

# Concatenate and print the String variables on a new line
# The 's' variable above should be printed first.
puts (s + s2)
```

References:

- [https://ruby-doc.org/core-2.5.0/Kernel.html#method-i-Integer](https://ruby-doc.org/core-2.5.0/Kernel.html#method-i-Integer)
- [https://ruby-doc.org/core-2.5.0/Kernel.html#method-i-Float](https://ruby-doc.org/core-2.5.0/Kernel.html#method-i-Float)
- [https://ruby-doc.org/core-2.5.0/Kernel.html#method-i-sprintf](https://ruby-doc.org/core-2.5.0/Kernel.html#method-i-sprintf)

### Scala

```scala
object Solution {
    def main(args: Array[String]) {
        val i = 4
        val d = 4.0
        val s = "HackerRank "

		// Read values of another integer, double, and string variables
        // Note use scala.io.StdIn to read from stdin
        val i2 = scala.io.StdIn.readLine().toInt
        val d2 = scala.io.StdIn.readLine().toDouble
        val s2 = scala.io.StdIn.readLine()
        
        // Print the sum of both the integer variables
        println(i + i2)
        
        // Print the sum of both the double variables
        println(d + d2)
        
        // Concatenate and print the string variables
        // The 's' variable above should be printed first.
        println(s + s2)
    }
}
```

References:

- [https://www.scala-lang.org/api/current/scala/collection/StringOps.html#toInt:Int](https://www.scala-lang.org/api/current/scala/collection/StringOps.html#toInt:Int)
- [https://www.scala-lang.org/api/current/scala/collection/StringOps.html#toDouble:Double](https://www.scala-lang.org/api/current/scala/collection/StringOps.html#toDouble:Double)

### Swift

```swift
var i = 4
var d = 4.0
var s = "HackerRank "
// Declare second integer, double, and String variables.

// Read and save an integer, double, and String to your variables.
var i2 = Int(readLine()!)!
var d2 = Double(readLine()!)!
var s2 = readLine()!

// Print the sum of both integer variables on a new line.
print(i + i2)

// Print the sum of the double variables on a new line.
print(d + d2)

// Concatenate and print the String variables on a new line
// The 's' variable above should be printed first.
print(s + s2)
```

References:

- [https://developer.apple.com/documentation/swift/int/2927504-init](https://developer.apple.com/documentation/swift/int/2927504-init)
- [https://developer.apple.com/documentation/swift/double/2926277-init](https://developer.apple.com/documentation/swift/double/2926277-init)

### VB.NET

```vbnet
Imports System

Module Solution
    
    Public Shared Sub Main()
        Dim i As Integer = 4
        Dim d As Decimal = 4.0
        Dim s As String = "HackerRank "
        'Declare second integer, double, and String variables.
        Dim i2 As Integer
        Dim d2 As Decimal
        Dim s2 As String
        
        'Read and save an integer, double, and String to your variables.
        i2 = Integer.Parse(Console.ReadLine())
        d2 = Decimal.Parse(Console.ReadLine())
        s2 = Console.ReadLine()
        
        'Print the sum of both integer variables on a new line.
        Console.WriteLine(i + i2)
        
        'Print the sum of the double variables on a new line.
        Console.WriteLine("{0:F1}", d + d2)
        
        'Concatenate and print the String variables on a new line
        'The 's' variable above should be printed first.
        Console.WriteLine(s + s2)
    End Sub
End Module
```

References:

- [https://docs.microsoft.com/en-us/dotnet/api/system.int32.parse](https://docs.microsoft.com/en-us/dotnet/api/system.int32.parse)
- [https://docs.microsoft.com/en-us/dotnet/api/system.decimal.parse](https://docs.microsoft.com/en-us/dotnet/api/system.decimal.parse)
- [https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings)
