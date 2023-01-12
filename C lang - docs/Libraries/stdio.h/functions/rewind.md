---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_rewind.htm
author: 
---

# C library function - rewind()

> ## Excerpt
> C library function - rewind(),  The C library function void rewind(FILE *stream) sets the file position to the beginning of the file of the given stream.

---
---

  

## Description

The C library function **void rewind(FILE \*stream)** sets the file position to the beginning of the file of the given **stream**.

## Declaration

Following is the declaration for rewind() function.

```c
void rewind(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of rewind() function.

```c
#include <stdio.h>

int main () {
   char str[] = "This is tutorialspoint.com";
   FILE *fp;
   int ch;

   /* First let's write some content in the file */
   fp = fopen( "file.txt" , "w" );
   fwrite(str , 1 , sizeof(str) , fp );
   fclose(fp);

   fp = fopen( "file.txt" , "r" );
   while(1) {
      ch = fgetc(fp);
      if( feof(fp) ) {
         break ;
      }
      printf("%c", ch);
   }
   rewind(fp);
   printf("\n");
   while(1) {
      ch = fgetc(fp);
      if( feof(fp) ) {
         break ;
      }
      printf("%c", ch);
     
   }
   fclose(fp);

   return(0);
}
```

Let us assume we have a text file **file.txt** that have the following content −

```c
This is tutorialspoint.com
```

Now let us compile and run the above program to produce the following result −

```c
This is tutorialspoint.com
This is tutorialspoint.com

```


