---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_ldiv.htm
author: 
---

# C library function - ldiv()

> ## Excerpt
> C library function - ldiv(),  The C library function div_t div(long int numer, long int denom) divides numer (numerator) by denom (denominator).

---
---

  

## Description

The C library function **div\_t div(long int numer, long int denom)** divides **numer (numerator)** by **denom (denominator)**.

## Declaration

Following is the declaration for ldiv() function.

```c
div_t div(long int numer, long int denom)
```

## Parameters

-   **numer** − This is the numerator.
    
-   **denom** − This is the denominator.
    

## Return Value

This function returns the value in a structure defined in <cstdlib>, which has two members. For ldiv\_t:_long quot; long rem;_

## Example

The following example shows the usage of ldiv() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   ldiv_t output;

   output = ldiv(100000L, 30000L);

   printf("Quotient = %ld\n", output.quot);

   printf("Remainder = %ld\n", output.rem);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Quotient = 3
Remainder = 10000

```


