---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strpbrk.htm
author: 
---

# C library function - strpbrk()

> ## Excerpt
> C library function - strpbrk(),  The C library function char *strpbrk(const char *str1, const char *str2)  finds the first character in the string str1 that matches any character specified in s

---
---

  

## Description

The C library function **char \*strpbrk(const char \*str1, const char \*str2)** finds the first character in the string **str1** that matches any character specified in **str2**. This does not include the terminating null-characters.

## Declaration

Following is the declaration for strpbrk() function.

```c
char *strpbrk(const char *str1, const char *str2)
```

## Parameters

-   **str1** − This is the C string to be scanned.
    
-   **str2** − This is the C string containing the characters to match.
    

## Return Value

This function returns a pointer to the character in str1 that matches one of the characters in str2, or NULL if no such character is found.

## Example

The following example shows the usage of strpbrk() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   const char str1[] = "abcde2fghi3jk4l";
   const char str2[] = "34";
   char *ret;

   ret = strpbrk(str1, str2);
   if(ret) {
      printf("First matching character: %c\n", *ret);
   } else {
      printf("Character not found");
   }
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
First matching character: 3

```


