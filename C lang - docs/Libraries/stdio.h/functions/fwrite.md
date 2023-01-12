---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fwrite.htm
author: 
---

# C library function - fwrite()

> ## Excerpt
> C library function - fwrite(),  The C library function size_t fwrite(const void *ptr, size_t size, size_t nmemb, FILE *stream) writes data from the array pointed to, by ptr to the given stream

---
---

  

## Description

The C library function **size\_t fwrite(const void \*ptr, size\_t size, size\_t nmemb, FILE \*stream)** writes data from the array pointed to, by **ptr** to the given **stream**.

## Declaration

Following is the declaration for fwrite() function.

```c
size_t fwrite(const void *ptr, size_t size, size_t nmemb, FILE *stream)
```

## Parameters

-   **ptr** − This is the pointer to the array of elements to be written.
    
-   **size** − This is the size in bytes of each element to be written.
    
-   **nmemb** − This is the number of elements, each one with a size of **size** bytes.
    
-   **stream** − This is the pointer to a FILE object that specifies an output stream.
    

## Return Value

This function returns the total number of elements successfully returned as a size\_t object, which is an integral data type. If this number differs from the nmemb parameter, it will show an error.

## Example

The following example shows the usage of fwrite() function.

```c
#include<stdio.h>

int main () {
   FILE *fp;
   char str[] = "This is tutorialspoint.com";

   fp = fopen( "file.txt" , "w" );
   fwrite(str , 1 , sizeof(str) , fp );

   fclose(fp);
  
   return(0);
}
```

Let us compile and run the above program that will create a file **file.txt** which will have following content −

```c
This is tutorialspoint.com

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
This is tutorialspoint.com

```


