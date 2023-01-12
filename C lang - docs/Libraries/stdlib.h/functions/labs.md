---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_labs.htm
author: 
---

# C library function - labs()

> ## Excerpt
> C library function - labs(),  The C library function long int labs(long int x) returns the absolute value of x.

---
---

  

## Description

The C library function **long int labs(long int x)** returns the absolute value of **x**.

## Declaration

Following is the declaration for labs() function.

```c
long int labs(long int x)
```

## Parameters

-   **x** − This is the integral value.
    

## Return Value

This function returns the absolute value of **x**.

## Example

The following example shows the usage of labs() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   long int a,b;

   a = labs(65987L);
   printf("Value of a = %ld\n", a);

   b = labs(-1005090L);
   printf("Value of b = %ld\n", b);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Value of a = 65987
Value of b = 1005090

```


