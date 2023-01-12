---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_tmpfile.htm
author: 
---

# C library function - tmpfile()

> ## Excerpt
> C library function - tmpfile(),  The C library function FILE *tmpfile(void) creates a temporary file in binary update mode (wb+). The temporary file created is automatically deleted when the st

---
---

  

## Description

The C library function **FILE \*tmpfile(void)** creates a temporary file in binary update mode (wb+). The temporary file created is automatically deleted when the stream is closed (fclose) or when the program terminates.

## Declaration

Following is the declaration for tmpfile() function.

```c
FILE *tmpfile(void)
```

## Parameters

-   **NA**
    

## Return Value

If successful, the function returns a stream pointer to the temporary file created. If the file cannot be created, then NULL is returned.

## Example

The following example shows the usage of tmpfile() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;

   fp = tmpfile();
   printf("Temporary file created\n");

   /* you can use tmp file here */

   fclose(fp);

   return(0);
}
```

Let us compile and run the above program to create a temporary file in /tmp folder but once your program is out, it will be deleted automatically and the program will produce the following result −

```c
Temporary file created

```


