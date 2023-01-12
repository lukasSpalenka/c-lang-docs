---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strtol.htm
author: 
---

# C library function - strtol()

> ## Excerpt
> C library function - strtol(),  The C library function long int strtol(const char *str, char **endptr, int base) converts the initial part of the string in str to a long int value according to

---
---

  

## Description

The C library function **long int strtol(const char \*str, char \*\*endptr, int base)** converts the initial part of the string in **str** to a **long int** value according to the given **base**, which must be between 2 and 36 inclusive, or be the special value 0.

## Declaration

Following is the declaration for strtol() function.

```c
long int strtol(const char *str, char **endptr, int base)
```

## Parameters

-   **str** − This is the string containing the representation of an integral number.
    
-   **endptr** − This is the reference to an object of type char\*, whose value is set by the function to the next character in _str_ after the numerical value.
    
-   **base** − This is the base, which must be between 2 and 36 inclusive, or be the special value 0.
    

## Return Value

This function returns the converted integral number as a long int value, else zero value is returned.

## Example

The following example shows the usage of strtol() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   char str[30] = "2030300 This is test";
   char *ptr;
   long ret;

   ret = strtol(str, &ptr, 10);
   printf("The number(unsigned long integer) is %ld\n", ret);
   printf("String part is |%s|", ptr);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The number(unsigned long integer) is 2030300
String part is | This is test|

```


