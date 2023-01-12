---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_putchar.htm
author: 
---

# C library function - putchar()

> ## Excerpt
> C library function - putchar(),  The C library function int putchar(int char) writes a character (an unsigned char) specified by the argument char to stdout.

---
---

  

## Description

The C library function **int putchar(int char)** writes a character (an unsigned char) specified by the argument char to stdout.

## Declaration

Following is the declaration for putchar() function.

```c
int putchar(int char)
```

## Parameters

-   **char** − This is the character to be written. This is passed as its int promotion.
    

## Return Value

This function returns the character written as an unsigned char cast to an int or EOF on error.

## Example

The following example shows the usage of putchar() function.

```c
#include <stdio.h>

int main () {
   char ch;

   for(ch = 'A' ; ch <= 'Z' ; ch++) {
      putchar(ch);
   }
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
ABCDEFGHIJKLMNOPQRSTUVWXYZ

```


