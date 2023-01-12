---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_mbtowc.htm
author: 
---

# C library function - mbtowc()

> ## Excerpt
> C library function - mbtowc(),  The C library function int mbtowc(whcar_t *pwc, const char *str, size_t n) converts a multibyte sequence to a wide character.

---
---

  

## Description

The C library function **int mbtowc(whcar\_t \*pwc, const char \*str, size\_t n)** converts a multibyte sequence to a wide character.

## Declaration

Following is the declaration for mbtowc() function.

```c
int mbtowc(whcar_t *pwc, const char *str, size_t n)
```

## Parameters

-   **pwc** − This is the pointer to an object of type wchar\_t.
    
-   **str** − This is the pointer to the first byte of a multi-byte character.
    
-   **n** − This is the maximum number of bytes to be checked for character length.
    

## Return Value

-   If str is not NULL, the mbtowc() function returns the number of consumed bytes starting at str, or 0 if **s** points to a null byte, or -1 upon failure.
    
-   If str is NULL, the mbtowc() function returns non-zero if the encoding has non-trivial shift state, or zero if the encoding is stateless.
    

## Example

The following example shows the usage of mbtowc() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
   char *str = "This is tutorialspoint.com";
   wchar_t mb[100];
   int len;
   
   len = mblen(NULL, MB_CUR_MAX); 

   mbtowc(mb, str, len*strlen(str) );
   
   wprintf(L"%ls \n", mb );   
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result which will be in multi-byte, a kind of binary output.

```c
???

```


