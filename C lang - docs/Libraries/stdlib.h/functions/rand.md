---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_rand.htm
author: 
---

# C library function - rand()

> ## Excerpt
> C library function - rand(),  The C library function int rand(void) returns a pseudo-random number in the range of 0 to RAND_MAX.

---
---

  

## Description

The C library function **int rand(void)** returns a pseudo-random number in the range of 0 to _RAND\_MAX_.

RAND\_MAX is a constant whose default value may vary between implementations but it is granted to be at least 32767.

## Declaration

Following is the declaration for rand() function.

```c
int rand(void)
```

## Parameters

-   **NA**
    

## Return Value

This function returns an integer value between 0 and RAND\_MAX.

## Example

The following example shows the usage of rand() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   int i, n;
   time_t t;
   
   n = 5;
   
   /* Intializes random number generator */
   srand((unsigned) time(&t));

   /* Print 5 random numbers from 0 to 49 */
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


