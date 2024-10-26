# Class: user_idle

The `user_idle` class provides a data structure for tracking the duration of time that a user has been idle. It allows you to retrieve various units of elapsed time since the last activity.

## Constructors

### `user_idle()`
- **Description**: Constructs an empty `user_idle` object and starts counting the time from when the object was created.

## Methods

### `uint64 get_elapsed_millis() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in milliseconds since the last activity as a property.

### `uint64 get_elapsed_seconds() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in seconds since the last activity as a property.

### `uint64 get_elapsed_minutes() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in minutes since the last activity as a property.

### `uint64 get_elapsed_hours() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in hours since the last activity as a property.

### `uint64 get_elapsed_days() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in days since the last activity as a property.

### `uint64 get_elapsed_weeks() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in weeks since the last activity as a property.
