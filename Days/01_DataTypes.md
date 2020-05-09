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

- Completed: 3
    - [C](#c)
    - [Java 7](#java-7)
    - [Java 8](#java-8)
- TODO: 16
    - C#
    - C++ (Up next...)
    - C++14
    - Go
    - JavaScript (Node.js)
    - Julia
    - Perl
    - PHP
    - Pypy 2
    - Pypy 3
    - Python 2
    - Python 3
    - Ruby
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
