# Class: context

The `context` class provides a data structure for managing the execution of AngelScript scripts. It allows you to prepare, execute, and abort script functions dynamically, handling arguments and return values as needed.

## Constructors

### `scripting::context()`
- **Description**: Constructs an empty `context` object ready to execute a script function.

## Methods

### `int prepare(scripting::function@ func) const`
- **Parameters**:
  - `func` (scripting::function@): The function to prepare for execution.
- **Return Type**: int
- **Description**: Prepares the script function for execution and returns an error code if any issues occur.

### `int unprepare() const`
- **Return Type**: int
- **Description**: Unprepares the currently prepared script function and returns an error code if any issues occur.

### `int execute() const`
- **Return Type**: int
- **Description**: Executes the prepared script function and returns an error code or the execution status.

### `int abort() const`
- **Return Type**: int
- **Description**: Aborts the currently executing script function and returns an error code if any issues occur.

### `int suspend() const`
- **Return Type**: int
- **Description**: Suspends the currently executing script function and returns an error code if any issues occur.

### `scripting::ctxstate get_state() const`
- **Return Type**: scripting::ctxstate
- **Description**: Returns the current state of the execution context (e.g., running, suspended, aborted).

### `int push_state() const`
- **Return Type**: int
- **Description**: Pushes the current state onto a stack and returns an error code if any issues occur.

### `int pop_state() const`
- **Return Type**: int
- **Description**: Pops the most recent state from the stack and returns an error code if any issues occur.

### `int set_arg_byte(uint index, int8 value) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (int8): The byte value to set as an argument.
- **Return Type**: int
- **Description**: Sets a byte value as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_word(uint index, int16 value) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (int16): The word value to set as an argument.
- **Return Type**: int
- **Description**: Sets a word value as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_dword(uint index, int value) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (int): The dword (32-bit integer) value to set as an argument.
- **Return Type**: int
- **Description**: Sets a dword (32-bit integer) value as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_qword(uint index, int64 value) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (int64): The qword (64-bit integer) value to set as an argument.
- **Return Type**: int
- **Description**: Sets a qword (64-bit integer) value as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_float(uint index, float value) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (float): The float value to set as an argument.
- **Return Type**: int
- **Description**: Sets a float value as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_double(uint index, double value) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (double): The double value to set as an argument.
- **Return Type**: int
- **Description**: Sets a double value as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_address(uint index, uint64 address) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `address` (uint64): The memory address to set as an argument.
- **Return Type**: int
- **Description**: Sets a memory address as an argument for the script function and returns an error code if any issues occur.

### `int set_arg_var_type(uint index, uint64 value, scripting::typeid type) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
  - `value` (uint64): The value to set as an argument.
  - `type` (scripting::typeid): The type of the argument.
- **Return Type**: int
- **Description**: Sets a value with its corresponding type as an argument for the script function and returns an error code if any issues occur.

### `uint64 get_address_of_arg(uint index) const`
- **Parameters**:
  - `index` (uint): The index of the argument.
- **Return Type**: uint64
- **Description**: Returns the memory address of a specific argument in the script function.

### `int8 get_return_byte() const`
- **Return Type**: int8
- **Description**: Retrieves the return value as an 8-bit integer if it matches the expected type.

### `int16 get_return_word() const`
- **Return Type**: int16
- **Description**: Retrieves the return value as a 16-bit integer if it matches the expected type.

### `int get_return_dword() const`
- **Return Type**: int
- **Description**: Retrieves the return value as a 32-bit integer if it matches the expected type.

### `int64 get_return_qword() const`
- **Return Type**: int64
- **Description**: Retrieves the return value as a 64-bit integer if it matches the expected type.

### `float get_return_float() const`
- **Return Type**: float
- **Description**: Retrieves the return value as a float if it matches the expected type.

### `double get_return_double() const`
- **Return Type**: double
- **Description**: Retrieves the return value as a double if it matches the expected type.

### `uint64 get_return_address() const`
- **Return Type**: uint64
- **Description**: Retrieves the return value as a memory address if it matches the expected type.

### `uint64 get_address_of_return_value() const`
- **Return Type**: uint64
- **Description**: Returns the memory address where the return value is stored.

### `string get_exception_info(bool call_stac = true) const`
- **Parameters**:
  - `call_stac` (bool): A flag indicating whether to include call stac information.
- **Return Type**: string
- **Description**: Retrieves a string containing information about any exceptions that occurred during script execution.
