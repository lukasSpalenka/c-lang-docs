---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fopen.htm
author: 
---

# C library function - fopen()

> ## Excerpt
> C library function - fopen(),  The C library function FILE *fopen(const char *filename, const char *mode) opens the filename pointed to, by filename using the given mode.

---
---

  

## Description

The C library function **FILE \*fopen(const char \*filename, const char \*mode)** opens the **filename** pointed to, by filename using the given **mode**.

## Declaration

Following is the declaration for fopen() function.

```c
FILE *fopen(const char *filename, const char *mode)
```

## Parameters

-   **filename** − This is the C string containing the name of the file to be opened.
    
-   **mode** − This is the C string containing a file access mode. It includes −
    

| Sr.No. | Mode & Description |
| --- | --- |
| 1 |  **"r"**<br>Opens a file for reading. The file must exist.<br> |
| 2 | <br>**"w"**<br>Creates an empty file for writing. If a file with the same name already exists, its content is erased and the file is considered as a new empty file.<br> |
| 3 | <br>**"a"**<br>Appends to a file. Writing operations, append data at the end of the file. The file is created if it does not exist.<br> |
| 4 | <br>**"r+"**<br>Opens a file to update both reading and writing. The file must exist.<br> |
| 5 | <br>**"w+"**<br>Creates an empty file for both reading and writing.<br> |
| 6 | <br>**"a+"**<br>Opens a file for reading and appending.<br> |

## Return Value

This function returns a FILE pointer. Otherwise, NULL is returned and the global variable errno is set to indicate the error.

## Example

The following example shows the usage of fopen() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   FILE * fp;

   fp = fopen ("file.txt", "w+");
   fprintf(fp, "%s %s %s %d", "We", "are", "in", 2012);
   
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will create a file **file.txt** with the following content −

```c
We are in 2012

```

Now let us see the content of the above file using the following program −

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
We are in 2012

```


