---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_log.htm
author: 
---

# C library function - log()

> ## Excerpt
> C library function - log(),  The C library function double log(double x) returns the natural logarithm (base-e logarithm) of x.

---
---

  

## Description

The C library function **double log(double x)** returns the natural logarithm (base-e logarithm) of **x**.

## Declaration

Following is the declaration for log() function.

```c
double log(double x)
```

## Parameters

-   **x** − This is the floating point value.
    

## Return Value

This function returns natural logarithm of x.

## Example

The following example shows the usage of log() function.

```c
#include <stdio.h>
#include <math.h>

int main () {
   double x, ret;
   x = 2.7;

   /* finding log(2.7) */
   ret = log(x);
   printf("log(%lf) = %lf", x, ret);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
log(2.700000) = 0.993252

```


