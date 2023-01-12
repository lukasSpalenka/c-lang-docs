---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_wcstombs.htm
author: 
---

# C library function - wcstombs()

> ## Excerpt
> C library function - wcstombs(),  The C library function size_t wcstombs(char *str, const wchar_t *pwcs, size_t n) converts the wide-character string pwcs to a multibyte string starting at str.

---
---

  

## Description

The C library function **size\_t wcstombs(char \*str, const wchar\_t \*pwcs, size\_t n)** converts the wide-character string **pwcs** to a multibyte string starting at **str**. At most **n** bytes are written to **str**.

## Declaration

Following is the declaration for wcstombs() function.

```c
size_t wcstombs(char *str, const wchar_t *pwcs, size_t n)
```

## Parameters

-   **str** − This is the pointer to an array of char elements at least n bytes long.
    
-   **pwcs** − This is wide-character string to be converted.
    
-   **n** − This is the maximum number of bytes to be written to str.
    

## Return Value

This function returns the number of bytes (not characters) converted and written to str, excluding the ending null-character. If an invalid multibyte character is encountered, -1 value is returned.

## Example

The following example shows the usage of wcstombs() function.

```c
#include <stdio.h>
#include <stdlib.h>

#define BUFFER_SIZE 50

int main () {
   size_t ret;
   char *MB = (char *)malloc( BUFFER_SIZE );
   wchar_t *WC = L"http://www.tutorialspoint.com";

   /* converting wide-character string */
   ret = wcstombs(MB, WC, BUFFER_SIZE);
   
   printf("Characters converted = %u\n", ret);
   printf("Multibyte character = %s\n\n", MB);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Characters converted = 29
Multibyte character = http://www.tutorialspoint.com

```


