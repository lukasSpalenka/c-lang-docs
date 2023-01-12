---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_scanf.htm
author: 
---

# C library function - scanf()

> ## Excerpt
> C library function - scanf(),  The C library function int scanf(const char *format, ...) reads formatted input from stdin.

---
---

  

## Description

The C library function **int scanf(const char \*format, ...)** reads formatted input from stdin.

## Declaration

Following is the declaration for scanf() function.

```c
int scanf(const char *format, ...)
```

## Parameters

-   **format** − This is the C string that contains one or more of the following items −
    
    _Whitespace character, Non-whitespace character and Format specifiers_. A format specifier will be like **\[=%\[\*\]\[width\]\[modifiers\]type=\]** as explained below −
    

| Sr.No. | Argument & Description |
| --- | --- |
| 1 |  **\***<br>This is an optional starting asterisk indicates that the data is to be read from the stream but ignored, i.e. it is not stored in the corresponding argument.<br> |
| 2 | <br>**width**<br>This specifies the maximum number of characters to be read in the current reading operation.<br> |
| 3 | <br>**modifiers**<br>Specifies a size different from int (in the case of d, i and n), unsigned int (in the case of o, u and x) or float (in the case of e, f and g) for the data pointed by the corresponding additional argument: h : short int (for d, i and n), or unsigned short int (for o, u and x) l : long int (for d, i and n), or unsigned long int (for o, u and x), or double (for e, f and g) L : long double (for e, f and g)<br> |
| 4 | <br>**type**<br>A character specifying the type of data to be read and how it is expected to be read. See next table.<br> |

### fscanf type specifiers

| type | Qualifying Input | Type of argument |
| --- | --- | --- |
| c | Single character: Reads the next character. If a width different from 1 is specified, the function reads width characters and stores them in the successive locations of the array passed as argument. No null character is appended at the end. | char \* |
| d | Decimal integer: Number optionally preceded with a + or - sign | int \* |
| e, E, f, g, G | Floating point: Decimal number containing a decimal point, optionally preceded by a + or - sign and optionally followed by the e or E character and a decimal number. Two examples of valid entries are -732.103 and 7.12e4 | float \* |
| o | Octal Integer: | int \* |
| s | String of characters. This will read subsequent characters until a whitespace is found (whitespace characters are considered to be blank, newline and tab). | char \* |
| u | Unsigned decimal integer. | unsigned int \* |
| x, X | Hexadecimal Integer | int \* |

-   **additional arguments** − Depending on the format string, the function may expect a sequence of additional arguments, each containing one value to be inserted instead of each %-tag specified in the format parameter, if any. There should be the same number of these arguments as the number of %-tags that expect a value.
    

## Return Value

On success, the function returns the number of items of the argument list successfully read. If a reading error happens or the end-of-file is reached while reading, the proper indicator is set (feof or ferror) and, if either happens before any data could be successfully read, EOF is returned.

## Example

The following example shows the usage of scanf() function.

```c
#include <stdio.h>

int main () {
   char str1[20], str2[30];

   printf("Enter name: ");
   scanf("%19s", str1);

   printf("Enter your website name: ");
   scanf("%29s", str2);

   printf("Entered Name: %s\n", str1);
   printf("Entered Website:%s", str2);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result in interactive mode −

```c
Enter name: admin
Enter your website name: www.tutorialspoint.com

Entered Name: admin
Entered Website: www.tutorialspoint.com

```

> **Please note:** if we enter a name longer than 20 characters, or a website longer than 30, it will overflow the buffers provided. And if we enter a name longer than 19 characters, or a website longer than 29, then printf will not find a trailing null byte, so it will start reading other parts of the stack and random garbage - in other words a buffer overrun.
> 
> So in this one code example you have both a buffer overflow and a buffer overrun. In many cases a vulnerability like this is enough to compromise an application written in C.
> 
> We should use %19s and %29s instead of %s to prevent this vulnerability. It will cut off the extra characters, but it will be safe.


