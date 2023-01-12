---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []

author: 
---

# C library function - cosh()

> ## Excerpt
> C library function - cosh(),  The C library function double cosh(double x) returns the hypebolic cosine of x.

---
---

  

## Description

The C library function **double cosh(double x)** returns the hypebolic cosine of **x**.

## Declaration

Following is the declaration for cosh() function.

```c
double cosh(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns hyperbolic cosine of x.

## Example

The following example shows the usage of cosh() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x;

   x = 0.5;
   printf("The hyperbolic cosine of %lf is %lf\n", x, cosh(x));

   x = 1.0;
   printf("The hyperbolic cosine of %lf is %lf\n", x, cosh(x));

   x = 1.5;
   printf("The hyperbolic cosine of %lf is %lf\n", x, cosh(x));

   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
The hyperbolic cosine of 0.500000 is 1.127626
The hyperbolic cosine of 1.000000 is 1.543081
The hyperbolic cosine of 1.500000 is 2.352410

```


