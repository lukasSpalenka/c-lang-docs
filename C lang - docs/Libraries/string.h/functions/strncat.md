---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strncat.htm
author: 
---

# C library function - strncat()

> ## Excerpt
> C library function - strncat(),  The C library function char *strncat(char *dest, const char *src, size_t n) appends the string pointed to by src to the end of the string pointed to by dest up

---
---

  

## Description

The C library function **char \*strncat(char \*dest, const char \*src, size\_t n)** appends the string pointed to by **src** to the end of the string pointed to by **dest** up to **n** characters long.

## Declaration

Following is the declaration for strncat() function.

```c
char *strncat(char *dest, const char *src, size_t n)
```

## Parameters

-   **dest** − This is pointer to the destination array, which should contain a C string, and should be large enough to contain the concatenated resulting string which includes the additional null-character.
    
-   **src** − This is the string to be appended.
    
-   **n** − This is the maximum number of characters to be appended.
    

## Return Value

This function returns a pointer to the resulting string dest.

## Example

The following example shows the usage of strncat() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char src[50], dest[50];

   strcpy(src,  "This is source");
   strcpy(dest, "This is destination");

   strncat(dest, src, 15);

   printf("Final destination string : |%s|", dest);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Final destination string : |This is destinationThis is source|

```


