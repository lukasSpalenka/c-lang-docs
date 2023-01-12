---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_putc.htm
author: 
---

# C library function - putc()

> ## Excerpt
> C library function - putc(),  The C library function int putc(int char, FILE *stream) writes a character (an unsigned char) specified by the argument char to the specified stream and advance

---
---

  

## Description

The C library function **int putc(int char, FILE \*stream)** writes a character (an unsigned char) specified by the argument **char** to the specified stream and advances the position indicator for the stream.

## Declaration

Following is the declaration for putc() function.

```c
int putc(int char, FILE *stream)
```

## Parameters

-   **char** − This is the character to be written. The character is passed as its int promotion.
    
-   **stream** − This is the pointer to a FILE object that identifies the stream where the character is to be written.
    

## Return Value

This function returns the character written as an unsigned char cast to an int or EOF on error.

## Example

The following example shows the usage of putc() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   int ch;

   fp = fopen("file.txt", "w");
   for( ch = 33 ; ch <= 100; ch++ ) {
      putc(ch, fp);
   }
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will create a file **file.txt** in the current directory which will have following content −

```c
!"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcd

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
         break ;
      }
      printf("%c", c);
   }
   fclose(fp);
   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
!"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcd

```


