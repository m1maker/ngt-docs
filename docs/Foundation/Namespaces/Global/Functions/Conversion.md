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

### `string ascii_to_character(int ascii)`
- **Parameters**:
  - `ascii` (int): The ASCII value of the character.
- **Return Type**: string
- **Description**: Converts an ASCII value to its corresponding character as a string.

### `int character_to_ascii(const string&in character)`
- **Parameters**:
  - `character` (const string&): A single character as a string.
- **Return Type**: int
- **Description**: Converts the specified character to its corresponding ASCII value.

### `string hex_to_string(const string&in the_hexadecimal_sequence)`
- **Parameters**:
  - `the_hexadecimal_sequence` (const string&): The hexadecimal sequence to convert.
- **Return Type**: string
- **Description**: Converts a hexadecimal sequence to its corresponding string.

### `string number_to_hex_string(int64 the_number)`
- **Parameters**:
  - `the_number` (int64): The number to convert to a hexadecimal string.
- **Return Type**: string
- **Description**: Converts an integer to its hexadecimal string representation.

## Base Encoding

### `string string_base64_decode(const string&in base64_encoded_string)`
- **Parameters**:
  - `base64_encoded_string` (const string&): The Base64-encoded string.
- **Return Type**: string
- **Description**: Decodes a Base64-encoded string and returns the original string.

### `string string_base64_encode(const string&in the_string)`
- **Parameters**:
  - `the_string` (const string&): The string to encode in Base64.
- **Return Type**: string
- **Description**: Encodes a string into its Base64 representation.

### `string string_base32_decode(const string&in base32_encoded_string)`
- **Parameters**:
  - `base32_encoded_string` (const string&): The Base32-encoded string.
- **Return Type**: string
- **Description**: Decodes a Base32-encoded string and returns the original string.

### `string string_base32_encode(const string&in the_string)`
- **Parameters**:
  - `the_string` (const string&): The string to encode in Base32.
- **Return Type**: string
- **Description**: Encodes a string into its Base32 representation.

### `string string_to_hex(const string&in the_string)`
- **Parameters**:
  - `the_string` (const string&): The string to convert to hexadecimal.
- **Return Type**: string
- **Description**: Converts a string to a hexadecimal representation.

### `void unicode_convert(const string&in utf8_string, wstring&out wide_string)`
- **Parameters**:
  - `utf8_string` (const string&): The UTF-8 encoded string.
  - `wide_string` (wstring&out): Output parameter for the converted wide string.
- **Description**: Converts an UTF-8 encoded string to a wide string.

### `void unicode_convert(const wstring&in wide_string, string&out utf8_string)`
- **Parameters**:
  - `wide_string` (const wstring&): The wide string.
  - `utf8_string` (string&out): Output parameter for the converted UTF-8 encoded string.
- **Description**: Converts a wide string to an UTF-8 encoded string.
