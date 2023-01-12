---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_div.htm
author: 
---

# C library function - div()

> ## Excerpt
> C library function - div(),  The C library function div_t div(int numer, int denom) divides numer (numerator) by denom (denominator).

---
---

  

## Description

The C library function **div\_t div(int numer, int denom)** divides **numer (numerator)** by **denom (denominator)**.

## Declaration

Following is the declaration for div() function.

```c
div_t div(int numer, int denom)
```

## Parameters

-   **numer** − This is the numerator.
    
-   **denom** − This is the denominator.
    

## Return Value

This function returns the value in a structure defined in <cstdlib>, which has two members. For div\_t:_int quot; int rem;_

## Example

The following example shows the usage of div() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   div_t output;

   output = div(27, 4);
   printf("Quotient part of (27/ 4) = %d\n", output.quot);
   printf("Remainder part of (27/4) = %d\n", output.rem);

   output = div(27, 3);
   printf("Quotient part of (27/ 3) = %d\n", output.quot);
   printf("Remainder part of (27/3) = %d\n", output.rem);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Quotient part of (27/ 4) = 6
Remainder part of (27/4) = 3
Quotient part of (27/ 3) = 9
Remainder part of (27/3) = 0

```


