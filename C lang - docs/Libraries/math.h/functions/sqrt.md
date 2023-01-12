---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_sqrt.htm
author: 
---

# C library function - sqrt()

> ## Excerpt
> C library function - sqrt(),  The C library function double sqrt(double x) returns the square root of x.

---
---

  

## Description

The C library function **double sqrt(double x)** returns the square root of **x**.

## Declaration

Following is the declaration for sqrt() function.

```c
double sqrt(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the square root of x.

## Example

The following example shows the usage of sqrt() function.

```c
#include <stdio.h>
#include <math.h>

int main () {

   printf("Square root of %lf is %lf\n", 4.0, sqrt(4.0) );
   printf("Square root of %lf is %lf\n", 5.0, sqrt(5.0) );
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Square root of 4.000000 is 2.000000
Square root of 5.000000 is 2.236068

```


