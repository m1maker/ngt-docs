# Class: complex

The `complex` class provides a data structure for representing complex numbers in NGT. It supports operations for basic arithmetic and accessing the real and imaginary parts of complex numbers.

## Constructors

### `void $list(const int&in count) { float, float }`
- **Parameters**:
  - `count` (int): The number of complex numbers to initialize.
- **Description**: Initializes an array of complex numbers with the specified count.

### `complex()`
- **Description**: Constructs a default complex number with zero real and imaginary parts.

### `complex(const complex&in other)`
- **Parameters**:
  - `other` (const complex&): The other complex number to copy.
- **Description**: Constructs a new complex number by copying another one.

### `complex(float value)`
- **Parameters**:
  - `value` (float): The real part of the complex number.
- **Description**: Constructs a complex number with the specified real part and zero imaginary part.

### `complex(float real, float imag)`
- **Parameters**:
  - `real` (float): The real part of the complex number.
  - `imag` (float): The imaginary part of the complex number.
- **Description**: Constructs a complex number with the specified real and imaginary parts.

## Methods

### `complex& opAddAssign(const complex&in other)`
- **Parameters**:
  - `other` (const complex&): The other complex number to add.
- **Return Type**: complex&
- **Description**: Adds another complex number to this one and returns a reference to this object.

### `complex& opSubAssign(const complex&in other)`
- **Parameters**:
  - `other` (const complex&): The other complex number to subtract.
- **Return Type**: complex&
- **Description**: Subtracts another complex number from this one and returns a reference to this object.

### `complex& opMulAssign(const complex&in other)`
- **Parameters**:
  - `other` (const complex&): The other complex number to multiply by.
- **Return Type**: complex&
- **Description**: Multiplies this complex number by another and returns a reference to this object.

### `complex& opDivAssign(const complex&in other)`
- **Parameters**:
  - `other` (const complex&): The other complex number to divide by.
- **Return Type**: complex&
- **Description**: Divides this complex number by another and returns a reference to this object.

### `bool opEquals(const complex&in other) const`
- **Parameters**:
  - `other` (const complex&): The other complex number to compare with.
- **Return Type**: bool
- **Description**: Compares this complex number with another for equality and returns `true` if they are equal; otherwise, returns `false`.

### `complex opAdd(const complex&in other) const`
- **Parameters**:
  - `other` (const complex&): The other complex number to add.
- **Return Type**: complex
- **Description**: Creates a new complex number by adding this one and another.

### `complex opSub(const complex&in other) const`
- **Parameters**:
  - `other` (const complex&): The other complex number to subtract.
- **Return Type**: complex
- **Description**: Creates a new complex number by subtracting another from this one.

### `complex opMul(const complex&in other) const`
- **Parameters**:
  - `other` (const complex&): The other complex number to multiply by.
- **Return Type**: complex
- **Description**: Creates a new complex number by multiplying this one by another.

### `complex opDiv(const complex&in other) const`
- **Parameters**:
  - `other` (const complex&): The other complex number to divide by.
- **Return Type**: complex
- **Description**: Creates a new complex number by dividing this one by another.

### `float abs() const`
- **Return Type**: float
- **Description**: Returns the absolute value of the complex number.

### `complex get_ri() const property`
- **Return Type**: complex
- **Description**: Returns the real part of the complex number as a property.

### `complex get_ir() const property`
- **Return Type**: complex
- **Description**: Returns the imaginary part of the complex number as a property.

### `void set_ri(const complex&in value) property`
- **Parameters**:
  - `value` (const complex&): The new real part to set.
- **Description**: Sets the real part of the complex number using a property.

### `void set_ir(const complex&in value) property`
- **Parameters**:
  - `value` (const complex&): The new imaginary part to set.
- **Description**: Sets the imaginary part of the complex number using a property.

## Properties

### `r`
- **Type**: float
- **Description**: A property representing the real part of the complex number.

### `i`
- **Type**: float
- **Description**: A property representing the imaginary part of the complex number.
