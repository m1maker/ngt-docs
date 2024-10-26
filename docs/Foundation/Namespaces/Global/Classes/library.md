# Class: library

The `library` class provides a data structure for managing dynamic libraries (DLLs or shared objects) in NGT. It allows you to load, unload, retrieve function pointers, and manage the functions within the loaded library.

## Constructors

### `library()`
- **Description**: Constructs an empty `library` object ready to load and interact with a dynamic library.

## Methods

### `bool load(const string&in library_path) const`
- **Parameters**:
  - `library_path` (const string&): The path to the dynamic library to load.
- **Return Type**: bool
- **Description**: Loads a dynamic library from the specified path and returns `true` if successful; otherwise, returns `false`.

### `bool get_active() const property`
- **Return Type**: bool
- **Description**: Returns whether the library is currently loaded as a property.

### `void unload() const`
- **Description**: Unloads the currently loaded dynamic library.

### `uint64 get_function_pointer(const string&in function_name) const`
- **Parameters**:
  - `function_name` (const string&): The name of the function to retrieve.
- **Return Type**: uint64
- **Description**: Retrieves a pointer to the specified function within the loaded library and returns it as a `uint64`.

### `void clear_functions() const`
- **Description**: Clears any stored function pointers from the library object, freeing up memory if necessary.
