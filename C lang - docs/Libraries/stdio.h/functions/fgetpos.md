---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fgetpos.htm
author: 
---

# C library function - fgetpos()

> ## Excerpt
> C library function - fgetpos(),  The C library function int fgetpos(FILE *stream, fpos_t *pos) gets the current file position of the stream and writes it to pos.

---
---

  

## Description

The C library function **int fgetpos(FILE \*stream, fpos\_t \*pos)** gets the current file position of the **stream** and writes it to **pos**.

## Declaration

Following is the declaration for fgetpos() function.

```c
int fgetpos(FILE *stream, fpos_t *pos)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    
-   **pos** − This is the pointer to a fpos\_t object.
    

## Return Value

This function returns zero on success, else non-zero value in case of an error.

## Example

The following example shows the usage of fgetpos() function.

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

Let us compile and run the above program to create a file **file.txt** which will have the following content. First of all we get the initial position of the file using **fgetpos()** function and then we write _Hello, World!_in the file, but later we have used **fsetpos()** function to reset the write pointer at the beginning of the file and then over-write the file with the following content −

```c
This is going to override previous content

```

Now let us see the content of the above file using the following program −

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int c;
   int n = 0;

   fp = fopen("file.txt","r");
   
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

Let us compile and run above program to produce the following result −

```c
This is going to override previous content

```


