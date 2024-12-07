# Class: vector

The `vector` class provides a data structure for representing and manipulating 3D vectors in NGT. It supports basic operations such as assigning values, resetting the vector, and accessing its components.

### `vector()`
- **Return Type**: void
- **Description**: Constructs a new vector object. The default constructor initializes the vector to zero.

### `vector(const vector&in)`
- **Return Type**: void
- **Description**: Constructs a new vector as a copy of another vector.

### `vector(float, float = 0, float = 0)`
- **Return Type**: void
- **Description**: Constructs a new vector with the specified x, y, and z components. If y and z are not provided, they default to zero.

### `vector& opAddAssign(const vector&in)`
- **Return Type**: vector&
- **Description**: Adds another vector to this vector in-place and returns a reference to this vector.

### `vector& opSubAssign(const vector&in)`
- **Return Type**: vector&
- **Description**: Subtracts another vector from this vector in-place and returns a reference to this vector.

### `vector& opMulAssign(float)`
- **Return Type**: vector&
- **Description**: Multiplies each component of this vector by the specified scalar value in-place and returns a reference to this vector.

### `vector& opDivAssign(float)`
- **Return Type**: vector&
- **Description**: Divides each component of this vector by the specified scalar value in-place and returns a reference to this vector.

### `bool opEquals(const vector&in) const`
- **Return Type**: bool
- **Description**: Compares two vectors for equality. Returns true if all corresponding components are equal; otherwise, returns false.

### `vector opAdd(const vector&in) const`
- **Return Type**: vector
- **Description**: Adds another vector to this vector and returns a new vector containing the result.

### `vector opSub(const vector&in) const`
- **Return Type**: vector
- **Description**: Subtracts another vector from this vector and returns a new vector containing the result.

### `vector opMul(float) const`
- **Return Type**: vector
- **Description**: Multiplies each component of this vector by the specified scalar value and returns a new vector containing the result.

### `vector opMul_r(float) const`
- **Return Type**: vector
- **Description**: Multiplies each component of the specified vector by the scalar value and returns a new vector containing the result (right-hand side multiplication).

### `vector opDiv(float) const`
- **Return Type**: vector
- **Description**: Divides each component of this vector by the specified scalar value and returns a new vector containing the result.

### `float length() const`
- **Return Type**: float
- **Description**: Calculates and returns the length (magnitude) of the vector.

### `vector get_xyz() const`
- **Return Type**: vector
- **Description**: Returns a new vector with components rearranged to x, y, z order.

### `vector get_yzx() const`
- **Return Type**: vector
- **Description**: Returns a new vector with components rearranged to y, z, x order.

### `vector get_zxy() const`
- **Return Type**: vector
- **Description**: Returns a new vector with components rearranged to z, x, y order.

### `vector get_zyx() const`
- **Return Type**: vector
- **Description**: Returns a new vector with components rearranged to z, y, x order.

### `vector get_yxz() const`
- **Return Type**: vector
- **Description**: Returns a new vector with components rearranged to y, x, z order.

### `vector get_xzy() const`
- **Return Type**: vector
- **Description**: Returns a new vector with components rearranged to x, z, y order.

### `void set_xyz(const vector&in)`
- **Return Type**: void
- **Description**: Sets the components of this vector to those of another vector in the x, y, z order.

### `void set_yzx(const vector&in)`
- **Return Type**: void
- **Description**: Sets the components of this vector to those of another vector in the y, z, x order.

### `void set_zxy(const vector&in)`
- **Return Type**: void
- **Description**: Sets the components of this vector to those of another vector in the z, x, y order.

### `void set_zyx(const vector&in)`
- **Return Type**: void
- **Description**: Sets the components of this vector to those of another vector in the z, y, x order.

### `void set_yxz(const vector&in)`
- **Return Type**: void
- **Description**: Sets the components of this vector to those of another vector in the y, x, z order.

### `void set_xzy(const vector&in)`
- **Return Type**: void
- **Description**: Sets the components of this vector to those of another vector in the x, z, y order.

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
