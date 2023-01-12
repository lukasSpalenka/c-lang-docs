---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_acos.htm
author: 
---

# C library function - acos()

> ## Excerpt
> C library function - acos(),  The C library function double acos(double x) returns the arc cosine of x in radians.

---
---

  

## Description

The C library function **double acos(double x)** returns the arc cosine of **x** in radians.

## Declaration

Following is the declaration for acos() function.

```c
double acos(double x)
```

## Parameters

-   **x** − This is the floating point value in the interval \[-1,+1\].
    

## Return Value

This function returns principal arc cosine of x, in the interval \[0, pi\] radians.

## Example

The following example shows the usage of acos() function.

```c
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main () {
   double x, ret, val;

   x = 0.9;
   val = 180.0 / PI;

   ret = acos(x) * val;
   printf("The arc cosine of %lf is %lf degrees", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The arc cosine of 0.900000 is 25.855040 degrees

```


