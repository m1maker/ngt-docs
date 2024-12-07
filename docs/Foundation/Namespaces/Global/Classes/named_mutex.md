## Named Mutex Operations

### `named_mutex(const string&in name)`
- **Return Type**: named_mutex@
- **Description**: Constructs a new named mutex object with the specified name. Named mutexes allow multiple threads or processes to synchronize access by referring to the same unique name.

### `void lock()`
- **Return Type**: void
- **Description**: Acquires the named mutex. If the mutex is already locked by another thread or process, this will block until the lock becomes available.

### `bool try_lock()`
- **Return Type**: bool
- **Description**: Attempts to acquire the named mutex without blocking. Returns true if the mutex was successfully acquired; otherwise, returns false immediately.

### `void unlock()`
- **Return Type**: void
- **Description**: Releases the lock on the named mutex that is currently held by the calling thread or process, allowing other threads or processes waiting to acquire it to proceed.
