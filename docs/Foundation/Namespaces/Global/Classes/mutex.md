## Mutex Operations

### `mutex()`
- **Return Type**: mutex@
- **Description**: Constructs a new mutex object.

### `void lock(int milliseconds)`
- **Return Type**: void
- **Description**: Acquires the mutex. If the mutex is already locked by another thread, this will block for up to `milliseconds` before timing out and returning.

### `bool try_lock(int milliseconds)`
- **Return Type**: bool
- **Description**: Attempts to acquire the mutex without blocking. Returns true if the mutex was successfully acquired within `milliseconds`; otherwise, returns false immediately.

### `void lock()`
- **Return Type**: void
- **Description**: Acquires the mutex, similar to the overload with an integer parameter. If the mutex is already locked by another thread, this will block indefinitely until the lock becomes available.

### `bool try_lock()`
- **Return Type**: bool
- **Description**: Attempts to acquire the mutex without blocking, as per the integer-parameter version. Returns true if the mutex was successfully acquired within an unspecified amount of time; otherwise, returns false immediately.

### `void unlock()`
- **Return Type**: void
- **Description**: Releases the lock on the mutex that is currently held by the calling thread, allowing other threads waiting to acquire it to proceed.
