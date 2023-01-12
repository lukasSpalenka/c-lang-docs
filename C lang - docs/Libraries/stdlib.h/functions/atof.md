---
created: 2023-01-12T18:03:26 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_atof.htm
author: 
---

# C library function - atof()

> ## Excerpt
> C library function - atof(),  The C library function double atof(const char *str) converts the string argument str to a floating-point number (type double).

---
---

  

## Description

The C library function **double atof(const char \*str)** converts the string argument **str** to a floating-point number (type double).

## Declaration

Following is the declaration for atof() function.

```c
double atof(const char *str)
```

## Parameters

-   **str** − This is the string having the representation of a floating-point number.
    

## Return Value

This function returns the converted floating point number as a double value. If no valid conversion could be performed, it returns zero (0.0).

## Example

The following example shows the usage of atof() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
   float val;
   char str[20];
   
   strcpy(str, "98993489");
   val = atof(str);
   printf("String value = %s, Float value = %f\n", str, val);

   strcpy(str, "tutorialspoint.com");
   val = atof(str);
   printf("String value = %s, Float value = %f\n", str, val);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
String value = 98993489, Float value = 98993488.000000
String value = tutorialspoint.com, Float value = 0.000000

```


