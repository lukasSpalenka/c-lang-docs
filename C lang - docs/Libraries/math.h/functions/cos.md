---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_cos.htm
author: 
---

# C library function - cos()

> ## Excerpt
> C library function - cos(),  The C library function double cos(double x) returns the cosine of a radian angle x.

---
---

  

## Description

The C library function **double cos(double x)** returns the cosine of a radian angle **x**.

## Declaration

Following is the declaration for cos() function.

```c
double cos(double x)
```

## Parameters

-   **x** − This is the floating point value representing an angle expressed in radians.
    

## Return Value

This function returns the cosine of x.

## Example

The following example shows the usage of cos() function.

```c
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main () {
   double x, ret, val;

   x = 60.0;
   val = PI / 180.0;
   ret = cos( x*val );
   printf("The cosine of %lf is %lf degrees\n", x, ret);
   
   x = 90.0;
   val = PI / 180.0;
   ret = cos( x*val );
   printf("The cosine of %lf is %lf degrees\n", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The cosine of 60.000000 is 0.500000 degrees
The cosine of 90.000000 is 0.000000 degrees

```


