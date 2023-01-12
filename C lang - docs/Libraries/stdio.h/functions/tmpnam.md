---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_tmpnam.htm
author: 
---

# C library function - tmpnam()

> ## Excerpt
> C library function - tmpnam(),  The C library function char *tmpnam(char *str) generates and returns a valid temporary filename which does not exist. If str is null then it simply returns the

---
---

  

## Description

The C library function **char \*tmpnam(char \*str)** generates and returns a valid temporary filename which does not exist. If **str** is null then it simply returns the tmp file name.

## Declaration

Following is the declaration for tmpnam() function.

```c
char *tmpnam(char *str)
```

## Parameters

-   **str** − This is the pointer to an array of chars where the proposed tempname will be stored as a C string.
    

## Return Value

-   Return value is a pointer to the C string containing the proposed name for a temporary file. If str was a null pointer, this points to an internal buffer that will be overwritten the next time this function is called.
    
-   If str was not a null pointer, str is returned. If the function fails to create a suitable filename, it returns a null pointer.
    

## Example

The following example shows the usage of tmpnam() function.

```c
#include <stdio.h>

int main () {
   char buffer[L_tmpnam];
   char *ptr;

   tmpnam(buffer);
   printf("Temporary name 1: %s\n", buffer);
 
   ptr = tmpnam(NULL);
   printf("Temporary name 2: %s\n", ptr);

   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
Temporary name 1: /tmp/filebaalTb
Temporary name 2: /tmp/filedCIbb0

```


