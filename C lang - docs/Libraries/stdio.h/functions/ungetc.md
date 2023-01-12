---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_ungetc.htm
author: 
---

# C library function - ungetc()

> ## Excerpt
> C library function - ungetc(),  The C library function int ungetc(int char, FILE *stream) pushes the character char (an unsigned char) onto the specified stream so that the this is available f

---
---

  

## Description

The C library function **int ungetc(int char, FILE \*stream)** pushes the character **char (an unsigned char)** onto the specified **stream** so that the this is available for the next read operation.

## Declaration

Following is the declaration for ungetc() function.

```c
int ungetc(int char, FILE *stream)
```

## Parameters

-   **char** − This is the character to be put back. This is passed as its int promotion.
    
-   **stream** − This is the pointer to a FILE object that identifies an input stream.
    

## Return Value

If successful, it returns the character that was pushed back otherwise, EOF is returned and the stream remains unchanged.

## Example

The following example shows the usage of ungetc() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int c;
   char buffer [256];

   fp = fopen("file.txt", "r");
   if( fp == NULL ) {
      perror("Error in opening file");
      return(-1);
   }
   while(!feof(fp)) {
      c = getc (fp);
      /* replace ! with + */
      if( c == '!' ) {
         ungetc ('+', fp);
      } else {
         ungetc(c, fp);
      }
      fgets(buffer, 255, fp);
      fputs(buffer, stdout);
   }
   return(0);
}
```

Let us assume, we have a text file **file.txt**, which contains the following data. This file will be used as an input for our example program −

```c
this is tutorials point
!c standard library
!library functions and macros
```

Now, let us compile and run the above program that will produce the following result −

```c
this is tutorials point
+c standard library
+library functions and macros

```


