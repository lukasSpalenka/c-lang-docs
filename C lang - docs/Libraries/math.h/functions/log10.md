---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_log10.htm
author: 
---

# C library function - log10()

> ## Excerpt
> C library function - log10(),  The C library function double log10(double x) returns the common logarithm (base-10 logarithm) of x.

---
---

  

## Description

The C library function **double log10(double x)** returns the common logarithm (base-10 logarithm) of **x**.

## Declaration

Following is the declaration for log10() function.

```c
double log10(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the common logarithm of x, for values of x greater than zero.

## Example

The following example shows the usage of log10() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x, ret;
   x = 10000;
  
   /* finding value of log1010000 */
   ret = log10(x);
   printf("log10(%lf) = %lf\n", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
log10(10000.000000) = 4.000000

```


