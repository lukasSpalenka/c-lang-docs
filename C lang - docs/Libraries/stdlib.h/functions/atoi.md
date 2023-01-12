---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_atoi.htm
author: 
---

# C library function - atoi()

> ## Excerpt
> C library function - atoi(),  The C library function int atoi(const char *str) converts the string argument str to an integer (type int).

---
---

  

## Description

The C library function **int atoi(const char \*str)** converts the string argument **str** to an integer (type int).

## Declaration

Following is the declaration for atoi() function.

```c
int atoi(const char *str)
```

## Parameters

-   **str** − This is the string representation of an integral number.
    

## Return Value

This function returns the converted integral number as an int value. If no valid conversion could be performed, it returns zero.

## Example

The following example shows the usage of atoi() function.

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
   int val;
   char str[20];
   
   strcpy(str, "98993489");
   val = atoi(str);
   printf("String value = %s, Int value = %d\n", str, val);

   strcpy(str, "tutorialspoint.com");
   val = atoi(str);
   printf("String value = %s, Int value = %d\n", str, val);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
String value = 98993489, Int value = 98993489
String value = tutorialspoint.com, Int value = 0

```


