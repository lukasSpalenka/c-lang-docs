---
created: 2023-01-12T21:12:26 (UTC +01:00)
tags: []

author: 
---

# C Library - <math.h>

> ## Excerpt
> C Library - <math.h>,  The math.h header defines various mathematical functions and one macro. All the functions available in this library take double as an argument and return double

---
---

The **math.h** header defines various mathematical functions and one macro. All the functions available in this library take **double** as an argument and return **double** as the result.

## Library Macros

There is only one macro defined in this library −

| Sr.No. | Macro & Description |
| --- | --- |
| 1 |  **HUGE\_VAL**<br>This macro is used when the result of a function may not be representable as a floating point number. If magnitude of the correct result is too large to be represented, the function sets errno to ERANGE to indicate a range error, and returns a particular, very large value named by the macro HUGE\_VAL or its negation (- HUGE\_VAL).<br>If the magnitude of the result is too small, a value of zero is returned instead. In this case, errno might or might not be set to ERANGE.<br> |

## Library Functions

Following are the functions defined in the header math.h −

| Sr.No. | Function & Description |
| --- | --- |
| 1 | [double acos(double x)](./functions/acos.md) Returns the arc cosine of x in radians.<br> |
| 2 | [double asin(double x)](./functions/asin.md)<br>Returns the arc sine of x in radians.<br> |
| 3 | [double atan(double x)](./functions/atan.md)<br>Returns the arc tangent of x in radians.<br> |
| 4 | [double atan2(double y, double x)](./functions/atan2.md)<br>Returns the arc tangent in radians of y/x based on the signs of both values to determine the correct quadrant.<br> |
| 5 | [double cos(double x)](./functions/cos.md)<br>Returns the cosine of a radian angle x.<br> |
| 7 | [double sin(double x)](./functions/sin.md)<br>Returns the sine of a radian angle x.<br> |
| 10 | [double exp(double x)](./functions/exp.md)<br>Returns the value of **e** raised to the xth power.<br> |
| 11 | [double frexp(double x, int \*exponent)](./functions/frexp.md)<br>The returned value is the mantissa and the integer pointed to by exponent is the exponent. The resultant value is x = mantissa \* 2 ^ exponent.<br> |
| 12 | [double ldexp(double x, int exponent)](./functions/ldexp.md)<br>Returns **x** multiplied by 2 raised to the power of exponent.<br> |
| 13 | [double log(double x)](./functions/log.md)<br>Returns the natural logarithm (base-e logarithm) of **x**.<br> |
| 14 | [double log10(double x)](./functions/log10.md)<br>Returns the common logarithm (base-10 logarithm) of **x**.<br> |
| 15 | [double modf(double x, double \*integer)](./functions/modf.md)<br>The returned value is the fraction component (part after the decimal), and sets integer to the integer component.<br> |
| 16 | [double pow(double x, double y)](./functions/pow.md)<br>Returns x raised to the power of **y**.<br> |
| 17 | [double sqrt(double x)](./functions/sqrt.md)<br>Returns the square root of **x**.<br> |
| 18 | [double ceil(double x)](./functions/ceil.md)<br>Returns the smallest integer value greater than or equal to **x**.<br> |
| 19 | [double fabs(double x)](./functions/fabs.md)<br>Returns the absolute value of **x**.<br> |
| 20 | [double floor(double x)](./functions/floor.md)<br>Returns the largest integer value less than or equal to **x**.<br> |
| 21 | [double fmod(double x, double y)](./functions/fmod.md)<br>Returns the remainder of x divided by **y**.<br> |
