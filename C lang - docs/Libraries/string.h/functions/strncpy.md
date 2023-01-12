---
created: 2023-01-12T17:59:48 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_strncpy.htm
author: 
---

# C library function - strncpy()

> ## Excerpt
> C library function - strncpy(),  The C library function char *strncpy(char *dest, const char *src, size_t n) copies up to n characters from the string pointed to, by src to dest. In a case wher

---
---

  

## Description

The C library function **char \*strncpy(char \*dest, const char \*src, size\_t n)** copies up to **n** characters from the string pointed to, by **src** to **dest**. In a case where the length of src is less than that of n, the remainder of dest will be padded with null bytes.

## Declaration

Following is the declaration for strncpy() function.

```c
char *strncpy(char *dest, const char *src, size_t n)
```

## Parameters

-   **dest** − This is the pointer to the destination array where the content is to be copied.
    
-   **src** − This is the string to be copied.
    
-   **n** − The number of characters to be copied from source.
    

## Return Value

This function returns the pointer to the copied string.

## Example

The following example shows the usage of strncpy() function. Here we have used function memset() to clear the memory location.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char src[40];
   char dest[12];
  
   memset(dest, '\0', sizeof(dest));
   strcpy(src, "This is tutorialspoint.com");
   strncpy(dest, src, 10);

   printf("Final copied string : %s\n", dest);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Final copied string : This is tu

```


