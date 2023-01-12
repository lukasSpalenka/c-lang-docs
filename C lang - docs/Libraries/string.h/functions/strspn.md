---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strspn.htm
author: 
---

# C library function - strspn()

> ## Excerpt
> C library function - strspn(),  The C library function size_t strspn(const char *str1, const char *str2) calculates the length of the initial segment of str1 which consists entirely of charact

---
---

  

## Description

The C library function **size\_t strspn(const char \*str1, const char \*str2)** calculates the length of the initial segment of **str1** which consists entirely of characters in **str2**.

## Declaration

Following is the declaration for strspn() function.

```c
size_t strspn(const char *str1, const char *str2)
```

## Parameters

-   **str1** − This is the main C string to be scanned.
    
-   **str2** − This is the string containing the list of characters to match in str1.
    

## Return Value

This function returns the number of characters in the initial segment of str1 which consist only of characters from str2.

## Example

The following example shows the usage of strspn() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   int len;
   const char str1[] = "ABCDEFG019874";
   const char str2[] = "ABCD";

   len = strspn(str1, str2);

   printf("Length of initial segment matching %d\n", len );
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Length of initial segment matching 4

```


