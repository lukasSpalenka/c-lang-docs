---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_fseek.htm
author: 
---

# C library function - fseek()

> ## Excerpt
> C library function - fseek(),  The C library function int fseek(FILE *stream, long int offset, int whence) sets the file position of the stream to the given offset.

---
---

  

## Description

The C library function **int fseek(FILE \*stream, long int offset, int whence)** sets the file position of the **stream** to the given **offset**.

## Declaration

Following is the declaration for fseek() function.

```c
int fseek(FILE *stream, long int offset, int whence)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream.
    
-   **offset** − This is the number of bytes to offset from whence.
    
-   **whence** − This is the position from where offset is added. It is specified by one of the following constants −
    

| Sr.No. | Constant & Description |
| --- | --- |
| 1 |  **SEEK\_SET**<br>Beginning of file<br> |
| 2 | <br>**SEEK\_CUR**<br>Current position of the file pointer<br> |
| 3 | <br>**SEEK\_END**<br>End of file<br> |

## Return Value

This function returns zero if successful, or else it returns a non-zero value.

## Example

The following example shows the usage of fseek() function.

```c
#include <stdio.h>

int main () {
   FILE *fp;

   fp = fopen("file.txt","w+");
   fputs("This is tutorialspoint.com", fp);
  
   fseek( fp, 7, SEEK_SET );
   fputs(" C Programming Language", fp);
   fclose(fp);
   
   return(0);
}
```

Let us compile and run the above program that will create a file **file.txt** with the following content. Initially program creates the file and writes _This is tutorialspoint.com_ but later we had reset the write pointer at 7th position from the beginning and used puts() statement which over-write the file with the following content −

```c
This is C Programming Language
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
         break;
      }
      printf("%c", c); 
   }
   fclose(fp);
   return(0);
}
```

Let us compile and run the above program to produce the following result −

```c
This is C Programming Language

```


