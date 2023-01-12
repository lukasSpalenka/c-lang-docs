---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_ftell.htm
author: 
---

# C library function - ftell()

> ## Excerpt
> C library function - ftell(),  The C library function long int ftell(FILE *stream) returns the current file position of the given stream.

---
---

  

## Description

The C library function **long int ftell(FILE \*stream)** returns the current file position of the given stream.

## Declaration

Following is the declaration for ftell() function.

```c
long int ftell(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    

## Return Value

This function returns the current value of the position indicator. If an error occurs, -1L is returned, and the global variable errno is set to a positive value.

## Example

The following example shows the usage of ftell() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int len;

   fp = fopen("file.txt", "r");
   if( fp == NULL )  {
      perror ("Error opening file");
      return(-1);
   }
   fseek(fp, 0, SEEK_END);

   len = ftell(fp);
   fclose(fp);

   printf("Total size of file.txt = %d bytes\n", len);
  
   return(0);
}
```

Let us assume we have a text file **file.txt**, which has the following content −

```c
This is tutorialspoint.com
```

Now let us compile and run the above program that will produce the following result if file has above mentioned content otherwise it will give different result based on the file content −

```c
Total size of file.txt = 26 bytes

```


