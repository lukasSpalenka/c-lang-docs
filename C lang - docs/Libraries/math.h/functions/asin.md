---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_asin.htm
author: 
---

# C library function - asin()

> ## Excerpt
> C library function - asin(),  The C library function double asin(double x) returns the arc sine of x in radians.

---
---

  

## Description

The C library function **double asin(double x)** returns the arc sine of **x** in radians.

## Declaration

Following is the declaration for asin() function.

```c
double asin(double x)
```

## Parameters

-   **x** − This is the floating point value in the interval \[-1,+1\].
    

## Return Value

This function returns the arc sine of x, in the interval \[-pi/2,+pi/2\] radians.

## Example

The following example shows the usage of asin() function.

```c
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main () {
   double x, ret, val;
   x = 0.9;
   val = 180.0 / PI;

   ret = asin(x) * val;
   printf("The arc sine of %lf is %lf degrees", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The arc sine of 0.900000 is 64.158067 degrees

```


