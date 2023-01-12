---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strcspn.htm
author: 
---

# C library function - strcspn()

> ## Excerpt
> C library function - strcspn(),  The C library function size_t strcspn(const char *str1, const char *str2)  calculates the length of the initial segment of str1, which consists entirely of char

---
---

  

## Description

The C library function **size\_t strcspn(const char \*str1, const char \*str2)** calculates the length of the initial segment of **str1**, which consists entirely of characters not in **str2**.

## Declaration

Following is the declaration for strcspn() function.

```c
size_t strcspn(const char *str1, const char *str2)
```

## Parameters

-   **str1** − This is the main C string to be scanned.
    
-   **str2** − This is the string containing a list of characters to match in str1.
    

## Return Value

This function returns the number of characters in the initial segment of string str1 which are not in the string str2.

## Example

The following example shows the usage of strcspn() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   int len;
   const char str1[] = "ABCDEF4960910";
   const char str2[] = "013";

   len = strcspn(str1, str2);

   printf("First matched character is at %d\n", len + 1);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
First matched character is at 10

```


