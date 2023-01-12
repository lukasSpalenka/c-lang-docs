---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_ceil.htm
author: 
---

# C library function - ceil()

> ## Excerpt
> C library function - ceil(),  The C library function double ceil(double x) returns the smallest integer value greater than or equal to x.

---
---

  

## Description

The C library function **double ceil(double x)** returns the smallest integer value greater than or equal to **x**.

## Declaration

Following is the declaration for ceil() function.

```c
double ceil(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the smallest integral value not less than **x**.

## Example

The following example shows the usage of ceil() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   float val1, val2, val3, val4;

   val1 = 1.6;
   val2 = 1.2;
   val3 = 2.8;
   val4 = 2.3;

   printf ("value1 = %.1lf\n", ceil(val1));
   printf ("value2 = %.1lf\n", ceil(val2));
   printf ("value3 = %.1lf\n", ceil(val3));
   printf ("value4 = %.1lf\n", ceil(val4));
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
value1 = 2.0
value2 = 2.0
value3 = 3.0
value4 = 3.0

```


