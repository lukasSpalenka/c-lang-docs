---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []

author: 
---

# C library function - fflush()

> ## Excerpt
> C library function - fflush(),  The C library function int fflush(FILE *stream) flushes the output buffer of a stream.

---
---

  

## Description

The C library function **int fflush(FILE \*stream)** flushes the output buffer of a stream.

## Declaration

Following is the declaration for fflush() function.

```c
int fflush(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that specifies a buffered stream.
    

## Return Value

This function returns a zero value on success. If an error occurs, EOF is returned and the error indicator is set (i.e. feof).

## Example

The following example shows the usage of fflush() function.

```c
#include <stdio.h>
#include <string.h>

int main () {

   char buff[1024];
   
   memset( buff, '\0', sizeof( buff ));
   
   fprintf(stdout, "Going to set full buffering on\n");
   setvbuf(stdout, buff, _IOFBF, 1024);

   fprintf(stdout, "This is tutorialspoint.com\n");
   fprintf(stdout, "This output will go into buff\n");
   fflush( stdout );

   fprintf(stdout, "and this will appear when programm\n");
   fprintf(stdout, "will come after sleeping 5 seconds\n");
   
   sleep(5);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result. Here program keeps buffering into the output into **buff** until it faces first call to **fflush()**, after which it again starts buffering the output and finally sleeps for 5 seconds. It sends remaining output to the STDOUT before program comes out.

```c
Going to set full buffering on
This is tutorialspoint.com
This output will go into buff
and this will appear when programm
will come after sleeping 5 seconds

```


