---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_atan2.htm
author: 
---

# C library function - atan2()

> ## Excerpt
> C library function - atan2(),  The C library function double atan2(double y, double x) returns the arc tangent in radians of y/x based on the signs of both values to determine the correct qua

---
---

  

## Description

The C library function **double atan2(double y, double x)** returns the arc tangent in radians of **y/x** based on the signs of both values to determine the correct quadrant.

## Declaration

Following is the declaration for atan2() function.

```c
double atan2(double y, double x)
```

## Parameters

-   **x** − This is the floating point value representing an x-coordinate.
    
-   **y** − This is the floating point value representing a y-coordinate.
    

## Return Value

This function returns the principal arc tangent of y/x, in the interval \[-pi,+pi\] radians.

## Example

The following example shows the usage of atan2() function.

```c
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main () {
   double x, y, ret, val;

   x = -7.0;
   y = 7.0;
   val = 180.0 / PI;

   ret = atan2 (y,x) * val;
   printf("The arc tangent of x = %lf, y = %lf ", x, y);
   printf("is %lf degrees\n", ret);
  
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The arc tangent of x = -7.000000, y = 7.000000 is 135.000000 degrees

```


