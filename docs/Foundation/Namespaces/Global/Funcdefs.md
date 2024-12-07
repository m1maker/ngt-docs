### array<T>::less
- **Return Type**: `bool`
- **Parameters**:
  - `a`: A constant reference to the first element of type T.
  - `b`: A constant reference to the second element of type T.
- **Description**: This function is used as a comparator for arrays. It returns true if `a` should come before `b` in the sorted order, and false otherwise.

### exit_callback
- **Return Type**: `int`
- **Parameters**: None
- **Description**: This function is called when the application is exiting. If function returns 0, application can free the memory and exit. If function returns 1, exit function can not be called and application will continue work.

### thread_func
- **Return Type**: `void`
- **Parameters**: dictionary@ args
- **Description**: This function defines the entry point for a new thread. It is responsible for the execution of tasks within that thread.
