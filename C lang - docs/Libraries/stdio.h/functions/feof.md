---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_feof.htm
author: 
---

# C library function - feof()

> ## Excerpt
> C library function - feof(),  The C library function int feof(FILE *stream) tests the end-of-file indicator for the given stream.

---
---

  

## Description

The C library function **int feof(FILE \*stream)** tests the end-of-file indicator for the given stream.

## Declaration

Following is the declaration for feof() function.

```c
int feof(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    

## Return Value

This function returns a non-zero value when End-of-File indicator associated with the stream is set, else zero is returned.

## Example

The following example shows the usage of feof() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int c;
  
   fp = fopen("file.txt","r");
   if(fp == NULL) {
      perror("Error in opening file");
      return(-1);
   }
   
   while(1) {
      c = fgetc(fp);
      if( feof(fp) ) { 
         break ;
      }
      printf("%c", c);
   }
   fclose(fp);
   
   return(0);
}
```

Assuming we have a text file **file.txt**, which has the following content. This file will be used as an input for our example program −

```c
This is tutorialspoint.com

```

Let us compile and run the above program, this will produce the following result −

```c
This is tutorialspoint.com

```


