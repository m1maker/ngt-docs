# Call Convention Enum

## Overview
The `callconv` enum defines different calling conventions that can be used for function calls in a software application. Calling conventions specify the order in which parameters are passed to functions, who cleans the stack, and where return values are stored.

## Syntax
```angelscript
enum callconv {
    CDECL,
    STDCALL
};
```

## Enum Values
- **CDECL (0)**: The function callee is responsible for cleaning the stack. This convention is commonly used in C and C++.
- **STDCALL (1)**: The function caller is responsible for cleaning the stack. This convention is commonly used in Windows API functions.
