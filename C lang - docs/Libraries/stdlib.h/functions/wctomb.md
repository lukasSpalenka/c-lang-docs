---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_wctomb.htm
author: 
---

# C library function - wctomb()

> ## Excerpt
> C library function - wctomb(),  The C library function int wctomb(char *str, wchar_t wchar) function converts the wide character wchar to its multibyte representation and stores it at the begi

---
---

  

## Description

The C library function **int wctomb(char \*str, wchar\_t wchar)** function converts the wide character **wchar** to its multibyte representation and stores it at the beginning of the character array pointed to by **str**.

## Declaration

Following is the declaration for wctomb() function.

```c
int wctomb(char *str, wchar_t wchar)
```

## Parameters

-   **str** − This is the pointer to an array large enough to hold a multibyte character,
    
-   **wchar** − This is the wide character of type wchar\_t.
    

## Return Value

-   If str is not NULL, the wctomb() function returns the number of bytes that have been written to the byte array at str. If wchar cannot be represented as a multibyte sequence, -1 is returned.
    
-   If str is NULL, the wctomb() function returns non-zero if the encoding has non-trivial shift state, or zero if the encoding is stateless.
    

## Example

The following example shows the usage of wctomb() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   int i;
   wchar_t wc = L'a';
   char *pmbnull = NULL;
   char *pmb = (char *)malloc(sizeof( char ));

   printf("Converting wide character:\n");
   i = wctomb( pmb, wc );
   printf("Characters converted: %u\n", i);
   printf("Multibyte character: %.1s\n", pmb);

   printf("Trying to convert when target is NULL:\n");
   i = wctomb( pmbnull, wc );
   printf("Characters converted: %u\n", i);
   /* this will not print any value */
   printf("Multibyte character: %.1s\n", pmbnull);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Converting wide character:
Characters converted: 1
Multibyte character: a
Trying to convert when target is NULL:
Characters converted: 0
Multibyte character: 

```


