## System and Environment

### `void set_exit_callback(exit_callback@ = null)`
- **Parameters**:
  - `callback` (exit_callback@): An optional callback function to be called when the application is exiting.
- **Description**: Sets a callback function that will be invoked when the application is exiting.

### `void set_library_path(const string&in path)`
- **Parameters**:
  - `path` (const string&): The path to the library directory.
- **Description**: Sets the path where libraries should be loaded from.

### `void exit(int retcode = 0)`
- **Parameters**:
  - `retcode` (int): The return code to use when exiting the application.
- **Description**: Exits the application with the specified return code.

### `bool get_quit_requested() property`
- **Return Type**: bool
- **Description**: Gets a flag indicating whether the quit operation has been requested as a property.
