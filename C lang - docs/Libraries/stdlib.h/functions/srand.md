---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_srand.htm
author: 
---

# C library function - srand()

> ## Excerpt
> C library function - srand(),  The C library function void srand(unsigned int seed) seeds the random number generator used by the function rand.

---
---

  

## Description

The C library function **void srand(unsigned int seed)** seeds the random number generator used by the function **rand**.

## Declaration

Following is the declaration for srand() function.

```c
void srand(unsigned int seed)
```

## Parameters

-   **seed** − This is an integer value to be used as seed by the pseudo-random number generator algorithm.
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of srand() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main () {
   int i, n;
   time_t t;
   
   n = 5;
   
   /* Intializes random number generator */
   srand((unsigned) time(&t));

   /* Print 5 random numbers from 0 to 50 */
   for( i = 0 ; i < n ; i++ ) {
      printf("%d\n", rand() % 50);
   }
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
38
45
29
29
47

```


