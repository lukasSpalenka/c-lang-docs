---
created: 2023-01-12T21:14:20 (UTC +01:00)
tags: []

author: 
---

# C Library - <string.h>

> ## Excerpt
> C Library - <string.h>,  The string.h header defines one variable type, one macro, and various functions for manipulating arrays of characters.

---
---

The **string.h** header defines one variable type, one macro, and various functions for manipulating arrays of characters.

## Library Variables

Following is the variable type defined in the header string.h −

| Sr.No. | Variable & Description |
| --- | --- |
| 1 |  **size\_t**<br>This is the unsigned integral type and is the result of the **sizeof** keyword.<br> |

## Library Macros

Following is the macro defined in the header string.h −

| Sr.No. | Macro & Description |
| --- | --- |
| 1 |  **NULL**<br>This macro is the value of a null pointer constant.<br> |

## Library Functions

Following are the functions defined in the header string.h −

| Sr.No. | Function & Description |
| --- | --- |
| 1 | [void \*memchr(const void \*str, int c, size\_t n)](./functions/memchr.md) Searches for the first occurrence of the character c (an unsigned char) in the first n bytes of the string pointed to, by the argument _str_.<br> |
| 2 | [int memcmp(const void \*str1, const void \*str2, size\_t n)](./functions/memcmp.md)<br>Compares the first n bytes of _str1_ and _str2_.<br> |
| 3 | [void \*memcpy(void \*dest, const void \*src, size\_t n)](./functions/memcpy.md)<br>Copies n characters from src to _dest_.<br> |
| 4 | [void \*memmove(void \*dest, const void \*src, size\_t n)](./functions/memmove.md)<br>Another function to copy n characters from _str2_ to _str1_.<br> |
| 5 | [void \*memset(void \*str, int c, size\_t n)](./functions/memset.md)<br>Copies the character c (an unsigned char) to the first n characters of the string pointed to, by the argument _str_.<br> |
| 6 | [char \*strcat(char \*dest, const char \*src)](./functions/strcat.md)<br>Appends the string pointed to, by _src_ to the end of the string pointed to by _dest_.<br> |
| 7 | [char \*strncat(char \*dest, const char \*src, size\_t n)](./functions/strncat.md)<br>Appends the string pointed to, by _src_ to the end of the string pointed to, by _dest_ up to n characters long.<br> |
| 8 | [char \*strchr(const char \*str, int c)](./functions/strchr.md)<br>Searches for the first occurrence of the character c (an unsigned char) in the string pointed to, by the argument _str_.<br> |
| 9 | [int strcmp(const char \*str1, const char \*str2)](./functions/strcmp.md)<br>Compares the string pointed to, by _str1_ to the string pointed to by _str2_.<br> |
| 10 | [int strncmp(const char \*str1, const char \*str2, size\_t n)](./functions/strncmp.md)<br>Compares at most the first n bytes of _str1_ and _str2_.<br> |
| 11 | [int strcoll(const char \*str1, const char \*str2)](./functions/strcoll.md)<br>Compares string _str1_ to _str2_. The result is dependent on the LC\_COLLATE setting of the location.<br> |
| 12 | [char \*strcpy(char \*dest, const char \*src)](./functions/strcpy.md)<br>Copies the string pointed to, by _src_ to _dest_.<br> |
| 13 | [char \*strncpy(char \*dest, const char \*src, size\_t n)](./functions/strncpy.md)<br>Copies up to n characters from the string pointed to, by _src_ to _dest_.<br> |
| 14 | [size\_t strcspn(const char \*str1, const char \*str2)](./functions/strcspn.md)<br>Calculates the length of the initial segment of str1 which consists entirely of characters not in str2.<br> |
| 15 | [char \*strerror(int errnum)](./functions/strerror.md)<br>Searches an internal array for the error number errnum and returns a pointer to an error message string.<br> |
| 16 | [size\_t strlen(const char \*str)](./functions/strlen.md)<br>Computes the length of the string str up to but not including the terminating null character.<br> |
| 17 | [char \*strpbrk(const char \*str1, const char \*str2)](./functions/strpbrk.md)<br>Finds the first character in the string _str1_ that matches any character specified in _str2_.<br> |
| 18 | [char \*strrchr(const char \*str, int c)](./functions/strrchr.md)<br>Searches for the last occurrence of the character c (an unsigned char) in the string pointed to by the argument _str_.<br> |
| 19 | [size\_t strspn(const char \*str1, const char \*str2)](./functions/strspn.md)<br>Calculates the length of the initial segment of _str1_ which consists entirely of characters in _str2_.<br> |
| 20 | [char \*strstr(const char \*haystack, const char \*needle)](./functions/strstr.md)<br>Finds the first occurrence of the entire string _needle_ (not including the terminating null character) which appears in the string _haystack_.<br> |
| 21 | [char \*strtok(char \*str, const char \*delim)](./functions/strtok.md)<br>Breaks string _str_ into a series of tokens separated by _delim_.<br> |
| 22 | [size\_t strxfrm(char \*dest, const char \*src, size\_t n)](./functions/strxfrm.md)<br>Transforms the first **n** characters of the string **src** into current locale and places them in the string **dest**.<br> |
