# Class: pack

The `pack` class provides a data structure for handling NGT archive files. It allows you to open, close, list, extract, and add files within an archive.

## Methods

### `bool open(const string&in filename, const string&in open_mode) const`
- **Parameters**:
  - `filename` (const string&): The path to the archive file.
  - `open_mode` (const string&): The mode in which to open the archive ("r" for read, "w" for write).
- **Return Type**: bool
- **Description**: Opens an archive file with the specified filename and mode and returns `true` if successful; otherwise, returns `false`.

### `void close() const`
- **Description**: Closes the currently open archive.

### `bool file_exists(const string&in internal_name) const`
- **Parameters**:
  - `internal_name` (const string&): The internal name of the file within the archive.
- **Return Type**: bool
- **Description**: Checks if a file with the specified internal name exists in the archive and returns `true` if it does; otherwise, returns `false`.

### `void extract_file(const string&in internal_name, const string&in file_on_disk) const`
- **Parameters**:
  - `internal_name` (const string&): The internal name of the file to extract.
  - `file_on_disk` (const string&): The path where the extracted file should be saved on disk.
- **Description**: Extracts a file from the archive with the specified internal name and saves it to the specified location on disk.

### `array<string>@ list_files() const`
- **Return Type**: array<string>
- **Description**: Returns an array of strings containing the names of all files in the archive.

### `void add_file(const string&in file_on_disk, const string&in internal_name) const`
- **Parameters**:
  - `file_on_disk` (const string&): The path to the file on disk to add to the archive.
  - `internal_name` (const string&): The internal name under which the file should be stored in the archive.
- **Description**: Adds a file from the disk to the archive with the specified internal name.

### `string get_file(const string&in filename) const`
- **Parameters**:
  - `filename` (const string&): The path to the file on disk where the contents of the archived file should be saved.
- **Description**: Retrieves a file from the archive and saves its contents to the specified location on disk.

### `uint64 get_file_size(const string&in filename) const`
- **Parameters**:
  - `filename` (const string&): The internal name of the file within the archive.
- **Return Type**: uint64
- **Description**: Returns the size of a file in bytes, specified by its internal name.

### `int get_file_count() const property`
- **Return Type**: int
- **Description**: Returns the number of files contained in the archive as a property.
