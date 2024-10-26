# Class: ref

The `ref` class provides a reference wrapper for managing and manipulating references in NGT. It allows you to create and assign references, check equality, and cast the reference to other types.

## Constructors

### `ref()`
- **Description**: Constructs an empty reference object.

### `ref(const ref&in other)`
- **Parameters**:
  - `other` (const ref&): The other reference object to copy.
- **Description**: Constructs a new reference by copying another one.

### `ref(const ?&in value)`
- **Parameters**:
  - `value` (const ?&): A value to reference.
- **Description**: Constructs a new reference that references the specified value.

## Methods

### `void opCast(?&out result)`
- **Parameters**:
  - `result` (?&out): Output parameter for the casted value.
- **Description**: Casts the reference to another type and assigns the result to the output parameter.

### `ref& opHndlAssign(const ref&in other)`
- **Parameters**:
  - `other` (const ref&): The other reference object to assign.
- **Return Type**: ref&
- **Description**: Assigns the contents of another reference to this one and returns a reference to this object.

### `ref& opHndlAssign(const ?&in value)`
- **Parameters**:
  - `value` (const ?&): A value to reference.
- **Return Type**: ref&
- **Description**: Assigns a new reference that references the specified value and returns a reference to this object.

### `bool opEquals(const ref&in other) const`
- **Parameters**:
  - `other` (const ref&): The other reference object to compare with.
- **Return Type**: bool
- **Description**: Compares this reference with another for equality and returns `true` if they are equal; otherwise, returns `false`.

### `bool opEquals(const ?&in value) const`
- **Parameters**:
  - `value` (const ?&): The value to compare with.
- **Return Type**: bool
- **Description**: Compares this reference with another value for equality and returns `true` if they are equal; otherwise, returns `false`.
