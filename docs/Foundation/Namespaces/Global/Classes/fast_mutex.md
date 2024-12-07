## Fast Mutex Operations

### `fast_mutex()`
- **Return Type**: fast_mutex@
- **Description**: Constructs a new fast mutex object. This type of mutex is designed for higher performance than regular mutexes, particularly in scenarios with frequent lock contention.

### `void lock(int milliseconds)`
- **Return Type**: void
- **Description**: Acquires the fast mutex. If the mutex is already locked by another thread, this will block for up to `milliseconds` before timing out and returning.

### `bool try_lock(int milliseconds)`
- **Return Type**: bool
- **Description**: Attempts to acquire the fast mutex without blocking. Returns true if the mutex was successfully acquired within `milliseconds`; otherwise, returns false immediately.

### `void lock()`
- **Return Type**: void
- **Description**: Acquires the fast mutex, similar to the overload with an integer parameter. If the mutex is already locked by another thread, this will block indefinitely until the lock becomes available.

### `bool try_lock()`
- **Return Type**: bool
- **Description**: Attempts to acquire the fast mutex without blocking, as per the integer-parameter version. Returns true if the mutex was successfully acquired within an unspecified amount of time; otherwise, returns false immediately.

### `void unlock()`
- **Return Type**: void
- **Description**: Releases the lock on the fast mutex that is currently held by the calling thread, allowing other threads waiting to acquire it to proceed.
