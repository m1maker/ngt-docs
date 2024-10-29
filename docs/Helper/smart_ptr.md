# smart_ptr Class Documentation

The `smart_ptr` class in AngelScript provides a simple yet effective way to manage dynamic memory allocation with automatic cleanup, mimicking the behavior of smart pointers in languages like C++. This ensures that dynamically allocated resources are properly freed when they are no longer needed.

## Overview

- **Purpose**: The `smart_ptr` class manages a block of memory and automatically deallocates it when the object is destroyed.
- **Memory Management**: Uses `malloc` for allocation and `free` for deallocation. For resizing, uses `realloc`.
- **Properties**: Provides access to the size of the allocated memory.

## Class Members

### Protected Members
- **handle** (`uint64`): Stores the pointer to the dynamically allocated memory.
- **allocated_size** (`size_t`): Stores the current size of the allocated memory.

### Constructors
- `smart_ptr(size_t _size)`: Initializes a new `smart_ptr` object and allocates memory of size `_size`. If allocation fails, `handle` is set to 0 and `allocated_size` to 0.
- `smart_ptr()`: Default constructor. Initializes an empty `smart_ptr`.

### Destructor
- `~smart_ptr()`: Frees the dynamically allocated memory when the `smart_ptr` object is destroyed.

### Operator Overloads
- `uint64 opImplConv()`: Allows implicit conversion of the `smart_ptr` to a `uint64` type (usually for pointer comparison).
- `string opCast()`: Converts the managed memory to a string using `c_str_to_string`.

### Properties
- **get_size()**: Returns the size of the currently allocated memory.
- **set_size(size_t new_size)**: Resizes the allocated memory. If resizing fails, `handle` is set to 0 and `allocated_size` to 0.

## Example Usage

```angelscript
// Create a smart_ptr managing a buffer of 100 bytes
smart_ptr ptr(100);

// Use the pointer for some operations (e.g., copying data)
if (ptr != null) {
    // Copy data into the allocated memory
    memcpy(ptr, source_data, 100);
}

// Automatically cleans up when ptr goes out of scope
```

## Notes

- The class provides a simple interface to manage dynamic memory, ensuring that resources are properly released when they are no longer needed.
- It handles common errors such as memory allocation failure by setting the `handle` and `allocated_size` to 0.

This `smart_ptr` implementation is useful for scenarios where manual memory management can be error-prone and where automatic cleanup is desired to prevent memory leaks.
