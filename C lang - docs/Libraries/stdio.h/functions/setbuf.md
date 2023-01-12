---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_setbuf.htm
author: 
---

# C library function - setbuf()

> ## Excerpt
> C library function - setbuf(),  The C library function void setbuf(FILE *stream, char *buffer) defines how a stream should be buffered. This function should be called once the file associated

---
---

  

## Description

The C library function **void setbuf(FILE \*stream, char \*buffer)** defines how a stream should be buffered. This function should be called once the file associated with the stream has already been opened, but before any input or output operation has taken place.

## Declaration

Following is the declaration for setbuf() function.

```c
void setbuf(FILE *stream, char *buffer)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies an open stream.
    
-   **buffer** − This is the user allocated buffer. This should have a length of at least BUFSIZ bytes, which is a macro constant to be used as the length of this array.
    

## Return Value

This function does not return any value.

## Example

The following example shows the usage of setbuf() function.

```c
#include <stdio.h>

int main () {
   char buf[BUFSIZ];

   setbuf(stdout, buf);
   puts("This is tutorialspoint");

   fflush(stdout);
   return(0);
}
```

Let us compile and run the above program to produce the following result. Here program sends output to the STDOUT just before it comes out, otherwise it keeps buffering the output. You can also use fflush() function to flush the output.

```c
This is tutorialspoint

```


