![img](https://assets.imaginablefutures.com/media/images/ALX_Logo.max-200x150.png)
> printf project

By: Teresiah Nduati and Nkwairanransome

## About 
In this project, we are required to implement the ```printf``` function in C from scratch 


## Resources 
1. [Secrets of printf](https://www.academia.edu/10297206/Secrets_of_printf_)

## Man/Help 
- printf(3)

## Authorized funtions / macros
    write (man 2 write)
    malloc (man 3 malloc)
    free (man 3 free)
    va_start (man 3 va_start)
    va_end (man 3 va_end)
    va_copy (man 3 va_copy)
    va_arg (man 3 va_arg)

## Compilation
Your code will be compiled with the following flags 

~~
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c

~~
This project entails the implementation of the printf function within the C standard library.

How to Use:
To utilize the function, include the "main.h" header before implementation. The _printf function returns the count of characters printed to stdout.

##
	#include "main.h"

int main(void) {
    int n = _printf("Wind: %d%s and Precipitation: %d%%\n", 28, "km/h", 0x1a);
    return (0);
}

##

Format Specifier Pattern:
The format specifier follows the pattern: %[flag][width][.precision][length]specifier. These fields are optional, but a specifier is mandatory, and they must be arranged in the specified order. If a specifier is missing (or invalid), and it's at the end of the format string, an error occurs. Conversely, if a specifier is absent (or invalid) and not at the end of the string, the raw, invalid specifier is printed as is.

Supported Flags:

#: Converts the value to an alternate form.
0: Pads the value with zeros instead of spaces.
-: Left-aligns the output on the field boundary, as the default is right-alignment.
A blank space is left before a positive number produced by a sign conversion if the flag is a space, and a sign (+ or -) is placed before a number produced by a signed conversion. By default, only the signs of negative numbers are shown.

Width and Precision:
The width and precision fields can be integers starting with a non-zero digit or specified with the * sign. If specified with *, the value is read from the argument list provided to _printf. The maximum value for these fields is 2147483647.

Supported Length Modifiers:

h: Prints the ASCII character representation of an integer.
l: Modifies the integer to be a long signed or unsigned integer.
Supported Conversion Specifiers:

c: Prints the ASCII character representation of an integer.
s: Prints the characters of a char * terminated by a null character (\0).
d, i: Prints the signed decimal notation of an integer argument.
f: Prints the signed decimal notation of an IEEE 754 floating-point argument.
o, u, x, X: Prints the unsigned int argument in unsigned octal notation (o), decimal notation (u), or hexadecimal notation (x and X). Lowercase hexadecimal characters are used for x, while uppercase is used for X.
%: Prints the "%" sign only.
p: Prints a void * argument in hexadecimal form.
b: Prints the binary representation of an unsigned integer.
R: Prints the rot13 translation of a string.
r: Prints the reverse of a string.
S: Prints a string and the hexadecimal representation of unprintable characters (prefixed with \x) in a null-terminated string.
Examples:

_printf("%.2f\n", -3.46) produces -3.46.
_printf("%#x\n", 478) produces 0x1de.
_printf("%R\n", "foobar") produces sbbone.
_printf("%r\n", "foo") produces oof.
