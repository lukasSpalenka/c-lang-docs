---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_puts.htm
author: 
---

# C library function - puts()

> ## Excerpt
> C library function - puts(),  The C library function int puts(const char *str) writes a string to stdout up to but not including the null character. A newline character is appended to the ou

---
---

  

## Description

The C library function **int puts(const char \*str)** writes a string to stdout up to but not including the null character. A newline character is appended to the output.

## Declaration

Following is the declaration for puts() function.

```c
int puts(const char *str)
```

## Parameters

-   **str** − This is the C string to be written.
    

## Return Value

If successful, non-negative value is returned. On error, the function returns EOF.

## Example

The following example shows the usage of puts() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str1[15];
   char str2[15];

   strcpy(str1, "tutorialspoint");
   strcpy(str2, "compileonline");

   puts(str1);
   puts(str2);
   
   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
tutorialspoint
compileonline

```


