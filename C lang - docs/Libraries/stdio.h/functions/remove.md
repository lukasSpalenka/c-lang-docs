---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_remove.htm
author: 
---

# C library function - remove()

> ## Excerpt
> C library function - remove(),  The C library function int remove(const char *filename) deletes the given filename so that it is no longer accessible.

---
---

  

## Description

The C library function **int remove(const char \*filename)** deletes the given **filename** so that it is no longer accessible.

## Declaration

Following is the declaration for remove() function.

```c
int remove(const char *filename)
```

## Parameters

-   **filename** − This is the C string containing the name of the file to be deleted.
    

## Return Value

On success, zero is returned. On error, -1 is returned, and errno is set appropriately.

## Example

The following example shows the usage of remove() function.

```c
#include <stdio.h>
#include <string.h>

int main () {
   int ret;
   FILE *fp;
   char filename[] = "file.txt";

   fp = fopen(filename, "w");

   fprintf(fp, "%s", "This is tutorialspoint.com");
   fclose(fp);
   
   ret = remove(filename);

   if(ret == 0) {
      printf("File deleted successfully");
   } else {
      printf("Error: unable to delete the file");
   }
   
   return(0);
}
```

Let us assume we have a text file **file.txt** having some content. So we are going to delete this file, using the above program. Let us compile and run the above program to produce the following message and the file will be deleted permanently.

```c
File deleted successfully

```


