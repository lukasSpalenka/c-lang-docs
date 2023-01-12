---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_frexp.htm
author: 
---

# C library function - frexp()

> ## Excerpt
> C library function - frexp(),  The C library function double frexp(double x, int *exponent) return value is the mantissa, and the integer pointed to by exponent is the exponent. The resultant

---
---

  

## Description

The C library function **double frexp(double x, int \*exponent)** return value is the mantissa, and the integer pointed to by **exponent** is the exponent. The resultant value is **x = mantissa \* 2 ^ exponent**.

## Declaration

Following is the declaration for frexp() function.

```c
double frexp(double x, int *exponent)
```

## Parameters

-   **x** − This is the floating point value to be computed.
    
-   **exponent** − This is the pointer to an **int** object where the value of the exponent is to be stored.
    

## Return Value

This function returns the normalized fraction. If the argument x is not zero, the normalized fraction is **x** times a power of two, and its absolute value is always in the range 1/2 (inclusive) to 1 (exclusive). If **x** is zero, then the normalized fraction is zero and zero is stored in exp.

## Example

The following example shows the usage of frexp() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x = 1024, fraction;
   int e;
   
   fraction = frexp(x, &e);
   printf("x = %.2lf = %.2lf * 2^%d\n", x, fraction, e);
   
   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
x = 1024.00 = 0.50 * 2^11

```


