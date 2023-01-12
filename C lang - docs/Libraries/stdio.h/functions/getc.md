---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_getc.htm
author: 
---

# C library function - getc()

> ## Excerpt
> C library function - getc(),  The C library function int getc(FILE *stream) gets the next character (an unsigned char) from the specified stream and advances the position indicator for the s

---
---

  

## Description

The C library function **int getc(FILE \*stream)** gets the next character (an unsigned char) from the specified stream and advances the position indicator for the stream.

## Declaration

Following is the declaration for getc() function.

```c
int getc(FILE *stream)
```

## Parameters

-   **stream** − This is the pointer to a FILE object that identifies the stream on which the operation is to be performed.
    

## Return Value

This function returns the character read as an unsigned char cast to an int or EOF on end of file or error.

## Example

The following example shows the usage of getc() function.

```c
#include<stdio.h>

int main () {
   char c;

   printf("Enter character: ");
   c = getc(stdin);
   printf("Character entered: ");
   putc(c, stdout);
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Enter character: a
Character entered: a

```


