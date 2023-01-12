---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_abs.htm
author: 
---

# C library function - abs()

> ## Excerpt
> C library function - abs(),  The C library function int abs(int x) returns the absolute value of int x.

---
---

  

## Description

The C library function **int abs(int x)** returns the absolute value of **int x**.

## Declaration

Following is the declaration for abs() function.

```c
int abs(int x)
```

## Parameters

-   **x** − This is the integral value.
    

## Return Value

This function returns the absolute value of x.

## Example

The following example shows the usage of abs() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   int a, b;

   a = abs(5);
   printf("value of a = %d\n", a);

   b = abs(-10);
   printf("value of b = %d\n", b);
   
   return(0);
}
```

Let us compile and run the above program, this will produce the following result −

```c
value of a = 5
value of b = 10

```


