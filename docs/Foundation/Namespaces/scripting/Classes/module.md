# Class: module

The `module` class provides a data structure for managing script modules in AngelScript. It allows you to add script sections, build the module, retrieve bytecode, and manage functions within the module.

## Constructors

### `scripting::module(const string&in)`
- **Parameters**:
  - `string`: The name of the module.
- **Description**: Constructs a new `module` object with the specified name.

## Methods

### `int add_script_section(const string&in, const string&in) const`
- **Parameters**:
  - `script_name` (const string&): The name of the script section.
  - `script_code` (const string&): The code of the script section.
- **Return Type**: int
- **Description**: Adds a new script section to the module and returns an error code if any issues occur.

### `int build() const`
- **Return Type**: int
- **Description**: Builds the module from added script sections, compiling the script code and returning an error code if any issues occur.

### `int discard() const`
- **Return Type**: int
- **Description**: Discards all resources associated with the module and returns an error code if any issues occur.

### `string get_byte_code(bool strip_debug = true) const`
- **Parameters**:
  - `strip_debug` (bool): A flag indicating whether to include debug information into  bytecode.
- **Return Type**: string
- **Description**: Retrieves a string containing the bytecode of the module, optionally including debug information.

### `int set_byte_code(const string&in) const`
- **Parameters**:
  - `bytecode` (const string&): The new bytecode for the module.
- **Return Type**: int
- **Description**: Sets new bytecode for the module and returns an error code if any issues occur.

### `scripting::function@ get_function_by_index(int index) const`
- **Parameters**:
  - `index` (int): The index of the function to retrieve.
- **Return Type**: scripting::function@
- **Description**: Retrieves a script function by its index and returns it.

### `scripting::function@ get_function_by_decl(const string&in) const`
- **Parameters**:
  - `declaration` (const string&): The declaration of the function to retrieve.
- **Return Type**: scripting::function@
- **Description**: Retrieves a script function by its declaration and returns it.

### `scripting::function@ get_function_by_name(const string&in) const`
- **Parameters**:
  - `name` (const string&): The name of the function to retrieve.
- **Return Type**: scripting::function@
- **Description**: Retrieves a script function by its name and returns it.

### `int bind_all_imported_functions() const`
- **Return Type**: int
- **Description**: Binds all imported functions to their implementations and returns an error code if any issues occur.

### `int unbind_all_imported_functions() const`
- **Return Type**: int
- **Description**: Unbinds all imported functions from their implementations and returns an error code if any issues occur.

### `int bind_imported_function(uint index, scripting::function@ func) const`
- **Parameters**:
  - `index` (uint): The index of the imported function to bind.
  - `func` (scripting::function@): The function implementation to bind.
- **Return Type**: int
- **Description**: Binds a specific imported function to its implementation and returns an error code if any issues occur.

### `int unbind_imported_function(uint index) const`
- **Parameters**:
  - `index` (uint): The index of the imported function to unbind.
- **Return Type**: int
- **Description**: Unbinds a specific imported function from its implementation and returns an error code if any issues occur.
