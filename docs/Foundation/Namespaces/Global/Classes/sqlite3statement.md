# Class: sqlite3statement

The `sqlite3statement` class provides a data structure for executing SQL statements in NGT using SQLite. It allows you to prepare, execute, and retrieve results from SQL queries.

## Constructors

### `sqlite3statement()`
- **Description**: Constructs an empty `sqlite3statement` object ready to be prepared with an SQL statement.

## Methods

### `int step()`
- **Return Type**: int
- **Description**: Advances the statement to the next row in its result set and returns an error code if any issues occur.

### `int reset()`
- **Return Type**: int
- **Description**: Resets the statement to its initial state, ready for re-execution with new parameters.

### `string get_expanded_sql_statement() property`
- **Return Type**: string
- **Description**: Returns the expanded SQL statement with bound parameters as a property.

### `string get_sql_statement() property`
- **Return Type**: string
- **Description**: Returns the original SQL statement used to create this statement object as a property.

### `int get_bind_param_count() property`
- **Return Type**: int
- **Description**: Returns the number of bind parameters in the prepared statement as a property.

### `int get_column_count() property`
- **Return Type**: int
- **Description**: Returns the number of columns in the result set of the executed statement as a property.

### `int bind_blob(int index, const string&in value, bool copy = true)`
- **Parameters**:
  - `index` (int): The parameter index to bind.
  - `value` (const string&): The blob value to bind.
  - `copy` (bool): Optional flag indicating whether to make a copy of the blob data.
- **Return Type**: int
- **Description**: Binds a blob value to a parameter in the statement and returns an error code if any issues occur.

### `int bind_double(int index, double value)`
- **Parameters**:
  - `index` (int): The parameter index to bind.
  - `value` (double): The double value to bind.
- **Return Type**: int
- **Description**: Binds a double value to a parameter in the statement and returns an error code if any issues occur.

### `int bind_int(int index, int value)`
- **Parameters**:
  - `index` (int): The parameter index to bind.
  - `value` (int): The integer value to bind.
- **Return Type**: int
- **Description**: Binds an integer value to a parameter in the statement and returns an error code if any issues occur.

### `int bind_int64(int index, int64 value)`
- **Parameters**:
  - `index` (int): The parameter index to bind.
  - `value` (int64): The 64-bit integer value to bind.
- **Return Type**: int
- **Description**: Binds a 64-bit integer value to a parameter in the statement and returns an error code if any issues occur.

### `int bind_null(int index)`
- **Parameters**:
  - `index` (int): The parameter index to bind.
- **Return Type**: int
- **Description**: Binds a null value to a parameter in the statement and returns an error code if any issues occur.

### `int bind_param_index(const string&in name)`
- **Parameters**:
  - `name` (const string&): The name of the parameter.
- **Return Type**: int
- **Description**: Retrieves the index of a parameter by its name and returns it.

### `string bind_param_name(int index)`
- **Parameters**:
  - `index` (int): The parameter index.
- **Return Type**: string
- **Description**: Retrieves the name of a parameter by its index and returns it.

### `int bind_text(int index, const string&in value, bool copy = true)`
- **Parameters**:
  - `index` (int): The parameter index to bind.
  - `value` (const string&): The text value to bind.
  - `copy` (bool): Optional flag indicating whether to make a copy of the text data.
- **Return Type**: int
- **Description**: Binds a text value to a parameter in the statement and returns an error code if any issues occur.

### `int clear_bindings()`
- **Return Type**: int
- **Description**: Clears all bindings from the statement, resetting it for new parameters, and returns an error code if any issues occur.

### `string column_blob(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: string
- **Description**: Retrieves a blob value from the current row of the result set and returns it.

### `int column_bytes(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: int
- **Description**: Retrieves the size of a blob or text value in bytes for the specified column of the current row.

### `string column_decltype(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: string
- **Description**: Retrieves the declared type of the specified column as a string.

### `double column_double(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: double
- **Description**: Retrieves a double value from the current row of the result set and returns it.

### `int column_int(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: int
- **Description**: Retrieves an integer value from the current row of the result set and returns it.

### `int64 column_int64(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: int64
- **Description**: Retrieves a 64-bit integer value from the current row of the result set and returns it.

### `string column_name(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: string
- **Description**: Retrieves the name of the specified column as a string.

### `int column_type(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: int
- **Description**: Retrieves the data type of the specified column as an integer.

### `string column_text(int index)`
- **Parameters**:
  - `index` (int): The column index.
- **Return Type**: string
- **Description**: Retrieves a text value from the current row of the result set and returns it.
