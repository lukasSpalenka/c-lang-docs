---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fmod.htm
author: 
---

# C library function - fmod()

> ## Excerpt
> C library function - fmod(),  The C library function double fmod(double x, double y) returns the remainder of x divided by y.

---
---

  

## Description

The C library function **double fmod(double x, double y)** returns the remainder of **x** divided by **y**.

## Declaration

Following is the declaration for fmod() function.

```c
double fmod(double x, double y)
```

## Parameters

-   **x** − This is the floating point value with the division numerator i.e. x.
    
-   **y** − This is the floating point value with the division denominator i.e. y.
    

## Return Value

This function returns the remainder of dividing x/y.

## Example

The following example shows the usage of fmod() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   float a, b;
   int c;
   a = 9.2;
   b = 3.7;
   c = 2;
   printf("Remainder of %f / %d is %lf\n", a, c, fmod(a,c));
   printf("Remainder of %f / %f is %lf\n", a, b, fmod(a,b));
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Remainder of 9.200000 / 2 is 1.200000
Remainder of 9.200000 / 3.700000 is 1.800000

```


