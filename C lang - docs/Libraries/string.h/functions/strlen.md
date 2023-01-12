---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strlen.htm
author: 
---

# C library function - strlen()

> ## Excerpt
> C library function - strlen(),  The C library function size_t strlen(const char *str) computes the length of the string str up to, but not including the terminating null character.

---
---

  

## Description

The C library function **size\_t strlen(const char \*str)** computes the length of the string **str** up to, but not including the terminating null character.

## Declaration

Following is the declaration for strlen() function.

```c
size_t strlen(const char *str)
```

## Parameters

-   **str** − This is the string whose length is to be found.
    

## Return Value

This function returns the length of string.

## Example

The following example shows the usage of strlen() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str[50];
   int len;

   strcpy(str, "This is tutorialspoint.com");

   len = strlen(str);
   printf("Length of |%s| is |%d|\n", str, len);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Length of |This is tutorialspoint.com| is |26|

```


