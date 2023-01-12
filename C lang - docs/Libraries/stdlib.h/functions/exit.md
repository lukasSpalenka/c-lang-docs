---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_exit.htm
author: 
---

# C library function - exit()

> ## Excerpt
> C library function - exit(),  The C library function void exit(int status) terminates the calling process immediately. Any open file descriptors belonging to the process are closed and any c

---
---

  

## Description

The C library function **void exit(int status)** terminates the calling process immediately. Any open file descriptors belonging to the process are closed and any children of the process are inherited by process 1, init, and the process parent is sent a SIGCHLD signal.

## Declaration

Following is the declaration for exit() function.

```c
void exit(int status)
```

## Parameters

-   **status** − This is the status value returned to the parent process.
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of exit() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   printf("Start of the program....\n");
   
   printf("Exiting the program....\n");
   exit(0);

   printf("End of the program....\n");

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Start of the program....
Exiting the program....

```


