# Ft_printf

## Introduction
The **ft_printf** project is a custom implementation of the standard C `printf` function. The goal is to recreate its behavior while deepening the understanding of variadic functions, format specifiers, and buffer management in C.

## Table of Contents
- [Features](#features)
- [Function Prototype](#function-prototype)
- [Supported Conversions](#supported-conversions)
- [Implementation Details](#implementation-details)
- [Compilation](#compilation)
- [Usage](#usage)
- [Testing](#testing)
- [License](#license)

## Features
- Handles various format specifiers
- Supports variadic arguments
- Efficient memory and buffer management
- Custom implementation of conversion functions

## Function Prototype
```c
int ft_printf(const char *format, ...);
```
- **format**: A string containing text and format specifiers.
- **...**: A variable number of arguments to be formatted and printed.
- **Returns**: The total number of characters printed.

## Supported Conversions
The following format specifiers are supported:
- `%c` - Character
- `%s` - String
- `%p` - Pointer address
- `%d` - Integer (decimal)
- `%i` - Integer (decimal)
- `%u` - Unsigned integer
- `%x` - Hexadecimal (lowercase)
- `%X` - Hexadecimal (uppercase)
- `%%` - Prints a percent sign

## Implementation Details
- Uses `va_list` to handle variadic arguments.
- Processes the format string and identifies format specifiers.
- Calls the appropriate function to handle each specifier.
- Outputs formatted text using `write()`.

## Compilation
To compile `ft_printf.c` into a static library:
```sh
gcc -Wall -Wextra -Werror -c ft_printf.c ft_printf_utils.c
ar rcs libftprintf.a ft_printf.o ft_printf_utils.o
```

## Usage
Include `ft_printf.h` in your project and link against the compiled library:

```c
#include "ft_printf.h"

int main() {
    ft_printf("Hello, %s! Your number is %d.\n", "World", 42);
    return 0;
}
```

Compile with:
```sh
gcc main.c -L. -lftprintf -o printf_test
```

## Testing
Run tests with sample inputs:
```sh
./printf_test
```
Expected output:
```
Hello, World! Your number is 42.
```

## License
This project is open-source and can be used for educational purposes.

