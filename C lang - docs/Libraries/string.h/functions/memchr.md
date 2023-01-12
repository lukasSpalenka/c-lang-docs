---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_memchr.htm
author: 
---

# C library function - memchr()

> ## Excerpt
> C library function - memchr(),  The C library function void *memchr(const void *str, int c, size_t n) searches for the first occurrence of the character c (an unsigned char) in the first n byt

---
---

  

## Description

The C library function **void \*memchr(const void \*str, int c, size\_t n)** searches for the first occurrence of the character **c** (an unsigned char) in the first **n** bytes of the string pointed to, by the argument **str**.

## Declaration

Following is the declaration for memchr() function.

```c
void *memchr(const void *str, int c, size_t n)
```

## Parameters

-   **str** − This is the pointer to the block of memory where the search is performed.
    
-   **c** − This is the value to be passed as an int, but the function performs a byte per byte search using the unsigned char conversion of this value.
    
-   **n** − This is the number of bytes to be analyzed.
    

## Return Value

This function returns a pointer to the matching byte or NULL if the character does not occur in the given memory area.

## Example

The following example shows the usage of memchr() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   const char str[] = "http://www.tutorialspoint.com";
   const char ch = '.';
   char *ret;

   ret = memchr(str, ch, strlen(str));

   printf("String after |%c| is - |%s|\n", ch, ret);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
String after |.| is - |.tutorialspoint.com|

```


