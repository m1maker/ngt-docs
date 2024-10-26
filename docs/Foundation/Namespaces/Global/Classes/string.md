# Class: string

The `string` class provides a dynamic string data structure in NGT. It supports various operations for managing and manipulating strings.

## Constructors

### `void string()`
- **Description**: Constructs an empty string.

### `void string(const string&in other)`
- **Parameters**:
  - `other` (const string&): The other string to copy.
- **Description**: Constructs a new string by copying another string.

### `void string(uint64 value)`
- **Parameters**:
  - `value` (uint64): The numeric value to convert into a string.
- **Description**: Constructs a string representing the given unsigned 64-bit integer.

### `void string(int64 value)`
- **Parameters**:
  - `value` (int64): The numeric value to convert into a string.
- **Description**: Constructs a string representing the given signed 64-bit integer.

### `void string(uint value)`
- **Parameters**:
  - `value` (uint): The numeric value to convert into a string.
- **Description**: Constructs a string representing the given unsigned integer.

### `void string(int value)`
- **Parameters**:
  - `value` (int): The numeric value to convert into a string.
- **Description**: Constructs a string representing the given signed integer.

### `void string(double value)`
- **Parameters**:
  - `value` (double): The numeric value to convert into a string.
- **Description**: Constructs a string representing the given double precision floating-point number.

### `void string(float value)`
- **Parameters**:
  - `value` (float): The numeric value to convert into a string.
- **Description**: Constructs a string representing the given single precision floating-point number.

### `void string(bool value)`
- **Parameters**:
  - `value` (bool): The boolean value to convert into a string.
- **Description**: Constructs a string representing the given boolean value.

### `void string(const ?&in, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null)`
- **Parameters**:
  - Multiple parameters (optional): Various types of values to convert into a string.
- **Description**: Constructs a string by formatting the given values in a specific format.

## Methods

### `string& opAssign(const string&in other)`
- **Parameters**:
  - `other` (const string&): The other string to assign.
- **Return Type**: string&
- **Description**: Assigns the contents of another string to this string and returns a reference to this string.

### `string& opAddAssign(const string&in other)`
- **Parameters**:
  - `other` (const string&): The other string to append.
- **Return Type**: string&
- **Description**: Appends another string to the current string and returns a reference to this string.

### `bool opEquals(const string&in other) const`
- **Parameters**:
  - `other` (const string&): The other string to compare.
- **Return Type**: bool
- **Description**: Compares this string with another string for equality and returns `true` if they are equal; otherwise, returns `false`.

### `int opCmp(const string&in other) const`
- **Parameters**:
  - `other` (const string&): The other string to compare.
- **Return Type**: int
- **Description**: Compares this string with another string and returns a value indicating the order of the two strings.

### `string opAdd(const string&in other) const`
- **Parameters**:
  - `other` (const string&): The other string to append.
- **Return Type**: string
- **Description**: Creates a new string by appending another string to this string and returns it.

### `uint length() const`
- **Return Type**: uint
- **Description**: Returns the current length of the string.

### `void resize(uint newLength)`
- **Parameters**:
  - `newLength` (uint): The new size for the string.
- **Description**: Resizes the string to the specified length, potentially changing its contents.

### `bool is_empty() const`
- **Return Type**: bool
- **Description**: Checks if the string is empty and returns `true` if it is; otherwise, returns `false`.

### `string opIndex(uint index)`
- **Parameters**:
  - `index` (uint): The index to access.
- **Return Type**: string
- **Description**: Provides indexed access to the string. Returns a substring starting from the specified index.

### `const string opIndex(uint index) const`
- **Parameters**:
  - `index` (uint): The index to access.
- **Return Type**: const string
- **Description**: Provides indexed access to the string in a read-only manner. Returns a substring starting from the specified index.

### `string& opAssign(double value)`
- **Parameters**:
  - `value` (double): The numeric value to convert into a string and assign.
- **Return Type**: string&
- **Description**: Assigns the string representation of the given double precision floating-point number to this string and returns a reference to this string.

### `string& opAddAssign(double value)`
- **Parameters**:
  - `value` (double): The numeric value to append as a string.
- **Return Type**: string&
- **Description**: Appends the string representation of the given double precision floating-point number to the current string and returns a reference to this string.

### `string opAdd(double value) const`
- **Parameters**:
  - `value` (double): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the string representation of the given double precision floating-point number to the current string and returns it.

### `string opAdd_r(double value) const`
- **Parameters**:
  - `value` (double): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the given double precision floating-point number to the current string and returns it.

### `string& opAssign(float value)`
- **Parameters**:
  - `value` (float): The numeric value to convert into a string and assign.
- **Return Type**: string&
- **Description**: Assigns the string representation of the given single precision floating-point number to this string and returns a reference to this string.

### `string& opAddAssign(float value)`
- **Parameters**:
  - `value` (float): The numeric value to append as a string.
- **Return Type**: string&
- **Description**: Appends the string representation of the given single precision floating-point number to the current string and returns a reference to this string.

### `string opAdd(float value) const`
- **Parameters**:
  - `value` (float): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the string representation of the given single precision floating-point number to the current string and returns it.

### `string opAdd_r(float value) const`
- **Parameters**:
  - `value` (float): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the given single precision floating-point number to the current string and returns it.

### `string& opAssign(int64 value)`
- **Parameters**:
  - `value` (int64): The numeric value to convert into a string and assign.
- **Return Type**: string&
- **Description**: Assigns the string representation of the given signed 64-bit integer to this string and returns a reference to this string.

### `string& opAddAssign(int64 value)`
- **Parameters**:
  - `value` (int64): The numeric value to append as a string.
- **Return Type**: string&
- **Description**: Appends the string representation of the given signed 64-bit integer to the current string and returns a reference to this string.

### `string opAdd(int64 value) const`
- **Parameters**:
  - `value` (int64): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the string representation of the given signed 64-bit integer to the current string and returns it.

### `string opAdd_r(int64 value) const`
- **Parameters**:
  - `value` (int64): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the given signed 64-bit integer to the current string and returns it.

### `string& opAssign(uint64 value)`
- **Parameters**:
  - `value` (uint64): The numeric value to convert into a string and assign.
- **Return Type**: string&
- **Description**: Assigns the string representation of the given unsigned 64-bit integer to this string and returns a reference to this string.

### `string& opAddAssign(uint64 value)`
- **Parameters**:
  - `value` (uint64): The numeric value to append as a string.
- **Return Type**: string&
- **Description**: Appends the string representation of the given unsigned 64-bit integer to the current string and returns a reference to this string.

### `string opAdd(uint64 value) const`
- **Parameters**:
  - `value` (uint64): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the string representation of the given unsigned 64-bit integer to the current string and returns it.

### `string opAdd_r(uint64 value) const`
- **Parameters**:
  - `value` (uint64): The numeric value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the given unsigned 64-bit integer to the current string and returns it.

### `string& opAssign(bool value)`
- **Parameters**:
  - `value` (bool): The boolean value to convert into a string and assign.
- **Return Type**: string&
- **Description**: Assigns the string representation of the given boolean value to this string and returns a reference to this string.

### `string& opAddAssign(bool value)`
- **Parameters**:
  - `value` (bool): The boolean value to append as a string.
- **Return Type**: string&
- **Description**: Appends the string representation of the given boolean value to the current string and returns a reference to this string.

### `string opAdd(bool value) const`
- **Parameters**:
  - `value` (bool): The boolean value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the string representation of the given boolean value to the current string and returns it.

### `string opAdd_r(bool value) const`
- **Parameters**:
  - `value` (bool): The boolean value to append as a string.
- **Return Type**: string
- **Description**: Creates a new string by appending the given boolean value to the current string and returns it.

### `string substr(uint start = 0, int count = -1) const`
- **Parameters**:
  - `start` (uint): The starting index of the substring.
  - `count` (int): The number of characters to include in the substring.
- **Return Type**: string
- **Description**: Returns a substring of the current string from the specified start index and count.

### `int find_first(const string&in substr, uint start = 0) const`
- **Parameters**:
  - `substr` (const string&): The substring to search for.
  - `start` (uint): The starting index for searching.
- **Return Type**: int
- **Description**: Searches for the first occurrence of a substring and returns its index; otherwise, returns `-1`.

### `int find_first_of(const string&in chars, uint start = 0) const`
- **Parameters**:
  - `chars` (const string&): The characters to search for.
  - `start` (uint): The starting index for searching.
- **Return Type**: int
- **Description**: Searches for the first occurrence of any character from a set and returns its index; otherwise, returns `-1`.

### `int find_first_not_of(const string&in chars, uint start = 0) const`
- **Parameters**:
  - `chars` (const string&): The characters to search for.
  - `start` (uint): The starting index for searching.
- **Return Type**: int
- **Description**: Searches for the first occurrence of a character not in a set and returns its index; otherwise, returns `-1`.

### `int find_last(const string&in substr, int start = -1) const`
- **Parameters**:
  - `substr` (const string&): The substring to search for.
  - `start` (int): The starting index for searching in reverse.
- **Return Type**: int
- **Description**: Searches for the last occurrence of a substring and returns its index; otherwise, returns `-1`.

### `int find_last_of(const string&in chars, int start = -1) const`
- **Parameters**:
  - `chars` (const string&): The characters to search for.
  - `start` (int): The starting index for searching in reverse.
- **Return Type**: int
- **Description**: Searches for the last occurrence of any character from a set and returns its index; otherwise, returns `-1`.

### `int find_last_not_of(const string&in chars, int start = -1) const`
- **Parameters**:
  - `chars` (const string&): The characters to search for.
  - `start` (int): The starting index for searching in reverse.
- **Return Type**: int
- **Description**: Searches for the last occurrence of a character not in a set and returns its index; otherwise, returns `-1`.

### `void insert(uint pos, const string&in other)`
- **Parameters**:
  - `pos` (uint): The position at which to insert the substring.
  - `other` (const string&): The substring to insert.
- **Description**: Inserts a substring into the current string at the specified position.

### `void erase(uint pos, int count = -1)`
- **Parameters**:
  - `pos` (uint): The position at which to start erasing.
  - `count` (int): The number of characters to erase.
- **Description**: Erases a substring from the current string starting at the specified position.

### `array<string>@ split(const string&in delimiter) const`
- **Parameters**:
  - `delimiter` (const string&): The delimiter to use for splitting the string.
- **Return Type**: array<string>
- **Description**: Splits the string into an array of substrings based on the specified delimiter.

### `string replace(const string&in old, const string&in new) const`
- **Parameters**:
  - `old` (const string&): The substring to be replaced.
  - `new` (const string&): The new substring.
- **Return Type**: string
- **Description**: Creates a new string with all occurrences of the specified old substring replaced by the new substring.

### `string capitalize() const`
- **Return Type**: string
- **Description**: Returns a new string with the first character capitalized and the rest in lowercase.

### `string upper() const`
- **Return Type**: string
- **Description**: Converts the string to uppercase and returns it.

### `string lower() const`
- **Return Type**: string
- **Description**: Converts the string to lowercase and returns it.

### `array<string>@ split_lines() const`
- **Return Type**: array<string>
- **Description**: Splits the string into an array of substrings, each representing a line.

### `bool ends_with(const string&in suffix) const`
- **Parameters**:
  - `suffix` (const string&): The substring to check if it is at the end.
- **Return Type**: bool
- **Description**: Checks if the string ends with the specified suffix and returns `true` if it does; otherwise, returns `false`.

### `bool starts_with(const string&in prefix) const`
- **Parameters**:
  - `prefix` (const string&): The substring to check if it is at the beginning.
- **Return Type**: bool
- **Description**: Checks if the string starts with the specified prefix and returns `true` if it does; otherwise, returns `false`.

### `bool contains(const string&in substring) const`
- **Parameters**:
  - `substring` (const string&): The substring to search for.
- **Return Type**: bool
- **Description**: Checks if the string contains the specified substring and returns `true` if it does; otherwise, returns `false`.

### `bool is_upper() const`
- **Return Type**: bool
- **Description**: Checks if all characters in the string are uppercase.

### `bool is_lower() const`
- **Return Type**: bool
- **Description**: Checks if all characters in the string are lowercase.

### `string format(const ?&in arg0 = null, const ?&in arg1 = null, const ?&in arg2 = null, const ?&in arg3 = null, const ?&in arg4 = null, const ?&in arg5 = null, const ?&in arg6 = null, const ?&in arg7 = null, const ?&in arg8 = null, const ?&in arg9 = null, const ?&in arg10 = null, const ?&in arg11 = null, const ?&in arg12 = null, const ?&in arg13 = null, const ?&in arg14 = null, const ?&in arg15 = null) const`
- **Parameters**:
  - Multiple parameters (optional): Various types of arguments to format into a string.
- **Return Type**: string
- **Description**: Creates a new string by formatting the given arguments according to a specified format.

### `uint64 c_str()`
- **Return Type**: uint64
- **Description**: Returns a pointer to the underlying C-style string representation.
