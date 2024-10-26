## Conversion

### `float fp_from_ieee(uint)`
- **Parameters**:
  - `value` (uint): The IEEE 32-bit floating-point value to convert.
- **Return Type**: float
- **Description**: Converts an IEEE 32-bit floating-point value to a native float.

### `uint fp_to_ieee(float)`
- **Parameters**:
  - `value` (float): The native float to convert.
- **Return Type**: uint
- **Description**: Converts a native float to an IEEE 32-bit floating-point value.

### `double fp_from_ieee(uint64)`
- **Parameters**:
  - `value` (uint64): The IEEE 64-bit floating-point value to convert.
- **Return Type**: double
- **Description**: Converts an IEEE 64-bit floating-point value to a native double.

### `uint64 fp_to_ieee(double)`
- **Parameters**:
  - `value` (double): The native double to convert.
- **Return Type**: uint64
- **Description**: Converts a native double to an IEEE 64-bit floating-point value.

### `string number_to_words(uint64 number, bool include_and)`
- **Parameters**:
  - `number` (uint64): The number to convert to words.
  - `include_and` (bool): Whether to include "and" in the word representation.
- **Return Type**: string
- **Description**: Converts a number to its word representation, optionally including "and".

### `string formatInt(int64 val, const string&in options = "", uint width = 0)`
- **Parameters**:
  - `val` (int64): The integer value to format.
  - `options` (const string&): Optional formatting options.
  - `width` (uint): Optional minimum field width for alignment.
- **Return Type**: string
- **Description**: Formats an integer value into a string with optional formatting options.

### `string formatUInt(uint64 val, const string&in options = "", uint width = 0)`
- **Parameters**:
  - `val` (uint64): The unsigned integer value to format.
  - `options` (const string&): Optional formatting options.
  - `width` (uint): Optional minimum field width for alignment.
- **Return Type**: string
- **Description**: Formats an unsigned integer value into a string with optional formatting options.

### `string formatFloat(double val, const string&in options = "", uint width = 0, uint precision = 0)`
- **Parameters**:
  - `val` (double): The floating-point value to format.
  - `options` (const string&): Optional formatting options.
  - `width` (uint): Optional minimum field width for alignment.
  - `precision` (uint): Optional number of decimal places for floating-point values.
- **Return Type**: string
- **Description**: Formats a floating-point value into a string with optional formatting options.

### `double string_to_number(const string&in, uint&out byteCount = 0)`
- **Parameters**:
  - `str` (const string&): The string to convert to a number.
  - `byteCount` (uint&out): Optional output parameter for the number of bytes processed.
- **Return Type**: double
- **Description**: Converts a string to a floating-point number and returns it.
