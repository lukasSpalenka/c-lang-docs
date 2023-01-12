---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strcpy.htm
author: 
---

# C library function - strcpy()

> ## Excerpt
> C library function - strcpy(),  The C library function char *strcpy(char *dest, const char *src) copies the string pointed to, by src to dest.

---
---

  

## Description

The C library function **char \*strcpy(char \*dest, const char \*src)** copies the string pointed to, by **src** to **dest**.

## Declaration

Following is the declaration for strcpy() function.

```c
char *strcpy(char *dest, const char *src)
```

## Parameters

-   **dest** − This is the pointer to the destination array where the content is to be copied.
    
-   **src** − This is the string to be copied.
    

## Return Value

This returns a pointer to the destination string dest.

## Example

The following example shows the usage of strcpy() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char src[40];
   char dest[100];
  
   memset(dest, '\0', sizeof(dest));
   strcpy(src, "This is tutorialspoint.com");
   strcpy(dest, src);

   printf("Final copied string : %s\n", dest);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Final copied string : This is tutorialspoint.com

```


