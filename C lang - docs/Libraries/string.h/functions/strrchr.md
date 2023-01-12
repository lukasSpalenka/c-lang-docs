---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strrchr.htm
author: 
---

# C library function - strrchr()

> ## Excerpt
> C library function - strrchr(),  The C library function char *strrchr(const char *str, int c) searches for the last occurrence of the character c (an unsigned char) in the string pointed to, by

---
---

  

## Description

The C library function **char \*strrchr(const char \*str, int c)** searches for the last occurrence of the character **c** (an unsigned char) in the string pointed to, by the argument **str**.

## Declaration

Following is the declaration for strrchr() function.

```c
char *strrchr(const char *str, int c)
```

## Parameters

-   **str** − This is the C string.
    
-   **c** − This is the character to be located. It is passed as its int promotion, but it is internally converted back to char.
    

## Return Value

This function returns a pointer to the last occurrence of character in str. If the value is not found, the function returns a null pointer.

## Example

The following example shows the usage of strrchr() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   int len;
   const char str[] = "http://www.tutorialspoint.com";
   const char ch = '.';
   char *ret;

   ret = strrchr(str, ch);

   printf("String after |%c| is - |%s|\n", ch, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
String after |.| is - |.com|

```


