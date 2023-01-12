---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strstr.htm
author: 
---

# C library function - strstr()

> ## Excerpt
> C library function - strstr(),  The C library function char *strstr(const char *haystack, const char *needle) function finds the first occurrence of the substring needle in the string haystack

---
---

  

## Description

The C library function **char \*strstr(const char \*haystack, const char \*needle)** function finds the first occurrence of the substring **needle** in the string **haystack**. The terminating '\\0' characters are not compared.

## Declaration

Following is the declaration for strstr() function.

```c
char *strstr(const char *haystack, const char *needle)
```

## Parameters

-   **haystack** − This is the main C string to be scanned.
    
-   **needle** − This is the small string to be searched with-in haystack string.
    

## Return Value

This function returns a pointer to the first occurrence in haystack of any of the entire sequence of characters specified in needle, or a null pointer if the sequence is not present in haystack.

## Example

The following example shows the usage of strstr() function.

```c
#include <stdio.h>
#include <string.h>


int main () {
   const char haystack[20] = "TutorialsPoint";
   const char needle[10] = "Point";
   char *ret;

   ret = strstr(haystack, needle);

   printf("The substring is: %s\n", ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The substring is: Point

```


