---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_exp.htm
author: 
---

# C library function - exp()

> ## Excerpt
> C library function - exp(),  The C library function double exp(double x) returns the value of e raised to the xth power.

---
---

  

## Description

The C library function **double exp(double x)** returns the value of **e** raised to the **xth** power.

## Declaration

Following is the declaration for exp() function.

```c
double exp(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the exponential value of x.

## Example

The following example shows the usage of exp() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x = 0;
  
   printf("The exponential value of %lf is %lf\n", x, exp(x));
   printf("The exponential value of %lf is %lf\n", x+1, exp(x+1));
   printf("The exponential value of %lf is %lf\n", x+2, exp(x+2));
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The exponential value of 0.000000 is 1.000000
The exponential value of 1.000000 is 2.718282
The exponential value of 2.000000 is 7.389056

```


