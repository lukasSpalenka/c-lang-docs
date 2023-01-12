---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_abort.htm
author: 
---

# C library function - abort()

> ## Excerpt
> C library function - abort(),  The C library function void abort(void) abort the program execution and comes out directly from the place of the call.

---
---

  

## Description

The C library function **void abort(void)** abort the program execution and comes out directly from the place of the call.

## Declaration

Following is the declaration for abort() function.

```c
void abort(void)
```

## Parameters

-   **NA**
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of abort() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   FILE *fp;
   
   printf("Going to open nofile.txt\n");
   fp = fopen( "nofile.txt","r" );
   if(fp == NULL) {
      printf("Going to abort the program\n");
      abort();
   }
   printf("Going to close nofile.txt\n");
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result when it tries to open **nofile.txt** file, which does not exist −

```c
Going to open nofile.txt                                                    
Going to abort the program                                                  
Aborted (core dumped)

```


