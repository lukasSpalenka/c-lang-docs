---
created: 2023-01-12T17:57:22 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_modf.htm
author: 
---

# C library function - modf()

> ## Excerpt
> C library function - modf(),  The C library function double modf(double x, double *integer) returns the fraction component (part after the decimal), and sets integer to the integer component

---
---

  

## Description

The C library function **double modf(double x, double \*integer)** returns the fraction component (part after the decimal), and sets integer to the integer component.

## Declaration

Following is the declaration for modf() function.

```c
double modf(double x, double *integer)
```

## Parameters

-   **x** − This is the floating point value.
    
-   **integer** − This is the pointer to an object where the integral part is to be stored.
    

## Return Value

This function returns the fractional part of x, with the same sign.

## Example

The following example shows the usage of modf() function.

```c
#include<stdio.h>
#include<math.h>

int main () {
   double x, fractpart, intpart;

   x = 8.123456;
   fractpart = modf(x, &intpart);

   printf("Integral part = %lf\n", intpart);
   printf("Fraction Part = %lf \n", fractpart);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Integral part = 8.000000
Fraction Part = 0.123456 

```


