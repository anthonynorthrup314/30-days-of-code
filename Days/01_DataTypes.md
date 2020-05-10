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

- Completed: 9
    - [C](#c)
    - [C++](#c-1)
    - [C#](#c-2)
    - [Java 7](#java-7)
    - [Java 8](#java-8)
    - [Perl](#perl)
    - [PHP](#php)
    - [Python 2](#python-2)
    - [Ruby](#ruby)
- TODO: 10
    - C++14
    - Go
    - JavaScript (Node.js) (Up next...)
    - Julia
    - Pypy 2
    - Pypy 3
    - Python 3
    - Scala
    - Swift
    - VB.NET

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

Reference:

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

Reference:

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

Reference:

- [https://docs.microsoft.com/en-us/dotnet/api/system.int32.parse](https://docs.microsoft.com/en-us/dotnet/api/system.int32.parse)
- [https://docs.microsoft.com/en-us/dotnet/api/system.double.parse](https://docs.microsoft.com/en-us/dotnet/api/system.double.parse)
- [https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings)

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

Reference:

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

Reference:

- [https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html#parseInt-java.lang.String-](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html#parseInt-java.lang.String-)
- [https://docs.oracle.com/javase/8/docs/api/java/lang/Double.html#parseDouble-java.lang.String-](https://docs.oracle.com/javase/8/docs/api/java/lang/Double.html#parseDouble-java.lang.String-)

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

Reference:

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

Reference:

- [https://www.php.net/manual/en/function.intval.php](https://www.php.net/manual/en/function.intval.php)
- [https://www.php.net/manual/en/function.doubleval.php](https://www.php.net/manual/en/function.doubleval.php)
- [https://www.php.net/manual/en/function.number-format.php](https://www.php.net/manual/en/function.number-format.php)

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

Reference:

- [https://docs.python.org/2.7/library/functions.html#int](https://docs.python.org/2.7/library/functions.html#int)
- [https://docs.python.org/2.7/library/functions.html#float](https://docs.python.org/2.7/library/functions.html#float)
- [https://docs.python.org/2.7/library/string.html#format-examples](https://docs.python.org/2.7/library/string.html#format-examples)

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
