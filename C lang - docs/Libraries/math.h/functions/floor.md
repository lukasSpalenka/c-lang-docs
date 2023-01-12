---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_floor.htm
author: 
---

# C library function - floor()

> ## Excerpt
> C library function - floor(),  The C library function double floor(double x) returns the largest integer value less than or equal to x.

---
---

  

## Description

The C library function **double floor(double x)** returns the largest integer value less than or equal to **x**.

## Declaration

Following is the declaration for floor() function.

```c
double floor(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the largest integral value not greater than x.

## Example

The following example shows the usage of floor() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   float val1, val2, val3, val4;

   val1 = 1.6;
   val2 = 1.2;
   val3 = 2.8;
   val4 = 2.3;

   printf("Value1 = %.1lf\n", floor(val1));
   printf("Value2 = %.1lf\n", floor(val2));
   printf("Value3 = %.1lf\n", floor(val3));
   printf("Value4 = %.1lf\n", floor(val4));
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Value1 = 1.0
Value2 = 1.0
Value3 = 2.0
Value4 = 2.0

```


