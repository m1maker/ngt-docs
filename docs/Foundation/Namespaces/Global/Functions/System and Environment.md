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

### `void abort()`
- **Return Type**: void
- **Description**: Terminates the current program immediately. The exact behavior of this function may vary depending on the implementation and platform, but it typically causes an abnormal termination with no normal cleanup. This function is often used in cases where a fatal error occurs that makes continued execution impossible or unsafe.

### `bool get_quit_requested() property`
- **Return Type**: bool
- **Description**: Gets a flag indicating whether the quit operation has been requested as a property.

### `string read_environment_variable(const string&in var_name)`
- **Parameters**:
  - `var_name` (const string&): The name of the environment variable to read.
- **Return Type**: string
- **Description**: Reads the value of an environment variable.

### `bool write_environment_variable(const string&in var_name, const string&in value)`
- **Parameters**:
  - `var_name` (const string&): The name of the environment variable to set.
  - `value` (const string&): The new value for the environment variable.
- **Return Type**: bool
- **Description**: Sets the value of an environment variable and returns `true` if successful; otherwise, returns `false`.

### `array<string>@ get_char_argv()`
- **Return Type**: array<string>
- **Description**: Retrieves an array of command line arguments passed to the script as a property.

### `int exec(const string&in cmd_line)`
- **Parameters**:
  - `cmd_line` (const string&): The command to execute.
- **Return Type**: int
- **Description**: Executes the system command and returns an error code if any issues occur.

### `int exec(const string&in cmd_line, string&out output)`
- **Parameters**:
  - `cmd_line` (const string&): The command to execute.
  - `output` (string&out): Output parameter for the execution result or error message.
- **Return Type**: int
- **Description**: Executes the system command and stores the result or error in the output parameter.

### `string get_SCRIPT_EXECUTABLE() property`
- **Return Type**: string
- **Description**: Retrieves the name of the currently executable file as a property.

### `string get_SCRIPT_EXECUTABLE_PATH() property`
- **Return Type**: string
- **Description**: Retrieves the path to the currently executable directory as a property.

### `powerstate system_power_info(int&out seconds = void, int&out percent = void)`
- **Parameters**:
  - `seconds` (int&): Optional parameter to store the remaining battery time in seconds.
  - `percent` (int&): Optional parameter to store the current battery percentage.
- **Return Type**: powerstate
- **Description**: Retrieves information about the system's power state. If `seconds` and/or `percent` are provided, they will be set to the remaining battery time and percentage, respectively. The function returns a `powerstate` indicating the current power status (e.g., plugged in, on battery).
