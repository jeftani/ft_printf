# ft_printf
42 ft_printf
This code is a C program that implements a custom version of the C standard library function printf(). It uses a variable number of arguments, specified by the ellipsis (...) in the function definition, and allows for the use of certain format specifiers (such as %c, %x, %p, %s, %d, %i, %u, %%) to format and print data. The program iterates through the format string passed as the first argument, and when it encounters a format specifier, it uses the corresponding function from ft_format to handle the variable argument. The variable argument is passed using the va_list object, va_start,
va_arg and va_end. The function returns the number of characters printed.
