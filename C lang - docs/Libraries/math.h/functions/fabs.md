---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fabs.htm
author: 
---

# C library function - fabs()

> ## Excerpt
> C library function - fabs(),  The C library function double fabs(double x) returns the absolute value of x.

---
---

  

## Description

The C library function **double fabs(double x)** returns the absolute value of **x**.

## Declaration

Following is the declaration for fabs() function.

```c
double fabs(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns the absolute value of x.

## Example

The following example shows the usage of fabs() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   int a, b;
   a = 1234;
   b = -344;
  
   printf("The absolute value of %d is %lf\n", a, fabs(a));
   printf("The absolute value of %d is %lf\n", b, fabs(b));
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The absolute value of 1234 is 1234.000000
The absolute value of -344 is 344.000000

```


