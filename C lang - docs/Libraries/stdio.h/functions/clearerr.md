---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_clearerr.htm
author: 
---

# C library function - clearerr()

> ## Excerpt
> C library function - clearerr(),  The C library function void clearerr(FILE *stream) clears the end-of-file and error indicators for the given stream.

---
---

  

## Description

The C library function **void clearerr(FILE \*stream)** clears the end-of-file and error indicators for the given stream.

## Declaration

Following is the declaration for clearerr() function.

```c
void clearerr(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    

## Return Value

This should not fail and do not set the external variable errno but in case it detects that its argument is not a valid stream, it must return -1 and set errno to EBADF.

## Example

The following example shows the usage of clearerr() function.

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

Assuming we have a text file **file.txt**, which is an empty file, let us compile and run the above program, this will produce the following result because we try to read a file which we opened in write only mode.

```c
Error reading from file "file.txt"

```


