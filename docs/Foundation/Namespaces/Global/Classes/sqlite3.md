# Class: sqlite3

The `sqlite3` class provides a data structure for interacting with SQLite databases in NGT. It allows you to open and close connections, prepare and execute SQL statements, manage transactions, retrieve metadata, and handle errors.

## Constructors

### `sqlite3()`
- **Description**: Constructs an empty `sqlite3` object ready to interact with an SQLite database.

## Methods

### `int close()`
- **Return Type**: int
- **Description**: Closes the connection to the SQLite database and returns an error code if any issues occur.

### `int open(const string&in filename, int flags = 6)`
- **Parameters**:
  - `filename` (const string&): The path to the SQLite database file.
  - `flags` (int): Optional flags for opening the database (e.g., read-only, writable).
- **Return Type**: int
- **Description**: Opens a connection to the specified SQLite database and returns an error code if any issues occur.

### `sqlite3statement@ prepare(const string&in sql, int&out out = void)`
- **Parameters**:
  - `sql` (const string&): The SQL statement to prepare.
  - `out` (int&out): Optional output parameter for additional information or error codes.
- **Return Type**: sqlite3statement@
- **Description**: Prepares an SQL statement for execution and returns a new `sqlite3statement` object.

### `int execute(const string&in sql)`
- **Parameters**:
  - `sql` (const string&): The SQL statement to execute.
- **Return Type**: int
- **Description**: Executes the specified SQL statement and returns an error code if any issues occur.

### `int64 get_rows_changed() property`
- **Return Type**: int64
- **Description**: Returns the number of rows modified (INSERT, UPDATE, DELETE) since the last operation as a property.

### `int64 get_total_rows_changed() property`
- **Return Type**: int64
- **Description**: Returns the total number of rows modified across all operations performed by this connection as a property.

### `int limit(int id, int val)`
- **Parameters**:
  - `id` (int): The identifier for the specific limit to set.
  - `val` (int): The new value for the specified limit.
- **Return Type**: int
- **Description**: Sets a specific SQLite limit and returns an error code if any issues occur.

### `int set_authorizer(sqlite3authorizer@ authorizer, const string&in arg = "")`
- **Parameters**:
  - `authorizer` (sqlite3authorizer@): The authorizer object to use for authorization callbacks.
  - `arg` (const string&): Optional argument for the authorizer callback.
- **Return Type**: int
- **Description**: Sets an authorizer for SQL operations and returns an error code if any issues occur.

### `int64 get_last_insert_rowid() property`
- **Return Type**: int64
- **Description**: Returns the row ID of the last inserted row as a property.

### `void set_last_insert_rowid(int64 id) property`
- **Parameters**:
  - `id` (int64): The new row ID to set as the last insert row.
- **Description**: Sets the row ID to use as the last insert row using a property.

### `int get_last_error()`
- **Return Type**: int
- **Description**: Returns the error code of the last operation that failed.

### `string get_last_error_text()`
- **Return Type**: string
- **Description**: Retrieves a human-readable error message for the last operation that failed.

### `bool get_active() property`
- **Return Type**: bool
- **Description**: Returns whether the connection to the SQLite database is currently active as a property.
