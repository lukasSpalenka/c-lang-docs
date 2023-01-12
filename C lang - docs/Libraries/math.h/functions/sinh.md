---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []

author: 
---

# C library function - sinh()

> ## Excerpt
> C library function - sinh(),  The C library function double sinh(double x) returns the hyperbolic sine of x.

---
---

  

## Description

The C library function **double sinh(double x)** returns the hyperbolic sine of **x**.

## Declaration

Following is the declaration for sinh() function.

```c
double sinh(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns hyperbolic sine of x.

## Example

The following example shows the usage of sinh() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x, ret;
   x = 0.5;

   ret = sinh(x);
   printf("The hyperbolic sine of %lf is %lf degrees", x, ret);
   
   return(0);
}
```

Let us compile and run the above program, this will produce the following result −

```c
The hyperbolic sine of 0.500000 is 0.521095 degrees

```


