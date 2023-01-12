---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_rename.htm
author: 
---

# C library function - rename()

> ## Excerpt
> C library function - rename(),  The C library function int rename(const char *old_filename, const char *new_filename) causes the filename referred to by old_filename to be changed to new_filen

---
---

  

## Description

The C library function **int rename(const char \*old\_filename, const char \*new\_filename)** causes the filename referred to by **old\_filename** to be changed to **new\_filename**.

## Declaration

Following is the declaration for rename() function.

```c
int rename(const char *old_filename, const char *new_filename)
```

## Parameters

-   **old\_filename** − This is the C string containing the name of the file to be renamed and/or moved.
    
-   **new\_filename** − This is the C string containing the new name for the file.
    

## Return Value

On success, zero is returned. On error, -1 is returned, and errno is set appropriately.

## Example

The following example shows the usage of rename() function.

```c
#include <stdio.h>

int main () {
   int ret;
   char oldname[] = "file.txt";
   char newname[] = "newfile.txt";
   
   ret = rename(oldname, newname);

   if(ret == 0) {
      printf("File renamed successfully");
   } else {
      printf("Error: unable to rename the file");
   }
   
   return(0);
}
```

Let us assume we have a text file **file.txt**, having some content. So, we are going to rename this file, using the above program. Let us compile and run the above program to produce the following message and the file will be renamed to **newfile.txt** file.

```c
File renamed successfully

```


