---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strcoll.htm
author: 
---

# C library function - strcoll()

> ## Excerpt
> C library function - strcoll(),  The C library function int strcoll(const char *str1, const char *str2) compares string str1 to str2. The result is dependent on the LC_COLLATE setting of the lo

---
---

  

## Description

The C library function **int strcoll(const char \*str1, const char \*str2)** compares string **str1** to **str2**. The result is dependent on the LC\_COLLATE setting of the location.

## Declaration

Following is the declaration for strcoll() function.

```c
int strcoll(const char *str1, const char *str2)
```

## Parameters

-   **str1** − This is the first string to be compared.
    
-   **str2** − This is the second string to be compared.
    

## Return Value

This function return values that are as follows −

-   if Return value < 0 then it indicates str1 is less than str2.
-   if Return value > 0 then it indicates str2 is less than str1.
-   if Return value = 0 then it indicates str1 is equal to str2.

## Example

The following example shows the usage of strcoll() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char str1[15];
   char str2[15];
   int ret;

   strcpy(str1, "abc");
   strcpy(str2, "ABC");

   ret = strcoll(str1, str2);

   if(ret > 0) {
      printf("str1 is less than str2");
   } else if(ret < 0) {
      printf("str2 is less than str1");
   } else {
      printf("str1 is equal to str2");
   }
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
str1 is less than str2

```


