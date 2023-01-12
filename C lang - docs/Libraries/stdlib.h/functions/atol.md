---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_atol.htm
author: 
---

# C library function - atol()

> ## Excerpt
> C library function - atol(),  The C library function long int atol(const char *str) converts the string argument str to a long integer (type long int).

---
---

  

## Description

The C library function **long int atol(const char \*str)** converts the string argument **str** to a long integer (type long int).

## Declaration

Following is the declaration for atol() function.

```c
long int atol(const char *str)
```

## Parameters

-   **str** − This is the string containing the representation of an integral number.
    

## Return Value

This function returns the converted integral number as a long int. If no valid conversion could be performed, it returns zero.

## Example

The following example shows the usage of atol() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
   long val;
   char str[20];
   
   strcpy(str, "98993489");
   val = atol(str);
   printf("String value = %s, Long value = %ld\n", str, val);

   strcpy(str, "tutorialspoint.com");
   val = atol(str);
   printf("String value = %s, Long value = %ld\n", str, val);

   return(0);
}
```

Let us compile and run the above program, this will produce the following result −

```c
String value = 98993489, Long value = 98993489
String value = tutorialspoint.com, Long value = 0

```


