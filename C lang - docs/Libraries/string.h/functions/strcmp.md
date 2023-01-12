---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strcmp.htm
author: 
---

# C library function - strcmp()

> ## Excerpt
> C library function - strcmp(),  The C library function int strcmp(const char *str1, const char *str2) compares the string pointed to, by str1 to the string pointed to by str2.

---
---

  

## Description

The C library function **int strcmp(const char \*str1, const char \*str2)** compares the string pointed to, by **str1** to the string pointed to by **str2**.

## Declaration

Following is the declaration for strcmp() function.

```c
int strcmp(const char *str1, const char *str2)
```

## Parameters

-   **str1** − This is the first string to be compared.
    
-   **str2** − This is the second string to be compared.
    

## Return Value

This function return values that are as follows −

-   if Return value < 0 then it indicates str1 is less than str2.
    
-   if Return value > 0 then it indicates str2 is less than str1.
    
-   if Return value = 0 then it indicates str1 is equal to str2.
    

## Example

The following example shows the usage of strcmp() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str1[15];
   char str2[15];
   int ret;


   strcpy(str1, "abcdef");
   strcpy(str2, "ABCDEF");

   ret = strcmp(str1, str2);

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


