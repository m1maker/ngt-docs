# Class: vector

The `vector` class provides a data structure for representing and manipulating 3D vectors in NGT. It supports basic operations such as assigning values, resetting the vector, and accessing its components.

## Constructors

### `vector()`
- **Description**: Constructs an empty 3D vector with all components set to zero.

## Methods

### `float get_length() const property`
- **Return Type**: float
- **Description**: Returns the length (magnitude) of the 3D vector as a property.

### `vector& opAssign(const vector&in other)`
- **Parameters**:
  - `other` (const vector&): The other vector to assign.
- **Return Type**: vector&
- **Description**: Assigns the contents of another vector to this one and returns a reference to this object.

### `void reset() const`
- **Description**: Resets all components of the vector to zero.

## Properties

### `x`
- **Type**: float
- **Description**: A property representing the x-component of the 3D vector.

### `y`
- **Type**: float
- **Description**: A property representing the y-component of the 3D vector.

### `z`
- **Type**: float
- **Description**: A property representing the z-component of the 3D vector.
