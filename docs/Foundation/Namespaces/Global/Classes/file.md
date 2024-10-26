# Class: file

The `file` class provides a data structure for handling file operations in NGT.

## Methods

### `int open(const string&in filename, const string&in mode)`
- **Parameters**:
  - `filename` (const string&): The name of the file to open.
  - `mode` (const string&): The mode in which to open the file (e.g., "r" for read, "w" for write).
- **Return Type**: int
- **Description**: Opens a file with the specified filename and mode and returns an error code if the operation fails.

### `int close()`
- **Return Type**: int
- **Description**: Closes the currently open file and returns an error code if the operation fails.

### `int get_size() const property`
- **Return Type**: int
- **Description**: Returns the size of the file in bytes as a property.

### `bool is_end_of_file() const`
- **Return Type**: bool
- **Description**: Checks if the end of the file has been reached and returns `true` if it has; otherwise, returns `false`.

### `string read(uint length)`
- **Parameters**:
  - `length` (uint): The number of bytes to read.
- **Return Type**: string
- **Description**: Reads a specified number of bytes from the file and returns them as a string.

### `string read_line()`
- **Return Type**: string
- **Description**: Reads a line from the file until it encounters a newline character and returns it.

### `int64 read_int(uint size)`
- **Parameters**:
  - `size` (uint): The size of the integer to read.
- **Return Type**: int64
- **Description**: Reads an integer of specified size from the file and returns it as an `int64`.

### `uint64 read_uint(uint size)`
- **Parameters**:
  - `size` (uint): The size of the unsigned integer to read.
- **Return Type**: uint64
- **Description**: Reads an unsigned integer of specified size from the file and returns it as a `uint64`.

### `float read_float()`
- **Return Type**: float
- **Description**: Reads a floating-point number from the file and returns it.

### `double read_double()`
- **Return Type**: double
- **Description**: Reads a double precision floating-point number from the file and returns it.

### `int write(const string&in data)`
- **Parameters**:
  - `data` (const string&): The string to write to the file.
- **Return Type**: int
- **Description**: Writes a string to the file and returns an error code if the operation fails.

### `int write_int(int64 value, uint size)`
- **Parameters**:
  - `value` (int64): The integer value to write to the file.
  - `size` (uint): The size of the integer to write.
- **Return Type**: int
- **Description**: Writes an integer of specified size to the file and returns an error code if the operation fails.

### `int write_uint(uint64 value, uint size)`
- **Parameters**:
  - `value` (uint64): The unsigned integer value to write to the file.
  - `size` (uint): The size of the unsigned integer to write.
- **Return Type**: int
- **Description**: Writes an unsigned integer of specified size to the file and returns an error code if the operation fails.

### `int write_float(float value)`
- **Parameters**:
  - `value` (float): The floating-point number to write to the file.
- **Return Type**: int
- **Description**: Writes a floating-point number to the file and returns an error code if the operation fails.

### `int write_double(double value)`
- **Parameters**:
  - `value` (double): The double precision floating-point number to write to the file.
- **Return Type**: int
- **Description**: Writes a double precision floating-point number to the file and returns an error code if the operation fails.

### `int get_pos() const property`
- **Return Type**: int
- **Description**: Returns the current position in the file as a property.

### `void set_pos(int pos) const property`
- **Parameters**:
  - `pos` (int): The new position to set.
- **Description**: Sets the current position in the file and returns an error code if the operation fails.

### `int move_pos(int offset)`
- **Parameters**:
  - `offset` (int): The offset from the current position to move.
- **Return Type**: int
- **Description**: Moves the current position in the file by a specified offset and returns an error code if the operation fails.

## Properties

### `most_significant_byte_first`
- **Type**: bool
- **Description**: A property indicating whether the most significant byte should be first when reading or writing integer values.
