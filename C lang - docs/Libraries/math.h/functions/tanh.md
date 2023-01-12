---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []

author: 
---

# C library function - tanh()

> ## Excerpt
> C library function - tanh(),  The C library function double tanh(double x) returns the hyperbolic tangent of x.

---
---

  

## Description

The C library function **double tanh(double x)** returns the hyperbolic tangent of **x**.

## Declaration

Following is the declaration for tanh() function.

```c
double tanh(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns hyperbolic tangent of x.

## Example

The following example shows the usage of tanh() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x, ret;
   x = 0.5;

   ret = tanh(x);
   printf("The hyperbolic tangent of %lf is %lf degrees", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The hyperbolic tangent of 0.500000 is 0.462117 degrees

```


