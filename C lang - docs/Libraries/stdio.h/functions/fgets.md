---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fgets.htm
author: 
---

# C library function - fgets()

> ## Excerpt
> C library function - fgets(),  The C library function char *fgets(char *str, int n, FILE *stream) reads a line from the specified stream and stores it into the string pointed to by str. It st

---
---

  

## Description

The C library function **char \*fgets(char \*str, int n, FILE \*stream)** reads a line from the specified stream and stores it into the string pointed to by **str**. It stops when either **(n-1)** characters are read, the newline character is read, or the end-of-file is reached, whichever comes first.

## Declaration

Following is the declaration for fgets() function.

```c
char *fgets(char *str, int n, FILE *stream)
```

## Parameters

-   **str** − This is the pointer to an array of chars where the string read is stored.
    
-   **n** − This is the maximum number of characters to be read (including the final null-character). Usually, the length of the array passed as str is used.
    
-   **stream** − This is the pointer to a FILE object that identifies the stream where characters are read from.
    

## Return Value

On success, the function returns the same str parameter. If the End-of-File is encountered and no characters have been read, the contents of str remain unchanged and a null pointer is returned.

If an error occurs, a null pointer is returned.

## Example

The following example shows the usage of fgets() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;
   char str[60];

   /* opening file for reading */
   fp = fopen("file.txt" , "r");
   if(fp == NULL) {
      perror("Error opening file");
      return(-1);
   }
   if( fgets (str, 60, fp)!=NULL ) {
      /* writing content to stdout */
      puts(str);
   }
   fclose(fp);
   
   return(0);
}
```

Let us assume, we have a text file **file.txt**, which has the following content. This file will be used as an input for our example program −

```c
We are in 2012
```

Now, let us compile and run the above program that will produce the following result −

```c
We are in 2012

```


