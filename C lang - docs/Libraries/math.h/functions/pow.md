---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_pow.htm
author: 
---

# C library function - pow()

> ## Excerpt
> C library function - pow(),  The C library function double pow(double x, double y) returns x raised to the power of y i.e. xy.

---
---

  

## Description

The C library function **double pow(double x, double y)** returns **x** raised to the power of **y** i.e. x<sup>y</sup>.

## Declaration

Following is the declaration for pow() function.

```c
double pow(double x, double y)
```

## Parameters

-   **x** − This is the floating point base value.
    
-   **y** − This is the floating point power value.
    

## Return Value

This function returns the result of raising **x** to the power **y**.

## Example

The following example shows the usage of pow() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   printf("Value 8.0 ^ 3 = %lf\n", pow(8.0, 3));

   printf("Value 3.05 ^ 1.98 = %lf", pow(3.05, 1.98));
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Value 8.0 ^ 3 = 512.000000
Value 3.05 ^ 1.98 = 9.097324

```


