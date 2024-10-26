## Engine Configuration

### `string get_engine_config() property`
- **Return Type**: string
- **Description**: Retrieves configuration settings of the AngelScript engine as a property.

## Function Registration

### `int register_function(const string&in func_sig, uint64 func_pointer, callconv conv)`
- **Parameters**:
  - `func_sig` (const string&): The signature under which the function will be registered.
  - `func_pointer` (uint64): A pointer to the function implementation.
  - `conv` (callconv): The calling convention of the function.
- **Return Type**: int
- **Description**: Registers a native function with the AngelScript engine.

## Error Handling

### `string get_messages(bool = true, bool = true, bool = false)`
- **Parameters**:
  - `include_errors` (bool): Optional flag to include error messages.
  - `include_warnings` (bool): Optional flag to include warning messages.
  - `include_info` (bool): Optional flag to include information messages.
- **Return Type**: string
- **Description**: Retrieves messages from the AngelScript engine.

### `void clear_messages()`
- **Description**: Clears any accumulated messages in the AngelScript engine.

## Low-Level Memory and Argument Handling

### `uint64 get_arg_address(?&in arg)`
- **Parameters**:
  - `arg` (?&): The argument to get the address of.
- **Return Type**: uint64
- **Description**: Retrieves the memory address of an argument passed to a script function.

### `uint64 get_address_of_arg(?&in arg)`
- **Parameters**:
  - `arg` (?&): The argument to get the address of.
- **Return Type**: uint64
- **Description**: Retrieves the memory address of an argument within an AngelScript context.

### `int get_arg_type_id(?&in arg)`
- **Parameters**:
  - `arg` (?&): The argument to get the type ID for.
- **Return Type**: int
- **Description**: Retrieves the type ID of an argument passed to a script function.

## Function Retrieval

### `function@ get_function_by_id(int id)`
- **Parameters**:
  - `id` (int): The ID of the function to retrieve.
- **Return Type**: function@
- **Description**: Retrieves a scripting::function object by its ID.

### `function@ get_function_by_decl(const string&in decl)`
- **Parameters**:
  - `decl` (const string&): The declaration of the function to retrieve.
- **Return Type**: function@
- **Description**: Retrieves a scripting::function object by its declaration.

## Context Management

### `context@ get_active_context() property`
- **Return Type**: context@
- **Description**: Retrieves the currently active scripting execution context as a property.

## Locking Mechanisms

### `void acquire_exclusive_lock()`
- **Description**: Acquires an exclusive lock to ensure no other thread can access shared resources during critical sections.

### `void release_exclusive_lock()`
- **Description**: Releases the exclusive lock after completing critical operations.

### `void acquire_shared_lock()`
- **Description**: Acquires a shared lock to allow multiple threads to read shared resources simultaneously, but prevent writes.

### `void release_shared_lock()`
- **Description**: Releases the shared lock after completing read operations.
