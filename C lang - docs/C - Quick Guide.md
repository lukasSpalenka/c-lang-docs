---
created: 2023-01-12T14:34:10 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/cprogramming/c_quick_guide.htm
author: 
---

# C - Quick Guide

> ## Excerpt
> C - Quick Guide,  C is a general-purpose, high-level language that was originally developed by Dennis M. Ritchie to develop the UNIX operating system at Bell Labs. C was original

---
- [C - Quick Guide](#c---quick-guide)
  - [Facts about C](#facts-about-c)
  - [Why use C?](#why-use-c)
  - [C Programs](#c-programs)
  - [C - Environment Setup](#c---environment-setup)
  - [Local Environment Setup](#local-environment-setup)
  - [Text Editor](#text-editor)
  - [The C Compiler](#the-c-compiler)
  - [Installation on UNIX/Linux](#installation-on-unixlinux)
  - [Installation on Mac OS](#installation-on-mac-os)
  - [Installation on Windows](#installation-on-windows)
  - [C - Program Structure](#c---program-structure)
  - [Hello World Example](#hello-world-example)
  - [Compile and Execute C Program](#compile-and-execute-c-program)
  - [C - Basic Syntax](#c---basic-syntax)
  - [Tokens in C](#tokens-in-c)
  - [Semicolons](#semicolons)
  - [Comments](#comments)
  - [Identifiers](#identifiers)
  - [Keywords](#keywords)
  - [Whitespace in C](#whitespace-in-c)
  - [C - Data Types](#c---data-types)
  - [Integer Types](#integer-types)
  - [Floating-Point Types](#floating-point-types)
  - [The void Type](#the-void-type)
  - [C - Variables](#c---variables)
  - [Variable Definition in C](#variable-definition-in-c)
  - [Variable Declaration in C](#variable-declaration-in-c)
    - [Example](#example)
  - [Lvalues and Rvalues in C](#lvalues-and-rvalues-in-c)
  - [C - Constants and Literals](#c---constants-and-literals)
  - [Integer Literals](#integer-literals)
  - [Floating-point Literals](#floating-point-literals)
  - [Character Constants](#character-constants)
  - [String Literals](#string-literals)
  - [Defining Constants](#defining-constants)
  - [The #define Preprocessor](#the-define-preprocessor)
  - [The const Keyword](#the-const-keyword)
  - [C - Storage Classes](#c---storage-classes)
  - [The auto Storage Class](#the-auto-storage-class)
  - [The register Storage Class](#the-register-storage-class)
  - [The static Storage Class](#the-static-storage-class)
  - [The extern Storage Class](#the-extern-storage-class)
  - [C - Operators](#c---operators)
  - [Arithmetic Operators](#arithmetic-operators)
  - [Relational Operators](#relational-operators)
  - [Logical Operators](#logical-operators)

---

C is a general-purpose, high-level language that was originally developed by Dennis M. Ritchie to develop the UNIX operating system at Bell Labs. C was originally first implemented on the DEC PDP-11 computer in 1972.

In 1978, Brian Kernighan and Dennis Ritchie produced the first publicly available description of C, now known as the K&R standard.

The UNIX operating system, the C compiler, and essentially all UNIX application programs have been written in C. C has now become a widely used professional language for various reasons −

-   Easy to learn
-   Structured language
-   It produces efficient programs
-   It can handle low-level activities
-   It can be compiled on a variety of computer platforms

## Facts about C

-   C was invented to write an operating system called UNIX.
    
-   C is a successor of B language which was introduced around the early 1970s.
    
-   The language was formalized in 1988 by the American National Standard Institute (ANSI).
    
-   The UNIX OS was totally written in C.
    
-   Today C is the most widely used and popular System Programming Language.
    
-   Most of the state-of-the-art software have been implemented using C.
    
-   Today's most popular Linux OS and RDBMS MySQL have been written in C.
    

## Why use C?

C was initially used for system development work, particularly the programs that make-up the operating system. C was adopted as a system development language because it produces code that runs nearly as fast as the code written in assembly language. Some examples of the use of C might be −

-   Operating Systems
-   Language Compilers
-   Assemblers
-   Text Editors
-   Print Spoolers
-   Network Drivers
-   Modern Programs
-   Databases
-   Language Interpreters
-   Utilities

## C Programs

A C program can vary from 3 lines to millions of lines and it should be written into one or more text files with extension **".c"**; for example, _hello.c_. You can use **"vi"**, **"vim"** or any other text editor to write your C program into a file.

This tutorial assumes that you know how to edit a text file and how to write source code inside a program file.

## C - Environment Setup

## Local Environment Setup

If you want to set up your environment for C programming language, you need the following two software tools available on your computer, (a) Text Editor and (b) The C Compiler.

## Text Editor

This will be used to type your program. Examples of few a editors include Windows Notepad, OS Edit command, Brief, Epsilon, EMACS, and vim or vi.

The name and version of text editors can vary on different operating systems. For example, Notepad will be used on Windows, and vim or vi can be used on windows as well as on Linux or UNIX.

The files you create with your editor are called the source files and they contain the program source codes. The source files for C programs are typically named with the extension "**.c**".

Before starting your programming, make sure you have one text editor in place and you have enough experience to write a computer program, save it in a file, compile it and finally execute it.

## The C Compiler

The source code written in source file is the human readable source for your program. It needs to be "compiled", into machine language so that your CPU can actually execute the program as per the instructions given.

The compiler compiles the source codes into final executable programs. The most frequently used and free available compiler is the GNU C/C++ compiler, otherwise you can have compilers either from HP or Solaris if you have the respective operating systems.

The following section explains how to install GNU C/C++ compiler on various OS. We keep mentioning C/C++ together because GNU gcc compiler works for both C and C++ programming languages.

## Installation on UNIX/Linux

If you are using **Linux or UNIX**, then check whether GCC is installed on your system by entering the following command from the command line −

```c
$ gcc -v

```

If you have GNU compiler installed on your machine, then it should print a message as follows −

```c
Using built-in specs.
Target: i386-redhat-linux
Configured with: ../configure --prefix=/usr .......
Thread model: posix
gcc version 4.1.2 20080704 (Red Hat 4.1.2-46)

```

If GCC is not installed, then you will have to install it yourself using the detailed instructions available at [https://gcc.gnu.org/install/](https://gcc.gnu.org/install/)

This tutorial has been written based on Linux and all the given examples have been compiled on the Cent OS flavor of the Linux system.

## Installation on Mac OS

If you use Mac OS X, the easiest way to obtain GCC is to download the Xcode development environment from Apple's web site and follow the simple installation instructions. Once you have Xcode setup, you will be able to use GNU compiler for C/C++.

Xcode is currently available at [developer.apple.com/technologies/tools/](https://developer.apple.com/technologies/tools/).

## Installation on Windows

To install GCC on Windows, you need to install MinGW. To install MinGW, go to the MinGW homepage, [www.mingw.org](https://www.mingw-w64.org/downloads/), and follow the link to the MinGW download page. Download the latest version of the MinGW installation program, which should be named MinGW-<version>.exe.

While installing Min GW, at a minimum, you must install gcc-core, gcc-g++, binutils, and the MinGW runtime, but you may wish to install more.

Add the bin subdirectory of your MinGW installation to your **PATH** environment variable, so that you can specify these tools on the command line by their simple names.

After the installation is complete, you will be able to run gcc, g++, ar, ranlib, dlltool, and several other GNU tools from the Windows command line.

## C - Program Structure

Before we study the basic building blocks of the C programming language, let us look at a bare minimum C program structure so that we can take it as a reference in the upcoming chapters.

## Hello World Example

A C program basically consists of the following parts −

-   Preprocessor Commands
-   Functions
-   Variables
-   Statements & Expressions
-   Comments

Let us look at a simple code that would print the words "Hello World" −

```c
#include <stdio.h>

int main() {
   /* my first program in C */
   printf("Hello, World! \n");
   
   return 0;
}
```

Let us take a look at the various parts of the above program −

-   The first line of the program _#include <stdio.h>_ is a preprocessor command, which tells a C compiler to include stdio.h file before going to actual compilation.
    
-   The next line _int main()_ is the main function where the program execution begins.
    
-   The next line /\*...\*/ will be ignored by the compiler and it has been put to add additional comments in the program. So such lines are called comments in the program.
    
-   The next line _printf(...)_ is another function available in C which causes the message "Hello, World!" to be displayed on the screen.
    
-   The next line **return 0;** terminates the main() function and returns the value 0.
    

## Compile and Execute C Program

Let us see how to save the source code in a file, and how to compile and run it. Following are the simple steps −

-   Open a text editor and add the above-mentioned code.
    
-   Save the file as _hello.c_
    
-   Open a command prompt and go to the directory where you have saved the file.
    
-   Type _gcc hello.c_ and press enter to compile your code.
    
-   If there are no errors in your code, the command prompt will take you to the next line and would generate _a.out_ executable file.
    
-   Now, type _a.out_ to execute your program.
    
-   You will see the output _"Hello World"_ printed on the screen.
    

```c
$ gcc hello.c
$ ./a.out
Hello, World!

```

Make sure the gcc compiler is in your path and that you are running it in the directory containing the source file hello.c.

## C - Basic Syntax

You have seen the basic structure of a C program, so it will be easy to understand other basic building blocks of the C programming language.

## Tokens in C

A C program consists of various tokens and a token is either a keyword, an identifier, a constant, a string literal, or a symbol. For example, the following C statement consists of five tokens −

```c
printf("Hello, World! \n");
```

The individual tokens are −

```c
printf
(
   "Hello, World! \n"
)
;
```

## Semicolons

In a C program, the semicolon is a statement terminator. That is, each individual statement must be ended with a semicolon. It indicates the end of one logical entity.

Given below are two different statements −

```c
printf("Hello, World! \n");
return 0;
```

## Comments

Comments are like helping text in your C program and they are ignored by the compiler. They start with /\* and terminate with the characters \*/ as shown below −

```c
/* my first program in C */

```

You cannot have comments within comments and they do not occur within a string or character literals.

## Identifiers

A C identifier is a name used to identify a variable, function, or any other user-defined item. An identifier starts with a letter A to Z, a to z, or an underscore '\_' followed by zero or more letters, underscores, and digits (0 to 9).

C does not allow punctuation characters such as @, $, and % within identifiers. C is a **case-sensitive** programming language. Thus, _Manpower_ and _manpower_ are two different identifiers in C. Here are some examples of acceptable identifiers −

```c
mohd       zara    abc   move_name  a_123
myname50   _temp   j     a23b9      retVal

```

## Keywords

The following list shows the reserved words in C. These reserved words may not be used as constants or variables or any other identifier names.

<table><tbody><tr><td>auto</td><td>else</td><td>long</td><td>switch</td></tr><tr><td>break</td><td>enum</td><td>register</td><td>typedef</td></tr><tr><td>case</td><td>extern</td><td>return</td><td>union</td></tr><tr><td>char</td><td>float</td><td>short</td><td>unsigned</td></tr><tr><td>const</td><td>for</td><td>signed</td><td>void</td></tr><tr><td>continue</td><td>goto</td><td>sizeof</td><td>volatile</td></tr><tr><td>default</td><td>if</td><td>static</td><td>while</td></tr><tr><td>do</td><td>int</td><td>struct</td><td>_Packed</td></tr><tr><td>double</td><td></td><td></td><td></td></tr></tbody></table>

## Whitespace in C

A line containing only whitespace, possibly with a comment, is known as a blank line, and a C compiler totally ignores it.

Whitespace is the term used in C to describe blanks, tabs, newline characters and comments. Whitespace separates one part of a statement from another and enables the compiler to identify where one element in a statement, such as int, ends and the next element begins. Therefore, in the following statement −

```c
int age;
```

there must be at least one whitespace character (usually a space) between int and age for the compiler to be able to distinguish them. On the other hand, in the following statement −

```c
fruit = apples + oranges;   // get the total fruit
```

no whitespace characters are necessary between fruit and =, or between = and apples, although you are free to include some if you wish to increase readability.

## C - Data Types

Data types in c refer to an extensive system used for declaring variables or functions of different types. The type of a variable determines how much space it occupies in storage and how the bit pattern stored is interpreted.

The types in C can be classified as follows −

| Sr.No. | Types & Description |
| ------ | ------------------- |
| 1      | **Basic Types**<br>They are arithmetic types and are further classified into: (a) integer types and (b) floating-point types.<br> |
| 2 | <br>**Enumerated types**<br>They are again arithmetic types and they are used to define variables that can only assign certain discrete integer values throughout the program.<br> |
| 3 | <br>**The type void**<br>The type specifier _void_ indicates that no value is available.<br> |
| 4 | <br>**Derived types**<br>They include (a) Pointer types, (b) Array types, (c) Structure types, (d) Union types and (e) Function types.<br> |

The array types and structure types are referred collectively as the aggregate types. The type of a function specifies the type of the function's return value. We will see the basic types in the following section, where as other types will be covered in the upcoming chapters.

## Integer Types

The following table provides the details of standard integer types with their storage sizes and value ranges −

| Type           | Storage size | Value range                                           |
| -------------- | ------------ | ----------------------------------------------------- |
| char           | 1 byte       | \-128 to 127 or 0 to 255                              |
| unsigned char  | 1 byte       | 0 to 255                                              |
| signed char    | 1 byte       | \-128 to 127                                          |
| int            | 2 or 4 bytes | \-32,768 to 32,767 or -2,147,483,648 to 2,147,483,647 |
| unsigned int   | 2 or 4 bytes | 0 to 65,535 or 0 to 4,294,967,295                     |
| short          | 2 bytes      | \-32,768 to 32,767                                    |
| unsigned short | 2 bytes      | 0 to 65,535                                           |
| long           | 8 bytes      | \-9223372036854775808 to 9223372036854775807          |
| unsigned long  | 8 bytes      | 0 to 18446744073709551615                             |

To get the exact size of a type or a variable on a particular platform, you can use the **sizeof** operator. The expressions _sizeof(type)_ yields the storage size of the object or type in bytes. Given below is an example to get the size of various type on a machine using different constant defined in limits.h header file −

```c
#include <stdio.h>
#include <stdlib.h>
#include <limits.h>
#include <float.h>

int main(int argc, char** argv) {

    printf("CHAR_BIT    :   %d\n", CHAR_BIT);
    printf("CHAR_MAX    :   %d\n", CHAR_MAX);
    printf("CHAR_MIN    :   %d\n", CHAR_MIN);
    printf("INT_MAX     :   %d\n", INT_MAX);
    printf("INT_MIN     :   %d\n", INT_MIN);
    printf("LONG_MAX    :   %ld\n", (long) LONG_MAX);
    printf("LONG_MIN    :   %ld\n", (long) LONG_MIN);
    printf("SCHAR_MAX   :   %d\n", SCHAR_MAX);
    printf("SCHAR_MIN   :   %d\n", SCHAR_MIN);
    printf("SHRT_MAX    :   %d\n", SHRT_MAX);
    printf("SHRT_MIN    :   %d\n", SHRT_MIN);
    printf("UCHAR_MAX   :   %d\n", UCHAR_MAX);
    printf("UINT_MAX    :   %u\n", (unsigned int) UINT_MAX);
    printf("ULONG_MAX   :   %lu\n", (unsigned long) ULONG_MAX);
    printf("USHRT_MAX   :   %d\n", (unsigned short) USHRT_MAX);

    return 0;
}
```

When you compile and execute the above program, it produces the following result on Linux −

```c
CHAR_BIT    :   8
CHAR_MAX    :   127
CHAR_MIN    :   -128
INT_MAX     :   2147483647
INT_MIN     :   -2147483648
LONG_MAX    :   9223372036854775807
LONG_MIN    :   -9223372036854775808
SCHAR_MAX   :   127
SCHAR_MIN   :   -128
SHRT_MAX    :   32767
SHRT_MIN    :   -32768
UCHAR_MAX   :   255
UINT_MAX    :   4294967295
ULONG_MAX   :   18446744073709551615
USHRT_MAX   :   65535

```

## Floating-Point Types

The following table provide the details of standard floating-point types with storage sizes and value ranges and their precision −

| Type        | Storage size | Value range            | Precision         |
| ----------- | ------------ | ---------------------- | ----------------- |
| float       | 4 byte       | 1.2E-38 to 3.4E+38     | 6 decimal places  |
| double      | 8 byte       | 2.3E-308 to 1.7E+308   | 15 decimal places |
| long double | 10 byte      | 3.4E-4932 to 1.1E+4932 | 19 decimal places |

The header file float.h defines macros that allow you to use these values and other details about the binary representation of real numbers in your programs. The following example prints the storage space taken by a float type and its range values −

```c
#include <stdio.h>
#include <stdlib.h>
#include <limits.h>
#include <float.h>

int main(int argc, char** argv) {

    printf("Storage size for float : %d \n", sizeof(float));
    printf("FLT_MAX     :   %g\n", (float) FLT_MAX);
    printf("FLT_MIN     :   %g\n", (float) FLT_MIN);
    printf("-FLT_MAX    :   %g\n", (float) -FLT_MAX);
    printf("-FLT_MIN    :   %g\n", (float) -FLT_MIN);
    printf("DBL_MAX     :   %g\n", (double) DBL_MAX);
    printf("DBL_MIN     :   %g\n", (double) DBL_MIN);
    printf("-DBL_MAX     :  %g\n", (double) -DBL_MAX);
    printf("Precision value: %d\n", FLT_DIG );

    return 0;
}
```

When you compile and execute the above program, it produces the following result on Linux −

```c
Storage size for float : 4 
FLT_MAX      :   3.40282e+38
FLT_MIN      :   1.17549e-38
-FLT_MAX     :   -3.40282e+38
-FLT_MIN     :   -1.17549e-38
DBL_MAX      :   1.79769e+308
DBL_MIN      :   2.22507e-308
-DBL_MAX     :  -1.79769e+308
Precision value: 6

```

## The void Type

The void type specifies that no value is available. It is used in three kinds of situations −

| Sr.No. | Types & Description |
| ------ | ------------------- |
| 1      | **Function returns as void**<br>There are various functions in C which do not return any value or you can say they return void. A function with no return value has the return type as void. For example, **void exit (int status);**<br> |
| 2 | <br>**Function arguments as void**<br>There are various functions in C which do not accept any parameter. A function with no parameter can accept a void. For example, **int rand(void);**<br> |
| 3 | <br>**Pointers to void**<br>A pointer of type void \* represents the address of an object, but not its type. For example, a memory allocation function **void \*malloc( size\_t size );** returns a pointer to void which can be casted to any data type.<br> |

## C - Variables

A variable is nothing but a name given to a storage area that our programs can manipulate. Each variable in C has a specific type, which determines the size and layout of the variable's memory; the range of values that can be stored within that memory; and the set of operations that can be applied to the variable.

The name of a variable can be composed of letters, digits, and the underscore character. It must begin with either a letter or an underscore. Upper and lowercase letters are distinct because C is case-sensitive. Based on the basic types explained in the previous chapter, there will be the following basic variable types −

| Sr.No. | Type & Description |
| ------ | ------------------ |
| 1      | **char**<br>Typically a single octet(one byte). It is an integer type.<br> |
| 2 | <br>**int**<br>The most natural size of integer for the machine.<br> |
| 3 | <br>**float**<br>A single-precision floating point value.<br> |
| 4 | <br>**double**<br>A double-precision floating point value.<br> |
| 5 | <br>**void**<br>Represents the absence of type.<br> |

C programming language also allows to define various other types of variables, which we will cover in subsequent chapters like Enumeration, Pointer, Array, Structure, Union, etc. For this chapter, let us study only basic variable types.

## Variable Definition in C

A variable definition tells the compiler where and how much storage to create for the variable. A variable definition specifies a data type and contains a list of one or more variables of that type as follows −

```c
type variable_list;

```

Here, **type** must be a valid C data type including char, w\_char, int, float, double, bool, or any user-defined object; and **variable\_list** may consist of one or more identifier names separated by commas. Some valid declarations are shown here −

```c
int    i, j, k;
char   c, ch;
float  f, salary;
double d;

```

The line **int i, j, k;** declares and defines the variables i, j, and k; which instruct the compiler to create variables named i, j and k of type int.

Variables can be initialized (assigned an initial value) in their declaration. The initializer consists of an equal sign followed by a constant expression as follows −

```c
type variable_name = value;

```

Some examples are −

```c
extern int d = 3, f = 5;    // declaration of d and f. 
int d = 3, f = 5;           // definition and initializing d and f. 
byte z = 22;                // definition and initializes z. 
char x = 'x';               // the variable x has the value 'x'.

```

For definition without an initializer: variables with static storage duration are implicitly initialized with NULL (all bytes have the value 0); the initial value of all other variables are undefined.

## Variable Declaration in C

A variable declaration provides assurance to the compiler that there exists a variable with the given type and name so that the compiler can proceed for further compilation without requiring the complete detail about the variable. A variable definition has its meaning at the time of compilation only, the compiler needs actual variable definition at the time of linking the program.

A variable declaration is useful when you are using multiple files and you define your variable in one of the files which will be available at the time of linking of the program. You will use the keyword **extern** to declare a variable at any place. Though you can declare a variable multiple times in your C program, it can be defined only once in a file, a function, or a block of code.

### Example

Try the following example, where variables have been declared at the top, but they have been defined and initialized inside the main function −

```c
#include <stdio.h>

// Variable declaration:
extern int a, b;
extern int c;
extern float f;

int main () {

   /* variable definition: */
   int a, b;
   int c;
   float f;
 
   /* actual initialization */
   a = 10;
   b = 20;
  
   c = a + b;
   printf("value of c : %d \n", c);

   f = 70.0/3.0;
   printf("value of f : %f \n", f);
 
   return 0;
}
```

When the above code is compiled and executed, it produces the following result −

```c
value of c : 30
value of f : 23.333334

```

The same concept applies on function declaration where you provide a function name at the time of its declaration and its actual definition can be given anywhere else. For example −

```c
// function declaration
int func();

int main() {

   // function call
   int i = func();
}

// function definition
int func() {
   return 0;
}
```

## Lvalues and Rvalues in C

There are two kinds of expressions in C −

-   **lvalue** − Expressions that refer to a memory location are called "lvalue" expressions. An lvalue may appear as either the left-hand or right-hand side of an assignment.
    
-   **rvalue** − The term rvalue refers to a data value that is stored at some address in memory. An rvalue is an expression that cannot have a value assigned to it which means an rvalue may appear on the right-hand side but not on the left-hand side of an assignment.
    

Variables are lvalues and so they may appear on the left-hand side of an assignment. Numeric literals are rvalues and so they may not be assigned and cannot appear on the left-hand side. Take a look at the following valid and invalid statements −

```c
int g = 20; // valid statement

10 = 20; // invalid statement; would generate compile-time error

```

## C - Constants and Literals

Constants refer to fixed values that the program may not alter during its execution. These fixed values are also called **literals**.

Constants can be of any of the basic data types like _an integer constant, a floating constant, a character constant, or a string literal_. There are enumeration constants as well.

Constants are treated just like regular variables except that their values cannot be modified after their definition.

## Integer Literals

An integer literal can be a decimal, octal, or hexadecimal constant. A prefix specifies the base or radix: 0x or 0X for hexadecimal, 0 for octal, and nothing for decimal.

An integer literal can also have a suffix that is a combination of U and L, for unsigned and long, respectively. The suffix can be uppercase or lowercase and can be in any order.

Here are some examples of integer literals −

```c
212         /* Legal */
215u        /* Legal */
0xFeeL      /* Legal */
078         /* Illegal: 8 is not an octal digit */
032UU       /* Illegal: cannot repeat a suffix */

```

Following are other examples of various types of integer literals −

```c
85         /* decimal */
0213       /* octal */
0x4b       /* hexadecimal */
30         /* int */
30u        /* unsigned int */
30l        /* long */
30ul       /* unsigned long */

```

## Floating-point Literals

A floating-point literal has an integer part, a decimal point, a fractional part, and an exponent part. You can represent floating point literals either in decimal form or exponential form.

While representing decimal form, you must include the decimal point, the exponent, or both; and while representing exponential form, you must include the integer part, the fractional part, or both. The signed exponent is introduced by e or E.

Here are some examples of floating-point literals −

```c
3.14159       /* Legal */
314159E-5L    /* Legal */
510E          /* Illegal: incomplete exponent */
210f          /* Illegal: no decimal or exponent */
.e55          /* Illegal: missing integer or fraction */

```

## Character Constants

Character literals are enclosed in single quotes, e.g., 'x' can be stored in a simple variable of **char** type.

A character literal can be a plain character (e.g., 'x'), an escape sequence (e.g., '\\t'), or a universal character (e.g., '\\u02C0').

There are certain characters in C that represent special meaning when preceded by a backslash for example, newline (\\n) or tab (\\t).

-   [Here, you have a list of such escape sequence codes −](https://www.tutorialspoint.com/cprogramming/c_quick_guide.htm#)

Following is the example to show a few escape sequence characters −

```c
#include <stdio.h>

int main() {
   printf("Hello\tWorld\n\n");

   return 0;
}
```

When the above code is compiled and executed, it produces the following result −

```c
Hello World

```

## String Literals

String literals or constants are enclosed in double quotes "". A string contains characters that are similar to character literals: plain characters, escape sequences, and universal characters.

You can break a long line into multiple lines using string literals and separating them using white spaces.

Here are some examples of string literals. All the three forms are identical strings.

```c
"hello, dear"

"hello, \

dear"

"hello, " "d" "ear"

```

## Defining Constants

There are two simple ways in C to define constants −

-   Using **#define** preprocessor.
    
-   Using **const** keyword.
    

## The #define Preprocessor

Given below is the form to use #define preprocessor to define a constant −

```c
#define identifier value

```

The following example explains it in detail −

```c
#include <stdio.h>

#define LENGTH 10   
#define WIDTH  5
#define NEWLINE '\n'

int main() {
   int area;  
  
   area = LENGTH * WIDTH;
   printf("value of area : %d", area);
   printf("%c", NEWLINE);

   return 0;
}
```

When the above code is compiled and executed, it produces the following result −

```c
value of area : 50

```

## The const Keyword

You can use **const** prefix to declare constants with a specific type as follows −

```c
const type variable = value;

```

The following example explains it in detail −

```c
#include <stdio.h>

int main() {
   const int  LENGTH = 10;
   const int  WIDTH = 5;
   const char NEWLINE = '\n';
   int area;  
   
   area = LENGTH * WIDTH;
   printf("value of area : %d", area);
   printf("%c", NEWLINE);

   return 0;
}
```

When the above code is compiled and executed, it produces the following result −

```c
value of area : 50

```

Note that it is a good programming practice to define constants in CAPITALS.

## C - Storage Classes

A storage class defines the scope (visibility) and life-time of variables and/or functions within a C Program. They precede the type that they modify. We have four different storage classes in a C program −

-   auto
-   register
-   static
-   extern

## The auto Storage Class

The **auto** storage class is the default storage class for all local variables.

```c
{
   int mount;
   auto int month;
}
```

The example above defines two variables with in the same storage class. 'auto' can only be used within functions, i.e., local variables.

## The register Storage Class

The **register** storage class is used to define local variables that should be stored in a register instead of RAM. This means that the variable has a maximum size equal to the register size (usually one word) and can't have the unary '&' operator applied to it (as it does not have a memory location).

```c
{
   register int  miles;
}
```

The register should only be used for variables that require quick access such as counters. It should also be noted that defining 'register' does not mean that the variable will be stored in a register. It means that it MIGHT be stored in a register depending on hardware and implementation restrictions.

## The static Storage Class

The **static** storage class instructs the compiler to keep a local variable in existence during the life-time of the program instead of creating and destroying it each time it comes into and goes out of scope. Therefore, making local variables static allows them to maintain their values between function calls.

The static modifier may also be applied to global variables. When this is done, it causes that variable's scope to be restricted to the file in which it is declared.

In C programming, when **static** is used on a global variable, it causes only one copy of that member to be shared by all the objects of its class.

```c
#include <stdio.h>
 
/* function declaration */
void func(void);
 
static int count = 5; /* global variable */
 
main() {

   while(count--) {
      func();
   }

   return 0;
}

/* function definition */
void func( void ) {

   static int i = 5; /* local static variable */
   i++;

   printf("i is %d and count is %d\n", i, count);
}
```

When the above code is compiled and executed, it produces the following result −

```c
i is 6 and count is 4
i is 7 and count is 3
i is 8 and count is 2
i is 9 and count is 1
i is 10 and count is 0

```

## The extern Storage Class

The **extern** storage class is used to give a reference of a global variable that is visible to ALL the program files. When you use 'extern', the variable cannot be initialized however, it points the variable name at a storage location that has been previously defined.

When you have multiple files and you define a global variable or function, which will also be used in other files, then _extern_ will be used in another file to provide the reference of defined variable or function. Just for understanding, _extern_ is used to declare a global variable or function in another file.

The extern modifier is most commonly used when there are two or more files sharing the same global variables or functions as explained below.

**First File: main.c**

```c
#include <stdio.h>
 
int count ;
extern void write_extern();
 
main() {
   count = 5;
   write_extern();
}
```

**Second File: support.c**

```c
#include <stdio.h>
 
extern int count;
 
void write_extern(void) {
   printf("count is %d\n", count);
}
```

Here, _extern_ is being used to declare _count_ in the second file, where as it has its definition in the first file, main.c. Now, compile these two files as follows −

```c
$gcc main.c support.c

```

It will produce the executable program **a.out**. When this program is executed, it produces the following result −

```c
count is 5

```

## C - Operators

An operator is a symbol that tells the compiler to perform specific mathematical or logical functions. C language is rich in built-in operators and provides the following types of operators −

-   Arithmetic Operators
-   Relational Operators
-   Logical Operators
-   Bitwise Operators
-   Assignment Operators
-   Misc Operators

We will, in this chapter, look into the way each operator works.

## Arithmetic Operators

The following table shows all the arithmetic operators supported by the C language. Assume variable **A** holds 10 and variable **B** holds 20 then −

[Show Examples](https://www.tutorialspoint.com/cprogramming/c_arithmetic_operators.htm)

| Operator | Description                                                  | Example      |
| -------- | ------------------------------------------------------------ | ------------ |
| +        | Adds two operands.                                           | A + B = 30   |
| −        | Subtracts second operand from the first.                     | A − B = -10  |
| \*       | Multiplies both operands.                                    | A \* B = 200 |
| /        | Divides numerator by de-numerator.                           | B / A = 2    |
| %        | Modulus Operator and remainder of after an integer division. | B % A = 0    |
| ++       | Increment operator increases the integer value by one.       | A++ = 11     |
| \--      | Decrement operator decreases the integer value by one.       | A-- = 9      |

## Relational Operators

The following table shows all the relational operators supported by C. Assume variable **A** holds 10 and variable **B** holds 20 then −

[Show Examples](https://www.tutorialspoint.com/cprogramming/c_relational_operators.htm)

| Operator | Description                                                                                                                          | Example               |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------ | --------------------- |
| \==      | Checks if the values of two operands are equal or not. If yes, then the condition becomes true.                                      | (A == B) is not true. |
| !=       | Checks if the values of two operands are equal or not. If the values are not equal, then the condition becomes true.                 | (A != B) is true.     |
| \>       | Checks if the value of left operand is greater than the value of right operand. If yes, then the condition becomes true.             | (A > B) is not true.  |
| <        | Checks if the value of left operand is less than the value of right operand. If yes, then the condition becomes true.                | (A < B) is true.      |
| \>=      | Checks if the value of left operand is greater than or equal to the value of right operand. If yes, then the condition becomes true. | (A >= B) is not true. |
| <=       | Checks if the value of left operand is less than or equal to the value of right operand. If yes, then the condition becomes true.    | (A <= B) is true.     |

## Logical Operators

Following table shows all the logical operators supported by C language. Assume variable **A** holds 1 and variable **B** holds 0, then −

[Show Examples](https://www.tutorialspoint.com/cprogramming/c_logical_operators.htm)
