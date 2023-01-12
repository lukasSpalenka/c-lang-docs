---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fputs.htm
author: 
---

# C library function - fputs()

> ## Excerpt
> C library function - fputs(),  The C library function int fputs(const char *str, FILE *stream) writes a string to the specified stream up to but not including the null character.

---
---

  

## Description

The C library function **int fputs(const char \*str, FILE \*stream)** writes a string to the specified stream up to but not including the null character.

## Declaration

Following is the declaration for fputs() function.

```c
int fputs(const char *str, FILE *stream)
```

## Parameters

-   **str** − This is an array containing the null-terminated sequence of characters to be written.
    
-   **stream** − This is the pointer to a FILE object that identifies the stream where the string is to be written.
    

## Return Value

This function returns a non-negative value, or else on error it returns EOF.

## Example

The following example shows the usage of fputs() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;

   fp = fopen("file.txt", "w+");

   fputs("This is c programming.", fp);
   fputs("This is a system programming language.", fp);

   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program, this will create a file **file.txt** with the following content −

```c
This is c programming.This is a system programming language.

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

Let us compile and run the above program to produce the following result.

```c
This is c programming.This is a system programming language.

```


