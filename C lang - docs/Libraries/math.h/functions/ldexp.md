---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_ldexp.htm
author: 
---

# C library function - ldexp()

> ## Excerpt
> C library function - ldexp(),  The C library function double ldexp(double x, int exponent) returns x multiplied by 2 raised to the power of exponent.

---
---

  

## Description

The C library function **double ldexp(double x, int exponent)** returns **x** multiplied by 2 raised to the power of **exponent**.

## Declaration

Following is the declaration for ldexp() function.

```c
double ldexp(double x, int exponent)
```

## Parameters

-   **x** − This is the floating point value representing the significand.
    
-   **exponent** − This is the value of the exponent.
    

## Return Value

This function returns x \* 2 <sup>exp</sup>

## Example

The following example shows the usage of ldexp() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x, ret;
   int n;

   x = 0.65;
   n = 3;
   ret = ldexp(x ,n);
   printf("%f * 2^%d = %f\n", x, n, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
0.650000 * 2^3 = 5.200000

```


