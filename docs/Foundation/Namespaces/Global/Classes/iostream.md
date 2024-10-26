# Class: iostream

The `iostream` class provides a data structure for handling input and output operations in NGT. It allows you to perform basic I/O operations such as writing strings, reading strings, clearing the stream, seeking positions, and retrieving the current position.

## Constructors

### `iostream()`
- **Description**: Constructs an empty `iostream` object.


## Methods

### `void write(const string&in)`
- **Parameters**:
  - `string`: The string to write.
- **Description**: Writes the specified string to the output stream.

### `string read()`
- **Return Type**: string
- **Description**: Reads a line of text from the input stream and returns it as a string.

### `string getline()`
- **Return Type**: string
- **Description**: Reads a line of text from the input stream, including newline characters if present, and returns it as a string.

### `void clear()`
- **Description**: Clears any error flags associated with the stream.

### `void seekg(uint64)`
- **Parameters**:
  - `uint64`: The new position to seek in the input stream.
- **Description**: Seeks to the specified position in the input stream.

### `uint64 tellg()`
- **Return Type**: uint64
- **Description**: Returns the current position in the input stream.

### `void seekp(uint64)`
- **Parameters**:
  - `uint64`: The new position to seek in the output stream.
- **Description**: Seeks to the specified position in the output stream.

### `uint64 tellp()`
- **Return Type**: uint64
- **Description**: Returns the current position in the output stream.

### `string str()`
- **Return Type**: string
- **Description**: Retrieves the contents of the input/output buffer as a string.

### `iostream& opShl(?&in)`
- **Parameters**:
  - `?&`: The value to write.
- **Return Type**: iostream&
- **Description**: Writes the specified value to the output stream and returns the modified stream object.

### `iostream& opShr(?&out)`
- **Parameters**:
  - `?&out`: Output parameter for reading the value.
- **Return Type**: iostream&
- **Description**: Reads a value from the input stream and stores it in the output parameter, then returns the modified stream object.
