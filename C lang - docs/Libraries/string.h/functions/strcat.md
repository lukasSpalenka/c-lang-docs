---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strcat.htm
author: 
---

# C library function - strcat()

> ## Excerpt
> C library function - strcat(),  The C library function char *strcat(char *dest, const char *src) appends the string pointed to by src to the end of the string pointed to by dest.

---
---

  

## Description

The C library function **char \*strcat(char \*dest, const char \*src)** appends the string pointed to by **src** to the end of the string pointed to by **dest**.

## Declaration

Following is the declaration for strcat() function.

```c
char *strcat(char *dest, const char *src)
```

## Parameters

-   **dest** − This is pointer to the destination array, which should contain a C string, and should be large enough to contain the concatenated resulting string.
    
-   **src** − This is the string to be appended. This should not overlap the destination.
    

## Return Value

This function returns a pointer to the resulting string dest.

## Example

The following example shows the usage of strcat() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char src[50], dest[50];

   strcpy(src,  "This is source");
   strcpy(dest, "This is destination");

   strcat(dest, src);

   printf("Final destination string : |%s|", dest);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Final destination string : |This is destinationThis is source|

```


