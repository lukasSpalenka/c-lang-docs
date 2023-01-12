---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_calloc.htm
author: 
---

# C library function - calloc()

> ## Excerpt
> C library function - calloc(),  The C library function void *calloc(size_t nitems, size_t size) allocates the requested memory and returns a pointer to it. The difference in malloc and calloc

---
---

  

## Description

The C library function **void \*calloc(size\_t nitems, size\_t size)** allocates the requested memory and returns a pointer to it. The difference in **malloc** and **calloc** is that malloc does not set the memory to zero where as calloc sets allocated memory to zero.

## Declaration

Following is the declaration for calloc() function.

```c
void *calloc(size_t nitems, size_t size)
```

## Parameters

-   **nitems** − This is the number of elements to be allocated.
    
-   **size** − This is the size of elements.
    

## Return Value

This function returns a pointer to the allocated memory, or NULL if the request fails.

## Example

The following example shows the usage of calloc() function.

```c
#include <stdio.h>
#include <stdlib.h>

int main () {
   int i, n;
   int *a;

   printf("Number of elements to be entered:");
   scanf("%d",&n);

   a = (int*)calloc(n, sizeof(int));
   printf("Enter %d numbers:\n",n);
   for( i=0 ; i < n ; i++ ) {
      scanf("%d",&a[i]);
   }

   printf("The numbers entered are: ");
   for( i=0 ; i < n ; i++ ) {
      printf("%d ",a[i]);
   }
   free( a );
   
   return(0);
}
```

Let us compile and run the above program that will produce the following result −

```c
Number of elements to be entered:3
Enter 3 numbers:
22
55
14
The numbers entered are: 22 55 14

```


