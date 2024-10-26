# Class: dictionary

The `dictionary` class provides a dynamic key-value data structure in NGT. It supports various operations for managing and manipulating dictionaries.

## Methods

### `dictionary& opAssign(const dictionary&in other)`
- **Parameters**:
  - `other` (const dictionary&): The other dictionary to assign.
- **Return Type**: dictionary&
- **Description**: Assigns the contents of another dictionary to this dictionary and returns a reference to this dictionary.

### `void set(const string&in key, const ?&in value)`
- **Parameters**:
  - `key` (const string&): The key for the new or existing entry.
  - `value` (const ?&): The value associated with the key.
- **Description**: Sets a new entry in the dictionary or updates an existing one.

### `bool get(const string&in key, ?&out value) const`
- **Parameters**:
  - `key` (const string&): The key to retrieve.
  - `value` (?&out): Output parameter for the retrieved value.
- **Return Type**: bool
- **Description**: Retrieves the value associated with a key and stores it in the output parameter. Returns `true` if the key exists; otherwise, returns `false`.

### `void set(const string&in key, const int64&in value)`
- **Parameters**:
  - `key` (const string&): The key for the new or existing entry.
  - `value` (const int64&): The integer value associated with the key.
- **Description**: Sets a new entry in the dictionary or updates an existing one with an integer value.

### `bool get(const string&in key, int64&out value) const`
- **Parameters**:
  - `key` (const string&): The key to retrieve.
  - `value` (int64&out): Output parameter for the retrieved integer value.
- **Return Type**: bool
- **Description**: Retrieves the integer value associated with a key and stores it in the output parameter. Returns `true` if the key exists; otherwise, returns `false`.

### `void set(const string&in key, const double&in value)`
- **Parameters**:
  - `key` (const string&): The key for the new or existing entry.
  - `value` (const double&): The double precision floating-point value associated with the key.
- **Description**: Sets a new entry in the dictionary or updates an existing one with a double precision floating-point value.

### `bool get(const string&in key, double&out value) const`
- **Parameters**:
  - `key` (const string&): The key to retrieve.
  - `value` (double&out): Output parameter for the retrieved double precision floating-point value.
- **Return Type**: bool
- **Description**: Retrieves the double precision floating-point value associated with a key and stores it in the output parameter. Returns `true` if the key exists; otherwise, returns `false`.

### `bool exists(const string&in key) const`
- **Parameters**:
  - `key` (const string&): The key to check for existence.
- **Return Type**: bool
- **Description**: Checks if a specific key exists in the dictionary.

### `bool is_empty() const`
- **Return Type**: bool
- **Description**: Checks if the dictionary is empty and returns `true` if it is; otherwise, returns `false`.

### `uint get_size() const`
- **Return Type**: uint
- **Description**: Returns the number of key-value pairs in the dictionary.

### `bool delete(const string&in key)`
- **Parameters**:
  - `key` (const string&): The key to remove.
- **Return Type**: bool
- **Description**: Removes an entry from the dictionary based on a given key and returns `true` if the key existed; otherwise, returns `false`.

### `void delete_all()`
- **Description**: Deletes all entries in the dictionary.

### `array<string>@ get_keys() const`
- **Return Type**: array<string>
- **Description**: Returns an array containing all keys from the dictionary.
