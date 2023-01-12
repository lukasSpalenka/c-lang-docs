---
created: 2023-01-12T21:11:20 (UTC +01:00)
tags: []

author: 
---

# C Library - <stdlib.h>

> ## Excerpt
> C Library - <stdlib.h>,  The stdlib.h header defines four variable types, several macros, and various functions for performing general functions.

---
---

The **stdlib.h** header defines four variable types, several macros, and various functions for performing general functions.

## Library Variables

Following are the variable types defined in the header stdlib.h −

| Sr.No. | Variable & Description |
| --- | --- |
| 1 |  **size\_t**<br>This is the unsigned integral type and is the result of the **sizeof** keyword.<br> |
| 2 | <br>**wchar\_t**<br>This is an integer type of the size of a **wide** character constant.<br> |
| 3 | <br>**div\_t**<br>This is the structure returned by the **div** function.<br> |
| 4 | <br>**ldiv\_t**<br>This is the structure returned by the **ldiv** function.<br> |

## Library Macros

Following are the macros defined in the header stdlib.h −

| Sr.No. | Macro & Description |
| --- | --- |
| 1 |  **NULL**<br>This macro is the value of a null pointer constant.<br> |
| 2 | <br>**EXIT\_FAILURE**<br>This is the value for the exit function to return in case of failure.<br> |
| 3 | <br>**EXIT\_SUCCESS**<br>This is the value for the exit function to return in case of success.<br> |
| 4 | <br>**RAND\_MAX**<br>This macro is the maximum value returned by the rand function.<br> |
| 5 | <br>**MB\_CUR\_MAX**<br>This macro is the maximum number of bytes in a multi-byte character set which cannot be larger than MB\_LEN\_MAX.<br> |

## Library Functions

Following are the functions defined in the header stlib.h −

| Sr.No. | Function & Description |
| --- | --- |
| 1 | [double atof(const char \*str)](./functions/atof.md) Converts the string pointed to, by the argument _str_ to a floating-point number (type double).<br> |
| 2 | [int atoi(const char \*str)](./functions/atoi.md)<br>Converts the string pointed to, by the argument _str_ to an integer (type int).<br> |
| 3 | [long int atol(const char \*str)](./functions/atol.md)<br>Converts the string pointed to, by the argument _str_ to a long integer (type long int).<br> |
| 4 | [double strtod(const char \*str, char \*\*endptr)](./functions/strtod.md)<br>Converts the string pointed to, by the argument _str_ to a floating-point number (type double).<br> |
| 5 | [long int strtol(const char \*str, char \*\*endptr, int base)](./functions/strtol.md)<br>Converts the string pointed to, by the argument _str_ to a long integer (type long int).<br> |
| 6 | [unsigned long int strtoul(const char \*str, char \*\*endptr, int base)](./functions/strtoul.md)<br>Converts the string pointed to, by the argument _str_ to an unsigned long integer (type unsigned long int).<br> |
| 7 | [void \*calloc(size\_t nitems, size\_t size)](./functions/calloc.md)<br>Allocates the requested memory and returns a pointer to it.<br> |
| 8 | [void free(void \*ptr](./functions/free.md)<br>Deallocates the memory previously allocated by a call to _calloc, malloc,_ or _realloc_.<br> |
| 9 | [void \*malloc(size\_t size)](./functions/malloc.md)<br>Allocates the requested memory and returns a pointer to it.<br> |
| 10 | [void \*realloc(void \*ptr, size\_t size)](./functions/realloc.md)<br>Attempts to resize the memory block pointed to by ptr that was previously allocated with a call to _malloc_ or _calloc_.<br> |
| 11 | [void abort(void)](./functions/abort.md)<br>Causes an abnormal program termination.<br> |
| 12 | [int atexit(void (\*func)(void))](./functions/atexit.md)<br>Causes the specified function **func** to be called when the program terminates normally.<br> |
| 13 | [void exit(int status)](./functions/exit.md)<br>Causes the program to terminate normally.<br> |
| 14 | [char \*getenv(const char \*name)](./functions/getenv.md)<br>Searches for the environment string pointed to by name and returns the associated value to the string.<br> |
| 15 | [int system(const char \*string)](./functions/system.md)<br>The command specified by string is passed to the host environment to be executed by the command processor.<br> |
| 17 | [void qsort(void \*base, size\_t nitems, size\_t size, int (\*compar)(const void \*, const void\*))](./functions/qsort.md)<br>Sorts an array.<br> |
| 18 | [int abs(int x)](./functions/abs.md)<br>Returns the absolute value of x.<br> |
| 19 | [div\_t div(int numer, int denom)](./functions/div.md)<br>Divides numer (numerator) by denom (denominator).<br> |
| 20 | [long int labs(long int x)](./functions/labs.md)<br>Returns the absolute value of x.<br> |
| 21 | [ldiv\_t ldiv(long int numer, long int denom)](./functions/ldiv.md)<br>Divides numer (numerator) by denom (denominator).<br> |
| 22 | [int rand(void)](./functions/rand.md)<br>Returns a pseudo-random number in the range of 0 to _RAND\_MAX_.<br> |
| 23 | [void srand(unsigned int seed)](./functions/srand.md)<br>This function seeds the random number generator used by the function **rand**.<br> |
| 24 | [int mblen(const char \*str, size\_t n)](./functions/mblen.md)<br>Returns the length of a multibyte character pointed to by the argument _str_.<br> |
| 25 | [size\_t mbstowcs(schar\_t \*pwcs, const char \*str, size\_t n)](./functions/mbstowcs.md)<br>Converts the string of multibyte characters pointed to by the argument _str_ to the array pointed to by _pwcs_.<br> |
| 26 | [int mbtowc(whcar\_t \*pwc, const char \*str, size\_t n)](./functions/mbtowc.md)<br>Examines the multibyte character pointed to by the argument _str_.<br> |
| 27 | [size\_t wcstombs(char \*str, const wchar\_t \*pwcs, size\_t n)](./functions/wcstombs.md)<br>Converts the codes stored in the array _pwcs_ to multibyte characters and stores them in the string _str_.<br> |
| 28 | [int wctomb(char \*str, wchar\_t wchar)](./functions/wctomb.md)<br>Examines the code which corresponds to a multibyte character given by the argument _wchar_.<br> |
