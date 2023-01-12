---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strtoul.htm
author: 
---

# C library function - strtoul()

> ## Excerpt
> C library function - strtoul(),  The C library function unsigned long int strtoul(const char *str, char **endptr, int base) function converts the initial part of the string in str to an unsigne

---
---

  

## Description

The C library function **unsigned long int strtoul(const char \*str, char \*\*endptr, int base)** function converts the initial part of the string in **str** to an unsigned long int value according to the given **base**, which must be between 2 and 36 inclusive, or be the special value 0.

## Declaration

Following is the declaration for strtoul() function.

```c
unsigned long int strtoul(const char *str, char **endptr, int base)
```

## Parameters

-   **str** − This is the string containing the representation of an unsigned integral number.
    
-   **endptr** − This is the reference to an object of type char\*, whose value is set by the function to the next character in str after the numerical value.
    
-   **base** − This is the base, which must be between 2 and 36 inclusive, or be the special value 0.
    

## Return Value

This function returns the converted integral number as a long int value. If no valid conversion could be performed, a zero value is returned.

## Example

The following example shows the usage of strtoul() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   char str[30] = "2030300 This is test";
   char *ptr;
   long ret;

   ret = strtoul(str, &ptr, 10);
   printf("The number(unsigned long integer) is %lu\n", ret);
   printf("String part is |%s|", ptr);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
The number(unsigned long integer) is 2030300
String part is | This is test|

```


