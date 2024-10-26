# Class: wstring

The `wstring` class provides a dynamic wide string data structure in NGT. It supports various operations for managing and manipulating wide strings.

## Constructors

### `void wstring()`
- **Description**: Constructs an empty wide string.

### `void wstring(const wstring&in other)`
- **Parameters**:
  - `other` (const wstring&): The other wide string to copy.
- **Description**: Constructs a new wide string by copying another wide string.

## Methods

### `wstring& opAssign(const wstring&in other)`
- **Parameters**:
  - `other` (const wstring&): The other wide string to assign.
- **Return Type**: wstring&
- **Description**: Assigns the contents of another wide string to this wide string and returns a reference to this wide string.

### `wstring& opAddAssign(const wstring&in other)`
- **Parameters**:
  - `other` (const wstring&): The other wide string to append.
- **Return Type**: wstring&
- **Description**: Appends another wide string to the current wide string and returns a reference to this wide string.

### `void clear()`
- **Description**: Clears the content of the wide string, making it empty.

### `uint64 c_str()`
- **Return Type**: uint64
- **Description**: Returns a pointer to the underlying C-style wide string representation.
