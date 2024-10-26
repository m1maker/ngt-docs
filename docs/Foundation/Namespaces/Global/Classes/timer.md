# Class: timer

The `timer` class provides a data structure for managing and controlling timers. It allows you to track elapsed time, force specific times, restart the timer, pause and resume it, and check if it is currently running.

## Constructors

### `timer()`
- **Description**: Constructs an empty `timer` object and initializes it to start counting from when it was created.

## Methods

### `uint64 get_elapsed_seconds() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in seconds since the timer was started or last reset as a property.

### `uint64 get_elapsed_minutes() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in minutes since the timer was started or last reset as a property.

### `uint64 get_elapsed_hours() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in hours since the timer was started or last reset as a property.

### `uint64 get_elapsed_millis() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in milliseconds since the timer was started or last reset as a property.

### `uint64 get_elapsed_micros() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in microseconds since the timer was started or last reset as a property.

### `uint64 get_elapsed_nanos() const property`
- **Return Type**: uint64
- **Description**: Returns the elapsed time in nanoseconds since the timer was started or last reset as a property.

### `void force_seconds(uint64 seconds) const`
- **Parameters**:
  - `seconds` (uint64): The new elapsed time in seconds.
- **Description**: Forces the timer to show a specific elapsed time in seconds.

### `void force_minutes(uint64 minutes) const`
- **Parameters**:
  - `minutes` (uint64): The new elapsed time in minutes.
- **Description**: Forces the timer to show a specific elapsed time in minutes.

### `void force_hours(uint64 hours) const`
- **Parameters**:
  - `hours` (uint64): The new elapsed time in hours.
- **Description**: Forces the timer to show a specific elapsed time in hours.

### `void force_millis(uint64 millis) const`
- **Parameters**:
  - `millis` (uint64): The new elapsed time in milliseconds.
- **Description**: Forces the timer to show a specific elapsed time in milliseconds.

### `void force_micros(uint64 micros) const`
- **Parameters**:
  - `micros` (uint64): The new elapsed time in microseconds.
- **Description**: Forces the timer to show a specific elapsed time in microseconds.

### `void force_nanos(uint64 nanos) const`
- **Parameters**:
  - `nanos` (uint64): The new elapsed time in nanoseconds.
- **Description**: Forces the timer to show a specific elapsed time in nanoseconds.

### `void restart() const`
- **Description**: Restarts the timer, resetting the elapsed time to zero.

### `void pause() const`
- **Description**: Pauses the timer.

### `void resume() const`
- **Description**: Resumes the paused timer.

### `bool get_running() const property`
- **Return Type**: bool
- **Description**: Returns whether the timer is currently running as a property.
