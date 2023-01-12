---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_getchar.htm
author: 
---

# C library function - getchar()

> ## Excerpt
> C library function - getchar(),  The C library function int getchar(void) gets a character (an unsigned char) from stdin. This is equivalent to getc with stdin as its argument.

---
---

  

## Description

The C library function **int getchar(void)** gets a character (an unsigned char) from stdin. This is equivalent to **getc** with stdin as its argument.

## Declaration

Following is the declaration for getchar() function.

```c
int getchar(void)
```

## Parameters

-   **NA**
    

## Return Value

This function returns the character read as an unsigned char cast to an int or EOF on end of file or error.

## Example

The following example shows the usage of getchar() function.

```c
#include <stdio.h>

int main () {
   char c;
 
   printf("Enter character: ");
   c = getchar();
 
   printf("Character entered: ");
   putchar(c);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Enter character: a
Character entered: a

```


