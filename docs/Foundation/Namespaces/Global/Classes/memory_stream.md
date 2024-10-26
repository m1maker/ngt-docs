# Class: memory_stream

The `memory_stream` class provides a data structure for in-memory input/output operations in NGT. It allows you to perform read and write operations directly on the stream's buffer without interacting with external files or devices.

## Constructors

### `memory_stream(uint64 size = 0)`
- **Parameters**:
  - `size` (uint64): The initial size of the memory buffer.
- **Description**: Constructs a new `memory_stream` object with an optional initial size for the internal buffer.


## Methods

### `void write(const string&in)`
- **Parameters**:
  - `string`: The string to write.
- **Description**: Writes the specified string to the end of the memory stream.

### `void read(string&out, uint64 size)`
- **Parameters**:
  - `string&out`: Output parameter for the read data.
  - `size` (uint64): The number of bytes to read from the stream.
- **Description**: Reads a specified number of bytes from the memory stream and stores them in the output string.

### `void write(uint64 value, uint64 size)`
- **Parameters**:
  - `value` (uint64): The value to write.
  - `size` (uint64): The number of bytes to write.
- **Description**: Writes a specified value into the memory stream as raw binary data.

### `void read(uint64&out, uint64 size)`
- **Parameters**:
  - `uint64&out`: Output parameter for the read value.
  - `size` (uint64): The number of bytes to read from the stream.
- **Description**: Reads a specified number of bytes from the memory stream as raw binary data and stores them in the output value.

### `void seek(int offset)`
- **Parameters**:
  - `offset` (int): The offset relative to the current position to move to.
- **Description**: Seeks to a new position within the memory stream by moving the current position forward or backward by the specified offset.

### `void seek(seek_origin origin, int offset)`
- **Parameters**:
  - `origin` (seek_origin): The origin from which to calculate the new position (e.g., beginning, current position, end).
  - `offset` (int): The offset relative to the origin to move to.
- **Description**: Seeks to a new position within the memory stream based on the specified origin and offset.

### `uint64 tell() const`
- **Return Type**: uint64
- **Description**: Returns the current position in the memory stream.

### `uint64 get_size() const property`
- **Return Type**: uint64
- **Description**: Returns the total size of the memory buffer as a property.

### `void clear() const`
- **Description**: Clears the contents of the memory stream, resetting it to an empty state.
