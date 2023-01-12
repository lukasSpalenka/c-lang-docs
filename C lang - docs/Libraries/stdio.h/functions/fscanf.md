---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fscanf.htm
author: 
---

# C library function - fscanf()

> ## Excerpt
> C library function - fscanf(),  The C library function int fscanf(FILE *stream, const char *format, ...) reads formatted input from a stream.

---
---

  

## Description

The C library function **int fscanf(FILE \*stream, const char \*format, ...)** reads formatted input from a stream.

## Declaration

Following is the declaration for fscanf() function.

```c
int fscanf(FILE *stream, const char *format, ...)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    
-   **format** − This is the C string that contains one or more of the following items − _Whitespace character, Non-whitespace character_ and _Format specifiers_. A format specifier will be as **\\[=%\\[\\*\\]\\[width\\]\\[modifiers\\]type=\\]**, which is explained below −
    

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

-   **additional arguments** − Depending on the format string, the function may expect a sequence of additional arguments, each containing one value to be inserted instead of each %-tag specified in the format parameter (if any). There should be the same number of these arguments as the number of %-tags that expect a value.
    

## Return Value

This function returns the number of input items successfully matched and assigned, which can be fewer than provided for, or even zero in the event of an early matching failure.

## Example

The following example shows the usage of fscanf() function.

```c
#include <stdio.h>
#include <stdlib.h>


int main () {
   char str1[10], str2[10], str3[10];
   int year;
   FILE * fp;

   fp = fopen ("file.txt", "w+");
   fputs("We are in 2012", fp);
   
   rewind(fp);
   fscanf(fp, "%s %s %s %d", str1, str2, str3, &year);
   
   printf("Read String1 |%s|\n", str1 );
   printf("Read String2 |%s|\n", str2 );
   printf("Read String3 |%s|\n", str3 );
   printf("Read Integer |%d|\n", year );

   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Read String1 |We|
Read String2 |are|
Read String3 |in|
Read Integer |2012|

```


