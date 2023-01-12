---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_atexit.htm
author: 
---

# C library function - atexit()

> ## Excerpt
> C library function - atexit(),  The C library function int atexit(void (*func)(void)) causes the specified function func to be called when the program terminates. You can register your termina

---
---

  

## Description

The C library function **int atexit(void (\*func)(void))** causes the specified function **func** to be called when the program terminates. You can register your termination function anywhere you like, but it will be called at the time of the program termination.

## Declaration

Following is the declaration for atexit() function.

```c
int atexit(void (*func)(void))
```

## Parameters

-   **func** − This is the function to be called at the termination of the program.
    

## Return Value

This function returns a zero value if the function is registered successfully, otherwise a non-zero value is returned if it is failed.

## Example

The following example shows the usage of atexit() function.

```c
#include <stdio.h>
#include <stdlib.h>

void functionA () {
   printf("This is functionA\n");
}

int main () {
   /* register the termination function */
   atexit(functionA );
   
   printf("Starting  main program...\n");

   printf("Exiting main program...\n");

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Starting main program...
Exiting main program...
This is functionA

```


