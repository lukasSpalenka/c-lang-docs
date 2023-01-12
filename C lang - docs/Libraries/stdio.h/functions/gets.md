---
created: 2023-01-12T18:01:37 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_gets.htm
author: 
---

# C library function - gets()

> ## Excerpt
> C library function - gets(),  The C library function char *gets(char *str) reads a line from stdin and stores it into the string pointed to by str. It stops when either the newline character

---
---

  

## Description

The C library function **char \*gets(char \*str)** reads a line from stdin and stores it into the string pointed to by str. It stops when either the newline character is read or when the end-of-file is reached, whichever comes first.

## Declaration

Following is the declaration for gets() function.

```c
char *gets(char *str)
```

## Parameters

-   **str** − This is the pointer to an array of chars where the C string is stored.
    

## Return Value

This function returns str on success, and NULL on error or when end of file occurs, while no characters have been read.

## Example

The following example shows the usage of gets() function.

```c
#include <stdio.h>

int main () {
   char str[50];

   printf("Enter a string : ");
   gets(str);

   printf("You entered: %s", str);

   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Enter a string : tutorialspoint.com
You entered: tutorialspoint.com

```


