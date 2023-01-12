---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fread.htm
author: 
---

# C library function - fread()

> ## Excerpt
> C library function - fread(),  The C library function size_t fread(void *ptr, size_t size, size_t nmemb, FILE *stream) reads data from the given stream into the array pointed to, by ptr.

---
---

  

## Description

The C library function **size\_t fread(void \*ptr, size\_t size, size\_t nmemb, FILE \*stream)** reads data from the given **stream** into the array pointed to, by **ptr**.

## Declaration

Following is the declaration for fread() function.

```c
size_t fread(void *ptr, size_t size, size_t nmemb, FILE *stream)
```

## Parameters

-   **ptr** − This is the pointer to a block of memory with a minimum size of _size\*nmemb_ bytes.
    
-   **size** − This is the size in bytes of each element to be read.
    
-   **nmemb** − This is the number of elements, each one with a size of **size** bytes.
    
-   **stream** − This is the pointer to a FILE object that specifies an input stream.
    

## Return Value

The total number of elements successfully read are returned as a size\_t object, which is an integral data type. If this number differs from the nmemb parameter, then either an error had occurred or the End Of File was reached.

## Example

The following example shows the usage of fread() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   FILE *fp;
   char c[] = "this is tutorialspoint";
   char buffer[100];

   /* Open file for both reading and writing */
   fp = fopen("file.txt", "w+");

   /* Write data to the file */
   fwrite(c, strlen(c) + 1, 1, fp);

   /* Seek to the beginning of the file */
   fseek(fp, 0, SEEK_SET);

   /* Read and display data */
   fread(buffer, strlen(c)+1, 1, fp);
   printf("%s\n", buffer);
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will create a file **file.txt** and write a content _this is tutorialspoint_. After that, we use **fseek()** function to reset writing pointer to the beginning of the file and prepare the file content which is as follows −

```c
this is tutorialspoint

```


