---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fclose.htm
author: 
---

# C library function - fclose()

> ## Excerpt
> C library function - fclose(),  The C library function int fclose(FILE *stream) closes the stream. All buffers are flushed.

---
---

  

## Description

The C library function **int fclose(FILE \*stream)** closes the stream. All buffers are flushed.

## Declaration

Following is the declaration for fclose() function.

```c
int fclose(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that specifies the stream to be closed.
    

## Return Value

This method returns zero if the stream is successfully closed. On failure, EOF is returned.

## Example

The following example shows the usage of fclose() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
 
   fp = fopen("file.txt", "w");

   fprintf(fp, "%s", "This is tutorialspoint.com");
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will create a file **file.txt**, and then it will write following text line and finally it will close the file using **fclose()** function.

```c
This is tutorialspoint.com

```


