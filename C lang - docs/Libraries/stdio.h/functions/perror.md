---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_perror.htm
author: 
---

# C library function - perror()

> ## Excerpt
> C library function - perror(),  The C library function void perror(const char *str) prints a descriptive error message to stderr. First the string str is printed, followed by a colon then a sp

---
---

  

## Description

The C library function **void perror(const char \*str)** prints a descriptive error message to stderr. First the string **str** is printed, followed by a colon then a space.

## Declaration

Following is the declaration for perror() function.

```c
void perror(const char *str)
```

## Parameters

-   **str** − This is the C string containing a custom message to be printed before the error message itself.
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of perror() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;

   /* first rename if there is any file */
   rename("file.txt", "newfile.txt");

   /* now let's try to open same file */
   fp = fopen("file.txt", "r");
   if( fp == NULL ) {
      perror("Error: ");
      return(-1);
   }
   fclose(fp);
      
   return(0);
}
```

Let us compile and run the above program that will produce the following result because we are trying to open a file which does not exist −

```c
Error: : No such file or directory

```


