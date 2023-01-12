---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_atan.htm
author: 
---

# C library function - atan()

> ## Excerpt
> C library function - atan(),  The C library function double atan(double x) returns the arc tangent of x in radians.

---
---

  

## Description

The C library function **double atan(double x)** returns the arc tangent of **x** in radians.

## Declaration

Following is the declaration for atan() function.

```c
double atan(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the principal arc tangent of x, in the interval \[-pi/2,+pi/2\] radians.

## Example

The following example shows the usage of atan() function.

```c
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main () {
   double x, ret, val;
   x = 1.0;
   val = 180.0 / PI;

   ret = atan (x) * val;
   printf("The arc tangent of %lf is %lf degrees", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The arc tangent of 1.000000 is 45.000000 degrees

```


