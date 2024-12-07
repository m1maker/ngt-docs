# Class: instance

The `instance` class provides a data structure for managing an application instance. It allows you to check if the instance is currently running.

## Constructors

### `instance(const string&in application_name)`
- **Parameters**:
  - `application_name` (const string&): The name of the application.
- **Description**: Constructs a new `instance` object and attempts to manage the specified application instance.

## Methods

### `bool is_running()`
- **Return Type**: bool
- **Description**: Returns whether the managed application instance is currently running.
