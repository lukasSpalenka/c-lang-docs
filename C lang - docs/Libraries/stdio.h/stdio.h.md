---
created: 2023-01-12T21:12:03 (UTC +01:00)
tags: []

author: 
---

# C Library - <stdio.h>

> ## Excerpt
> C Library - <stdio.h>,  The stdio.h header defines three variable types, several macros, and various functions for performing input and output.

---
---

The **stdio.h** header defines three variable types, several macros, and various functions for performing input and output.

## Library Variables

Following are the variable types defined in the header stdio.h −

| Sr.No. | Variable & Description |
| --- | --- |
| 1 |  **size\_t**<br>This is the unsigned integral type and is the result of the **sizeof** keyword.<br> |
| 2 | <br>**FILE**<br>This is an object type suitable for storing information for a file stream.<br> |
| 3 | <br>**fpos\_t**<br>This is an object type suitable for storing any position in a file.<br> |

## Library Macros

Following are the macros defined in the header stdio.h −

| Sr.No. | Macro & Description |
| --- | --- |
| 1 |  **NULL**<br>This macro is the value of a null pointer constant.<br> |
| 2 | <br>**\_IOFBF, \_IOLBF** and **\_IONBF**<br>These are the macros which expand to integral constant expressions with distinct values and suitable for the use as third argument to the **setvbuf** function.<br> |
| 3 | <br>**BUFSIZ**<br>This macro is an integer, which represents the size of the buffer used by the **setbuf** function.<br> |
| 4 | <br>**EOF**<br>This macro is a negative integer, which indicates that the end-of-file has been reached.<br> |
| 5 | <br>**FOPEN\_MAX**<br>This macro is an integer, which represents the maximum number of files that the system can guarantee to be opened simultaneously.<br> |
| 6 | <br>**FILENAME\_MAX**<br>This macro is an integer, which represents the longest length of a char array suitable for holding the longest possible filename. If the implementation imposes no limit, then this value should be the recommended maximum value.<br> |
| 7 | <br>**L\_tmpnam**<br>This macro is an integer, which represents the longest length of a char array suitable for holding the longest possible temporary filename created by the **tmpnam** function.<br> |
| 8 | <br>**SEEK\_CUR, SEEK\_END,** and **SEEK\_SET**<br>These macros are used in the **fseek** function to locate different positions in a file.<br> |
| 9 | <br>**TMP\_MAX**<br>This macro is the maximum number of unique filenames that the function **tmpnam** can generate.<br> |
| 10 | <br>**stderr, stdin,** and **stdout**<br>These macros are pointers to FILE types which correspond to the standard error, standard input, and standard output streams.<br> |

## Library Functions

Following are the functions defined in the header stdio.h −

| Sr.No. | Function & Description |
| --- | --- |
| 1 | [int fclose(FILE \*stream)](./functions/fclose.md) Closes the stream. All buffers are flushed.<br> |
| 2 | [void clearerr(FILE \*stream)](./functions/clearerr.md)<br>Clears the end-of-file and error indicators for the given stream.<br> |
| 3 | [int feof(FILE \*stream)](./functions/feof.md)<br>Tests the end-of-file indicator for the given stream.<br> |
| 4 | [int ferror(FILE \*stream)](./functions/ferror.md)<br>Tests the error indicator for the given stream.<br> |
| 6 | [int fgetpos(FILE \*stream, fpos\_t \*pos)](./functions/fgetpos.md)<br>Gets the current file position of the stream and writes it to pos.<br> |
| 7 | [FILE \*fopen(const char \*filename, const char \*mode)](./functions/fopen.md)<br>Opens the filename pointed to by filename using the given mode.<br> |
| 8 | [size\_t fread(void \*ptr, size\_t size, size\_t nmemb, FILE \*stream)](./functions/fread.md)<br>Reads data from the given stream into the array pointed to by ptr.<br> |
| 9 | [FILE \*freopen(const char \*filename, const char \*mode, FILE \*stream)](./functions/freopen.md)<br>Associates a new filename with the given open stream and same time closing the old file in stream.<br> |
| 10 | [int fseek(FILE \*stream, long int offset, int whence)](./functions/fseek.md)<br>Sets the file position of the stream to the given offset. The argument _offset_ signifies the number of bytes to seek from the given _whence_ position.<br> |
| 11 | [int fsetpos(FILE \*stream, const fpos\_t \*pos)](./functions/fsetpos.md)<br>Sets the file position of the given stream to the given position. The argument _pos_ is a position given by the function fgetpos.<br> |
| 12 | [long int ftell(FILE \*stream)](./functions/ftell.md)<br>Returns the current file position of the given stream.<br> |
| 13 | [size\_t fwrite(const void \*ptr, size\_t size, size\_t nmemb, FILE \*stream)](./functions/fwrite.md)<br>Writes data from the array pointed to by ptr to the given stream.<br> |
| 14 | [int remove(const char \*filename)](./functions/remove.md)<br>Deletes the given filename so that it is no longer accessible.<br> |
| 15 | [int rename(const char \*old\_filename, const char \*new\_filename)](./functions/rename.md)<br>Causes the filename referred to, by old\_filename to be changed to new\_filename.<br> |
| 16 | [void rewind(FILE \*stream)](./functions/rewind.md)<br>Sets the file position to the beginning of the file of the given stream.<br> |
| 17 | [void setbuf(FILE \*stream, char \*buffer)](./functions/setbuf.md)<br>Defines how a stream should be buffered.<br> |
| 18 | [int setvbuf(FILE \*stream, char \*buffer, int mode, size\_t size)](./functions/setvbuf.md)<br>Another function to define how a stream should be buffered.<br> |
| 19 | [FILE \*tmpfile(void)](./functions/tmpfile.md)<br>Creates a temporary file in binary update mode (wb+).<br> |
| 20 | [char \*tmpnam(char \*str)](./functions/tmpnam.md)<br>Generates and returns a valid temporary filename which does not exist.<br> |
| 21 | [int fprintf(FILE \*stream, const char \*format, ...)](./functions/fprintf.md)<br>Sends formatted output to a stream.<br> |
| 22 | [int printf(const char \*format, ...)](./functions/printf.md)<br>Sends formatted output to stdout.<br> |
| 23 | [int sprintf(char \*str, const char \*format, ...)](./functions/sprintf.md)<br>Sends formatted output to a string.<br> |
| 24 | [int vfprintf(FILE \*stream, const char \*format, va\_list arg)](./functions/vfprintf.md)<br>Sends formatted output to a stream using an argument list.<br> |
| 25 | [int vprintf(const char \*format, va\_list arg)](./functions/vprintf.md)<br>Sends formatted output to stdout using an argument list.<br> |
| 26 | [int vsprintf(char \*str, const char \*format, va\_list arg)](./functions/vsprintf.md)<br>Sends formatted output to a string using an argument list.<br> |
| 27 | [int fscanf(FILE \*stream, const char \*format, ...)](./functions/fscanf.md)<br>Reads formatted input from a stream.<br> |
| 28 | [int scanf(const char \*format, ...)](./functions/scanf.md)<br>Reads formatted input from stdin.<br> |
| 29 | [int sscanf(const char \*str, const char \*format, ...)](./functions/sscanf.md)<br>Reads formatted input from a string.<br> |
| 30 | [int fgetc(FILE \*stream)](./functions/fgetc.md)<br>Gets the next character (an unsigned char) from the specified stream and advances the position indicator for the stream.<br> |
| 31 | [char \*fgets(char \*str, int n, FILE \*stream)](./functions/fgets.md)<br>Reads a line from the specified stream and stores it into the string pointed to by str. It stops when either (n-1) characters are read, the newline character is read, or the end-of-file is reached, whichever comes first.<br> |
| 32 | [int fputc(int char, FILE \*stream)](./functions/fputc.md)<br>Writes a character (an unsigned char) specified by the argument char to the specified stream and advances the position indicator for the stream.<br> |
| 33 | [int fputs(const char \*str, FILE \*stream)](./functions/fputs.md)<br>Writes a string to the specified stream up to but not including the null character.<br> |
| 34 | [int getc(FILE \*stream)](./functions/getc.md)<br>Gets the next character (an unsigned char) from the specified stream and advances the position indicator for the stream.<br> |
| 35 | [int getchar(void)](./functions/getchar.md)<br>Gets a character (an unsigned char) from stdin.<br> |
| 36 | [char \*gets(char \*str)](./functions/gets.md)<br>Reads a line from stdin and stores it into the string pointed to by, str. It stops when either the newline character is read or when the end-of-file is reached, whichever comes first.<br> |
| 37 | [int putc(int char, FILE \*stream)](./functions/putc.md)<br>Writes a character (an unsigned char) specified by the argument char to the specified stream and advances the position indicator for the stream.<br> |
| 38 | [int putchar(int char)](./functions/putchar.md)<br>Writes a character (an unsigned char) specified by the argument char to stdout.<br> |
| 39 | [int puts(const char \*str)](./functions/puts.md)<br>Writes a string to stdout up to but not including the null character. A newline character is appended to the output.<br> |
| 40 | [int ungetc(int char, FILE \*stream)](./functions/ungetc.md)<br>Pushes the character char (an unsigned char) onto the specified stream so that the next character is read.<br> |
| 41 | [void perror(const char \*str)](./functions/perror.md)<br>Prints a descriptive error message to stderr. First the string str is printed followed by a colon and then a space.<br> |
