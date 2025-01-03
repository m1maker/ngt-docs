## Filesystem Information

### `bool exists(const string&in path)`
- **Return Type**: bool
- **Description**: Checks if the specified file or directory exists at the given path. Returns true if it exists; otherwise, returns false.

### `bool is_directory(const string&in path)`
- **Return Type**: bool
- **Description**: Determines if the specified path refers to a directory. Returns true if it does; otherwise, returns false.

### `string get_current_path() property`
- **Return Type**: string
- **Description**: Retrieves the current working directory of the application as a property.

### `void set_current_path(const string&in path) property`
- **Return Type**: void
- **Description**: Changes the current working directory to the specified new path. The method does not return any value.

### `void list_directory(const string&in path = current_path, array<string>@ files = null, array<string>@ folders = null, const string&in file_pattern = '*', const string&in folder_pattern = '*')`
- **Return Type**: void
- **Description**: Lists all files and directories in the specified path that match the given pattern. If no arrays are provided for storing results, the method will not store them.

### `bool create_directory(const string&in path)`
- **Return Type**: bool
- **Description**: Creates a new directory at the specified path. Returns true if the directory is successfully created; otherwise, returns false.

### `bool remove(const string&in path)`
- **Return Type**: bool
- **Description**: Deletes the file or directory at the specified path. If a directory is deleted and it contains files, those files will also be removed. Returns true if the operation is successful; otherwise, returns false.

### `bool rename(const string&in old, const string&in new)`
- **Return Type**: bool
- **Description**: Renames a file or directory from its current name to a new one. Returns true if the operation is successful; otherwise, returns false.

### `string get_file_extension(const string&in path)`
- **Return Type**: string
- **Description**: Extracts and returns the extension (including the dot) of the specified file path.

### `bool copy(const string&in source, const string&in des)`
- **Return Type**: bool
- **Description**: Copies a file from the source to the destination. Returns true if the operation is successful; otherwise, returns false.

### `bool move(const string&in source, const string&in des)`
- **Return Type**: bool
- **Description**: Moves a file or directory from the source path to the destination path. Similar to renaming but can also be used for moving directories across drives. Returns true if the operation is successful; otherwise, returns false.

### `uint64 get_file_size(const string&in path)`
- **Return Type**: uint64
- **Description**: Retrieves and returns the size of the specified file in bytes.

### `datetime get_last_modified_time(const string&in path)`
- **Return Type**: datetime
- **Description**: Returns the last modified time for the specified file or directory.
