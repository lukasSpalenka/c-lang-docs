---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_sscanf.htm
author: 
---

# C library function - sscanf()

> ## Excerpt
> C library function - sscanf(),  The C library function int sscanf(const char *str, const char *format, ...) reads formatted input from a string.

---
---

  

## Description

The C library function **int sscanf(const char \*str, const char \*format, ...)** reads formatted input from a string.

## Declaration

Following is the declaration for sscanf() function.

```c
int sscanf(const char *str, const char *format, ...)
```

## Parameters

-   **str** − This is the C string that the function processes as its source to retrieve the data.
    
-   **format** − This is the C string that contains one or more of the following items: _Whitespace character, Non-whitespace character and Format specifiers_
    
    A format specifier follows this prototype: \[=%\[\*\]\[width\]\[modifiers\]type=\]
    

| Sr.No. | Argument & Description |
| --- | --- |
| 1 |  **\***<br>This is an optional starting asterisk, which indicates that the data is to be read from the stream but ignored, i.e. it is not stored in the corresponding argument.<br> |
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

-   **other arguments** − This function expects a sequence of pointers as additional arguments, each one pointing to an object of the type specified by their corresponding %-tag within the format string, in the same order.
    
    For each format specifier in the format string that retrieves data, an additional argument should be specified. If you want to store the result of a sscanf operation on a regular variable you should precede its identifier with the reference operator, i.e. an ampersand sign (&), like: int n; sscanf (str,"%d",&n);
    

## Return Value

On success, the function returns the number of variables filled. In the case of an input failure before any data could be successfully read, EOF is returned.

## Example

The following example shows the usage of sscanf() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
   int day, year;
   char weekday[20], month[20], dtm[100];

   strcpy( dtm, "Saturday March 25 1989" );
   sscanf( dtm, "%s %s %d  %d", weekday, month, &day, &year );

   printf("%s %d, %d = %s\n", month, day, year, weekday );
    
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
March 25, 1989 = Saturday

```


