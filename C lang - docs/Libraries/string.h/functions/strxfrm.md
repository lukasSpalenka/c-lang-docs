---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strxfrm.htm
author: 
---

# C library function - strxfrm()

> ## Excerpt
> C library function - strxfrm(),  The C library function size_t strxfrm(char *dest, const char *src, size_t n) transforms the first n characters of the string src into current locale and place t

---
---

  

## Description

The C library function **size\_t strxfrm(char \*dest, const char \*src, size\_t n)** transforms the first **n** characters of the string **src** into current locale and place them in the string **dest**.

## Declaration

Following is the declaration for strxfrm() function.

```c
size_t strxfrm(char *dest, const char *src, size_t n)
```

## Parameters

-   **dest** − This is the pointer to the destination array where the content is to be copied. It can be a null pointer if the argument for n is zero.
    
-   **src** − This is the C string to be transformed into current locale.
    
-   **n** − The maximum number of characters to be copied to str1.
    

## Return Value

This function returns the length of the transformed string, not including the terminating null-character.

## Example

The following example shows the usage of strxfrm() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char dest[20];
   char src[20];
   int len;

   strcpy(src, "Tutorials Point");
   len = strxfrm(dest, src, 20);

   printf("Length of string |%s| is: |%d|", dest, len);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Length of string |Tutorials Point| is: |15|

```


