---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_mbstowcs.htm
author: 
---

# C library function - mbstowcs()

> ## Excerpt
> C library function - mbstowcs(),  The C library function size_t mbstowcs(schar_t *pwcs, const char *str, size_t n) converts the string of multi-byte characters pointed to, by the argument str to

---
---

  

## Description

The C library function **size\_t mbstowcs(schar\_t \*pwcs, const char \*str, size\_t n)** converts the string of multi-byte characters pointed to, by the argument **str** to the array pointed to by **pwcs**.

## Declaration

Following is the declaration for mbstowcs() function.

```c
size_t mbstowcs(schar_t *pwcs, const char *str, size_t n)
```

## Parameters

-   **pwcs** − This is the pointer to an array of wchar\_t elements that is long enough to store a wide string max characters long.
    
-   **str** − This is the C multi-byte character string to be interpreted.
    
-   **n** − This is the maximum number of wchar\_t characters to be interpreted.
    

## Return Value

This function returns the number of characters translated, excluding the ending null-character. If an invalid multi-byte character is encountered, a -1 value is returned.

## Example

The following example shows the usage of mbstowcs() function.

```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>

int main () {
   int len;
   char *pmbnull  = NULL;
   char *pmb = (char *)malloc( MB_CUR_MAX );
   wchar_t *pwc = L"Hi";
   wchar_t *pwcs = (wchar_t *)malloc( sizeof( wchar_t ));

   printf("Converting to multibyte string\n");
   len = wcstombs( pmb, pwc, MB_CUR_MAX);
   printf("Characters converted %d\n", len);
   printf("Hex value of first multibyte character: %#.4x\n", pmb);
   
   printf("Converting back to Wide-Character string\n");
   len = mbstowcs( pwcs, pmb, MB_CUR_MAX);
   printf("Characters converted %d\n", len);
   printf("Hex value of first wide character %#.4x\n\n", pwcs);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Converting to multibyte string
Characters converted 1
Hex value of first multibyte character: 0x19a60010
Converting back to Wide-Character string
Characters converted 1
Hex value of first wide character 0x19a60030

```


