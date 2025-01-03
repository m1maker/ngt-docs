## Input and Output

### `void print(const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null)`
- **Parameters**:
  - `args` (const ?&): Variable arguments to print.
- **Description**: Prints the specified arguments to the standard output.

### `void println(const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null)`
- **Parameters**:
  - `args` (const ?&): Variable arguments to print.
- **Description**: Prints the specified arguments and appends a newline character to the standard output.

### `void printf(const string&in format, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null, const ?&in = null)`
- **Parameters**:
  - `format` (const string&): The format string.
  - `args` (const ?&): Variable arguments to format.
- **Description**: Prints formatted output based on a format string and variable arguments.

### `string get_input()`
- **Return Type**: string
- **Description**: Reads user input from the window and returns it as a string.

### `string input_box(const string&in title, const string&in text, const string&in default_text = "", bool secure = false, bool multiline = false)`
- **Parameters**:
  - `title` (const string&): The title of the input box.
  - `text` (const string&): The prompt or message in the input box.
  - `default_text` (const string&): Optional default text to pre-fill the input field.
  - `secure` (bool): Whether the input is secure (e.g., password).
  - `multiline` (bool): Whether the input allows multiple lines.
- **Return Type**: string
- **Description**: Opens an input box with the specified parameters and returns the user's input as a string.

### `string open_file_dialog(const string&in filters = "", const string&in default_location = "")`
- **Parameters**:
  - `filters` (const string&): A semicolon-separated list of file filters. Each filter is in the format "Description (*.ext)". Default is an empty string, which means no filtering.
  - `default_location` (const string&): The default directory to open when the dialog appears. Default is an empty string, which means using the user's home directory.
- **Return Type**: string
- **Description**: Opens a file dialog for opening files. Returns the path of the selected file if the user chooses one; otherwise, returns an empty string.


### `string save_file_dialog(const string&in filters = "", const string&in default_location = "")`
- **Parameters**:
  - `filters` (const string&): A semicolon-separated list of file filters. Each filter is in the format "Description (*.ext)". Default is an empty string, which means no filtering.
  - `default_location` (const string&): The default directory to open when the dialog appears. Default is an empty string, which means using the user's home directory.
- **Return Type**: string
- **Description**: Opens a file dialog for saving files. Returns the path of the selected file if the user chooses one; otherwise, returns an empty string.


### `string select_folder_dialog(const string&in default_location = "")`
- **Parameters**:
  - `default_location` (const string&): The default directory to open when the dialog appears. Default is an empty string, which means using the user's home directory.
- **Return Type**: string
- **Description**: Opens a folder selection dialog. Returns the path of the selected folder if the user chooses one; otherwise, returns an empty string.

## Standard Streams

### `iostream@ get_cout() property`
- **Return Type**: iostream@
- **Description**: Retrieves the standard output stream (`cout`) as a property.

### `iostream@ get_cin() property`
- **Return Type**: iostream@
- **Description**: Retrieves the standard input stream (`cin`) as a property.

### `iostream@ get_cerr() property`
- **Return Type**: iostream@
- **Description**: Retrieves the standard error stream (`cerr`) as a property.
