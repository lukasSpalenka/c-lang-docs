---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_ferror.htm
author: 
---

# C library function - ferror()

> ## Excerpt
> C library function - ferror(),  The C library function int ferror(FILE *stream) tests the error indicator for the given stream.

---
---

  

## Description

The C library function **int ferror(FILE \*stream)** tests the error indicator for the given stream.

## Declaration

Following is the declaration for ferror() function.

```c
int ferror(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    

## Return Value

If the error indicator associated with the stream was set, the function returns a non-zero value else, it returns a zero value.

## Example

The following example shows the usage of ferror() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   char c;

   fp = fopen("file.txt", "w");

   c = fgetc(fp);
   if( ferror(fp) ) {
      printf("Error in reading from file : file.txt\n");
   }
   clearerr(fp);
   
   if( ferror(fp) ) {
      printf("Error in reading from file : file.txt\n");
   }
   fclose(fp);

   return(0);
}
```

Assuming we have a text file **file.txt**, which is an empty file. Let us compile and run the above program that will produce the following result because we try to read a file which we opened in **write only** mode.

```c
Error reading from file "file.txt"

```


