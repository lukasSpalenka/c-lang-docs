---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_memset.htm
author: 
---

# C library function - memset()

> ## Excerpt
> C library function - memset(),  The C library function void *memset(void *str, int c, size_t n) copies the character c (an unsigned char) to the first n characters of the string pointed to, by

---
---

  

## Description

The C library function **void \*memset(void \*str, int c, size\_t n)** copies the character **c** (an unsigned char) to the first **n** characters of the string pointed to, by the argument **str**.

## Declaration

Following is the declaration for memset() function.

```c
void *memset(void *str, int c, size_t n)
```

## Parameters

-   **str** − This is a pointer to the block of memory to fill.
    
-   **c** − This is the value to be set. The value is passed as an int, but the function fills the block of memory using the unsigned char conversion of this value.
    
-   **n** − This is the number of bytes to be set to the value.
    

## Return Value

This function returns a pointer to the memory area str.

## Example

The following example shows the usage of memset() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str[50];

   strcpy(str,"This is string.h library function");
   puts(str);

   memset(str,'$',7);
   puts(str);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
This is string.h library function
$$$$$$$ string.h library function

```


