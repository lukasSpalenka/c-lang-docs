---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fgetc.htm
author: 
---

# C library function - fgetc()

> ## Excerpt
> C library function - fgetc(),  The C library function int fgetc(FILE *stream) gets the next character (an unsigned char) from the specified stream and advances the position indicator for the

---
---

  

## Description

The C library function **int fgetc(FILE \*stream)** gets the next character (an unsigned char) from the specified stream and advances the position indicator for the stream.

## Declaration

Following is the declaration for fgetc() function.

```c
int fgetc(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream on which the operation is to be performed.
    

## Return Value

This function returns the character read as an unsigned char cast to an int or EOF on end of file or error.

## Example

The following example shows the usage of fgetc() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int c;
   int n = 0;
  
   fp = fopen("file.txt","r");
   if(fp == NULL) {
      perror("Error in opening file");
      return(-1);
   } do {
      c = fgetc(fp);
      if( feof(fp) ) {
         break ;
      }
      printf("%c", c);
   } while(1);

   fclose(fp);
   return(0);
}
```

Let us assume, we have a text file **file.txt**, which has the following content. This file will be used as an input for our example program −

```c
We are in 2012
```

Now, let us compile and run the above program that will produce the following result −

```c
We are in 2012

```


