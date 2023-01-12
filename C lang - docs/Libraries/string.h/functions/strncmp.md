---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strncmp.htm
author: 
---

# C library function - strncmp()

> ## Excerpt
> C library function - strncmp(),  The C library function int strncmp(const char *str1, const char *str2, size_t n) compares at most the first n bytes of str1 and str2.

---
---

  

## Description

The C library function **int strncmp(const char \*str1, const char \*str2, size\_t n)** compares at most the first **n** bytes of **str1** and **str2**.

## Declaration

Following is the declaration for strncmp() function.

```c
int strncmp(const char *str1, const char *str2, size_t n)
```

## Parameters

-   **str1** − This is the first string to be compared.
    
-   **str2** − This is the second string to be compared.
    
-   **n** − The maximum number of characters to be compared.
    

## Return Value

This function return values that are as follows −

-   if Return value < 0 then it indicates str1 is less than str2.
    
-   if Return value > 0 then it indicates str2 is less than str1.
    
-   if Return value = 0 then it indicates str1 is equal to str2.
    

## Example

The following example shows the usage of strncmp() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str1[15];
   char str2[15];
   int ret;

   strcpy(str1, "abcdef");
   strcpy(str2, "ABCDEF");

   ret = strncmp(str1, str2, 4);

   if(ret < 0) {
      printf("str1 is less than str2");
   } else if(ret > 0) {
      printf("str2 is less than str1");
   } else {
      printf("str1 is equal to str2");
   }
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
str2 is less than str1

```


