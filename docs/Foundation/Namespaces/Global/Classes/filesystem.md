# Class: filesystem

The `filesystem` class provides methods for interacting with the file system in NGT. It allows you to perform operations such as checking file and directory existence, changing paths, copying files, and retrieving file properties.

## Methods

### `bool file_exists(const string&in path)`
- **Parameters**:
  - `path` (const string&): The path to check for a file.
- **Return Type**: bool
- **Description**: Checks if a file exists at the specified path and returns `true` if it does; otherwise, returns `false`.

### `bool dir_exists(const string&in path)`
- **Parameters**:
  - `path` (const string&): The path to check for a directory.
- **Return Type**: bool
- **Description**: Checks if a directory exists at the specified path and returns `true` if it does; otherwise, returns `false`.

### `bool change_current_path(const string&in new_path)`
- **Parameters**:
  - `new_path` (const string&): The new current working directory.
- **Return Type**: bool
- **Description**: Changes the current working directory to the specified path and returns `true` if successful; otherwise, returns `false`.

### `string get_current_path() const property`
- **Return Type**: string
- **Description**: Returns the current working directory as a property.

### `array<string>@ get_dirs() const property`
- **Return Type**: array<string>
- **Description**: Returns an array of directory names in the current directory as a property.

### `array<string>@ get_files(string filter = "*") const`
- **Parameters**:
  - `filter` (string): The file name pattern to match.
- **Return Type**: array<string>
- **Description**: Returns an array of filenames that match the specified filter in the current directory.

### `bool is_dir(const string&in path) const`
- **Parameters**:
  - `path` (const string&): The path to check if it's a directory.
- **Return Type**: bool
- **Description**: Checks if the specified path is a directory and returns `true` if it is; otherwise, returns `false`.

### `bool is_link(const string&in path) const`
- **Parameters**:
  - `path` (const string&): The path to check if it's a symbolic link.
- **Return Type**: bool
- **Description**: Checks if the specified path is a symbolic link and returns `true` if it is; otherwise, returns `false`.

### `int64 get_size(const string&in path) const`
- **Parameters**:
  - `path` (const string&): The path to get the size of.
- **Return Type**: int64
- **Description**: Returns the size of the specified file or directory in bytes.

### `int make_dir(const string&in path)`
- **Parameters**:
  - `path` (const string&): The path for the new directory.
- **Return Type**: int
- **Description**: Creates a new directory at the specified path and returns an error code if the operation fails.

### `int remove_dir(const string&in path)`
- **Parameters**:
  - `path` (const string&): The path of the directory to remove.
- **Return Type**: int
- **Description**: Removes the directory at the specified path and returns an error code if the operation fails.

### `int delete_file(const string&in path)`
- **Parameters**:
  - `path` (const string&): The path of the file to delete.
- **Return Type**: int
- **Description**: Deletes the file at the specified path and returns an error code if the operation fails.

### `int copy_file(const string&in source, const string&in destination)`
- **Parameters**:
  - `source` (const string&): The path of the source file.
  - `destination` (const string&): The path of the destination file.
- **Return Type**: int
- **Description**: Copies a file from the source to the destination and returns an error code if the operation fails.

### `int move(const string&in source, const string&in destination)`
- **Parameters**:
  - `source` (const string&): The path of the source file or directory.
  - `destination` (const string&): The path of the destination file or directory.
- **Return Type**: int
- **Description**: Moves a file or directory from the source to the destination and returns an error code if the operation fails.

### `datetime get_create_date_time(const string&in path) const`
- **Parameters**:
  - `path` (const string&): The path of the file or directory.
- **Return Type**: datetime
- **Description**: Returns the creation date and time of the specified file or directory as a datetime object.

### `datetime get_modify_date_time(const string&in path) const`
- **Parameters**:
  - `path` (const string&): The path of the file or directory.
- **Return Type**: datetime
- **Description**: Returns the last modification date and time of the specified file or directory as a datetime object.
