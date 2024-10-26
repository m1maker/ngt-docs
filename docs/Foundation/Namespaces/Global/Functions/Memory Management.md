## Memory Management

### `uint64 malloc(uint64 alloc_size)`
- **Parameters**:
  - `alloc_size` (uint64): The size of the memory to allocate in bytes.
- **Return Type**: uint64
- **Description**: Allocates a block of memory and returns a pointer to it.

### `uint64 calloc(uint64 num, uint64 size)`
- **Parameters**:
  - `num` (uint64): The number of elements to allocate.
  - `size` (uint64): The size of each element in bytes.
- **Return Type**: uint64
- **Description**: Allocates and initializes a block of memory with zeros and returns a pointer to it.

### `uint64 realloc(uint64 ptr, uint64 new_size)`
- **Parameters**:
  - `ptr` (uint64): The pointer to the previously allocated memory.
  - `new_size` (uint64): The new size of the memory block in bytes.
- **Return Type**: uint64
- **Description**: Reallocates a block of memory to a new size and returns a pointer to the new block.

### `void free(uint64 ptr)`
- **Parameters**:
  - `ptr` (uint64): The pointer to the memory block to free.
- **Description**: Frees a previously allocated block of memory.

### `uint64 memcpy(uint64 dest, uint64 src, uint64 n)`
- **Parameters**:
  - `dest` (uint64): The destination memory address.
  - `src` (uint64): The source memory address.
  - `n` (uint64): The number of bytes to copy.
- **Return Type**: uint64
- **Description**: Copies `n` bytes from the source memory block to the destination memory block.

## String and Memory Conversion

### `string c_str_to_string(uint64 array_pointer, uint64 string_length = 0)`
- **Parameters**:
  - `array_pointer` (uint64): The pointer to the C-style null-terminated string.
  - `string_length` (uint64): Optional length of the string if not null-terminated.
- **Return Type**: string
- **Description**: Converts a C-style null-terminated string to an AngelScript string.

### `wstring wc_str_to_wstring(uint64 array_pointer, uint64 string_length = 0)`
- **Parameters**:
  - `array_pointer` (uint64): The pointer to the wide character string.
  - `string_length` (uint64): Optional length of the string if not null-terminated.
- **Return Type**: wstring
- **Description**: Converts a wide character string to an AngelScript wide string.

### `uint64 c_str_len(uint64 array_pointer)`
- **Parameters**:
  - `array_pointer` (uint64): The pointer to the C-style null-terminated string.
- **Return Type**: uint64
- **Description**: Returns the length of a C-style null-terminated string.

### `uint64 wc_str_len(uint64 array_pointer)`
- **Parameters**:
  - `array_pointer` (uint64): The pointer to the wide character string.
- **Return Type**: uint64
- **Description**: Returns the length of a wide character string.

### `uint64 sizeof(const ?&in arg = null)`
- **Parameters**:
  - `arg` (?&): The argument to get the size of.
- **Return Type**: uint64
- **Description**: Retrieves the memory size required for an argument, with a default value if no argument is provided.
