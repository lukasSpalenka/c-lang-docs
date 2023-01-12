---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_sin.htm
author: 
---

# C library function - sin()

> ## Excerpt
> C library function - sin(),  The C library function double sin(double x) returns the sine of a radian angle x.

---
---

  

## Description

The C library function **double sin(double x)** returns the sine of a radian angle **x**.

## Declaration

Following is the declaration for sin() function.

```c
double sin(double x)
```

## Parameters

-   **x** − This is the floating point value representing an angle expressed in radians.
    

## Return Value

This function returns sine of x.

## Example

The following example shows the usage of sin() function.

```c
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main () {
   double x, ret, val;

   x = 45.0;
   val = PI / 180;
   ret = sin(x*val);
   printf("The sine of %lf is %lf degrees", x, ret);
   
   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
The sine of 45.000000 degrees is 0.707107

```


