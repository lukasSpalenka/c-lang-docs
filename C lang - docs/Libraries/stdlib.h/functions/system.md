---
created: 2023-01-12T18:03:27 (UTC +01:00)
tags: []
source: https://www.tutorialspoint.com/c_standard_library/c_function_system.htm
author: 
---

# C library function - system()

> ## Excerpt
> C library function - system(),  The C library function int system(const char *command) passes the command name or program name specified by command to the host environment to be executed by th

---
---

  

## Description

The C library function **int system(const char \*command)** passes the command name or program name specified by **command** to the host environment to be executed by the command processor and returns after the command has been completed.

## Declaration

Following is the declaration for system() function.

```c
int system(const char *command)
```

## Parameters

-   **command** − This is the C string containing the name of the requested variable.
    

## Return Value

The value returned is -1 on error, and the return status of the command otherwise.

## Example

The following example shows the usage of system() function to list down all the files and directories in the current directory under unix machine.

```c
#include <iostream>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
   char command[50];

   strcpy( command, "ls -l" );
   system(command);

   return(0);
} 
```

Let us compile and run the above program that will produce the following result on my unix machine −

```c
drwxr-xr-x 2 apache apache 4096 Aug 22 07:25 hsperfdata_apache
drwxr-xr-x 2 railo railo 4096 Aug 21 18:48 hsperfdata_railo
rw------ 1 apache apache 8 Aug 21 18:48 mod_mono_dashboard_XXGLOBAL_1
rw------ 1 apache apache 8 Aug 21 18:48 mod_mono_dashboard_asp_2
srwx---- 1 apache apache 0 Aug 22 05:28 mod_mono_server_asp
rw------ 1 apache apache 0 Aug 22 05:28 mod_mono_server_asp_1280495620
srwx---- 1 apache apache 0 Aug 21 18:48 mod_mono_server_global

```

The following example shows the usage of system() function to list down all the files and directories in the current directory under windows machine.

```c
#include <stdio.h>
#include <string.h>

int main () {
   char command[50];

   strcpy( command, "dir" );
   system(command);

   return(0);
} 
```

Let us compile and run the above program that will produce the following result on my windows machine −

```c
a.txt
amit.doc
sachin
saurav
file.c

```


