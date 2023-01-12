---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_free.htm
author: 
---

# C library function - free()

> ## Excerpt
> C library function - free(),  The C library function void free(void *ptr) deallocates the memory previously allocated by a call to calloc, malloc, or realloc.

---
---

  

## Description

The C library function **void free(void \*ptr)** deallocates the memory previously allocated by a call to calloc, malloc, or realloc.

## Declaration

Following is the declaration for free() function.

```c
void free(void *ptr)
```

## Parameters

-   **ptr** − This is the pointer to a memory block previously allocated with malloc, calloc or realloc to be deallocated. If a null pointer is passed as argument, no action occurs.
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of free() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

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

   /* Deallocate allocated memory */
   free(str);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
String = tutorialspoint, Address = 355090448
String = tutorialspoint.com, Address = 355090448

```


