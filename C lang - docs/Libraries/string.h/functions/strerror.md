---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strerror.htm
author: 
---

# C library function - strerror()

> ## Excerpt
> C library function - strerror(),  The C library function char *strerror(int errnum) searches an internal array for the error number errnum and returns a pointer to an error message string. The e

---
---

  

## Description

The C library function **char \*strerror(int errnum)** searches an internal array for the error number **errnum** and returns a pointer to an error message string. The error strings produced by **strerror** depend on the developing platform and compiler.

## Declaration

Following is the declaration for strerror() function.

```c
char *strerror(int errnum)
```

## Parameters

-   **errnum** − This is the error number, usually **errno**.
    

## Return Value

This function returns a pointer to the error string describing error errnum.

## Example

The following example shows the usage of strerror() function.

```c
#include <stdio.h>
#include <string.h>
#include <errno.h>

int main () {
   FILE *fp;

   fp = fopen("file.txt","r");
   if( fp == NULL ) {
      printf("Error: %s\n", strerror(errno));
   }
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result because we are trying to open a file which does not exist −

```c
Error: No such file or directory

```


