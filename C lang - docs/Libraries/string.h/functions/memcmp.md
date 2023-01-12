---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_memcmp.htm
author: 
---

# C library function - memcmp()

> ## Excerpt
> C library function - memcmp(),  The C library function int memcmp(const void *str1, const void *str2, size_t n)) compares the first n bytes of memory area str1 and memory area str2.

---
---

  

## Description

The C library function **int memcmp(const void \*str1, const void \*str2, size\_t n))** compares the first **n** bytes of memory area **str1** and memory area **str2**.

## Declaration

Following is the declaration for memcmp() function.

```c
int memcmp(const void *str1, const void *str2, size_t n)
```

## Parameters

-   **str1** − This is the pointer to a block of memory.
    
-   **str2** − This is the pointer to a block of memory.
    
-   **n** − This is the number of bytes to be compared.
    

## Return Value

-   if Return value < 0 then it indicates str1 is less than str2.
    
-   if Return value > 0 then it indicates str2 is less than str1.
    
-   if Return value = 0 then it indicates str1 is equal to str2.
    

## Example

The following example shows the usage of memcmp() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str1[15];
   char str2[15];
   int ret;

   memcpy(str1, "abcdef", 6);
   memcpy(str2, "ABCDEF", 6);

   ret = memcmp(str1, str2, 5);

   if(ret > 0) {
      printf("str2 is less than str1");
   } else if(ret < 0) {
      printf("str1 is less than str2");
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


