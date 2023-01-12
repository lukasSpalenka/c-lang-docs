---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strtod.htm
author: 
---

# C library function - strtod()

> ## Excerpt
> C library function - strtod(),  The C library function double strtod(const char *str, char **endptr) converts the string pointed to by the argument str to a floating-point number (type double)

---
---

  

## Description

The C library function **double strtod(const char \*str, char \*\*endptr)** converts the string pointed to by the argument **str** to a floating-point number (type double). If **endptr** is not NULL, a pointer to the character after the last character used in the conversion is stored in the location referenced by endptr.

## Declaration

Following is the declaration for strtod() function.

```c
double strtod(const char *str, char **endptr)
```

## Parameters

-   **str** − This is the value to be converted to a string.
    
-   **endptr** − This is the reference to an already allocated object of type char\*, whose value is set by the function to the next character in _str_ after the numerical value.
    

## Return Value

This function returns the converted floating point number as a double value, else zero value (0.0) is returned.

## Example

The following example shows the usage of strtod() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () { 
   char str[30] = "20.30300 This is test";
   char *ptr;
   double ret;

   ret = strtod(str, &ptr);
   printf("The number(double) is %lf\n", ret);
   printf("String part is |%s|", ptr);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The number(double) is 20.303000
String part is | This is test|

```


