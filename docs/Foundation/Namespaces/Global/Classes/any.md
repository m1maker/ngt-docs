# Class: any

The `any` class provides a data structure that can hold and manage values of different types in NGT. It allows for flexible storage and retrieval of various data types.

## Constructors

### `any()`
- **Description**: Constructs an empty `any` object.

### `any(?&in value)`
- **Parameters**:
  - `value` (?&): A value to store.
- **Description**: Constructs a new `any` object and stores the specified value.

### `any(const int64&in value)`
- **Parameters**:
  - `value` (const int64&): An integer value to store.
- **Description**: Constructs a new `any` object and stores the specified integer value.

### `any(const double&in value)`
- **Parameters**:
  - `value` (const double&): A floating-point value to store.
- **Description**: Constructs a new `any` object and stores the specified floating-point value.


## Methods

### `any& opAssign(any&in other)`
- **Parameters**:
  - `other` (any&): The other `any` object to assign.
- **Return Type**: any&
- **Description**: Assigns the contents of another `any` object to this one and returns a reference to this object.

### `void store(?&in value)`
- **Parameters**:
  - `value` (?&): A value to store.
- **Description**: Stores the specified value in the `any` object.

### `void store(const int64&in value)`
- **Parameters**:
  - `value` (const int64&): An integer value to store.
- **Description**: Stores the specified integer value in the `any` object.

### `void store(const double&in value)`
- **Parameters**:
  - `value` (const double&): A floating-point value to store.
- **Description**: Stores the specified floating-point value in the `any` object.

### `bool retrieve(?&out result)`
- **Parameters**:
  - `result` (?&out): Output parameter for the retrieved value.
- **Return Type**: bool
- **Description**: Retrieves the stored value and assigns it to the output parameter. Returns `true` if successful; otherwise, returns `false`.

### `bool retrieve(int64&out result)`
- **Parameters**:
  - `result` (int64&out): Output parameter for the retrieved integer value.
- **Return Type**: bool
- **Description**: Retrieves the stored integer value and assigns it to the output parameter. Returns `true` if successful; otherwise, returns `false`.

### `bool retrieve(double&out result)`
- **Parameters**:
  - `result` (double&out): Output parameter for the retrieved floating-point value.
- **Return Type**: bool
- **Description**: Retrieves the stored floating-point value and assigns it to the output parameter. Returns `true` if successful; otherwise, returns `false`.
