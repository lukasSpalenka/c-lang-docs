---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fsetpos.htm
author: 
---

# C library function - fsetpos()

> ## Excerpt
> C library function - fsetpos(),  The C library function int fsetpos(FILE *stream, const fpos_t *pos) sets the file position of the given stream to the given position. The argument pos is a posi

---
---

  

## Description

The C library function **int fsetpos(FILE \*stream, const fpos\_t \*pos)** sets the file position of the given **stream** to the given position. The argument **pos** is a position given by the function fgetpos.

## Declaration

Following is the declaration for fsetpos() function.

```c
int fsetpos(FILE *stream, const fpos_t *pos)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    
-   **pos** − This is the pointer to a fpos\_t object containing a position previously obtained with fgetpos.
    

## Return Value

This function returns zero value if successful, or else it returns a non-zero value and sets the global variable **errno** to a positive value, which can be interpreted with perror.

## Example

The following example shows the usage of fsetpos() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   fpos_t position;

   fp = fopen("file.txt","w+");
   fgetpos(fp, &position);
   fputs("Hello, World!", fp);
  
   fsetpos(fp, &position);
   fputs("This is going to override previous content", fp);
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program to create a file **file.txt** which will have the following content. First of all we get the initial position of the file using **fgetpos()** function, and then we write _Hello, World!_ in the file but later we used **fsetpos()** function to reset the write pointer at the beginning of the file and then over-write the file with the following content −

```c
This is going to override previous content

```

Now let's see the content of the above file using the following program −

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int c;

   fp = fopen("file.txt","r");
   while(1) {
      c = fgetc(fp);
      if( feof(fp) ) {
         break;
      }
      printf("%c", c);
   }
   fclose(fp);
   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
This is going to override previous content

```


