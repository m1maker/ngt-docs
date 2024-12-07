# Class: thread

The `thread` class provides a data structure for managing and controlling threads in NGT. It allows you to create, manage, and terminate threads, as well as wait for them to complete their execution.

## Constructors

### `thread(thread_func@ func, dictionary@ args = null)`
- **Parameters**:
  - `func` (thread_func@): A function to be executed by the new thread.
  - `args` (dictionary@): A dictionary with arguments handled by thread_func.
- **Description**: Constructs a new `thread` object and starts executing the specified function in a separate thread.

## Methods

### `void detach() const`
- **Description**: Detaches the thread, allowing it to run independently and freeing up resources once it completes execution.

### `void join() const`
- **Description**: Waits for the thread to complete its execution before continuing. This blocks the calling thread until the target thread finishes.

### `void destroy() const`
- **Description**: Terminates the thread forcefully. Note that this should be used with caution as it can lead to resource leaks and undefined behavior.
