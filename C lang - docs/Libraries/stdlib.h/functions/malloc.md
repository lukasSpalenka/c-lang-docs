---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_malloc.htm
author: 
---

# C library function - malloc()

> ## Excerpt
> C library function - malloc(),  The C library function void *malloc(size_t size) allocates the requested memory and returns a pointer to it.

---
---

  

## Description

The C library function **void \*malloc(size\_t size)** allocates the requested memory and returns a pointer to it.

## Declaration

Following is the declaration for malloc() function.

```c
void *malloc(size_t size)
```

## Parameters

-   **size** − This is the size of the memory block, in bytes.
    

## Return Value

This function returns a pointer to the allocated memory, or NULL if the request fails.

## Example

The following example shows the usage of malloc() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   char *str;

   /* Initial memory allocation */
   str = (char *) malloc(15);
   strcpy(str, "tutorialspoint");
   printf("String = %s,  Address = %u\n", str, str);

   /* Reallocating memory */
   str = (char *) realloc(str, 25);
   strcat(str, ".com");
   printf("String = %s,  Address = %u\n", str, str);

   free(str);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
String = tutorialspoint, Address = 355090448
String = tutorialspoint.com, Address = 355090448

```


