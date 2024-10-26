# Class: array<T>

The `array<T>` class provides a dynamic array data structure in NGT. It supports various operations for managing and manipulating arrays of any type `T`.

## Constructors

### `array<T>()`
- **Description**: Constructs an empty array.

### `array<T>(int&in length)`
- **Parameters**:
  - `length` (int): The initial length of the array.
- **Description**: Constructs an array with the specified initial length, filled with default values.

### `array<T>(int&in length, const T&in value)`
- **Parameters**:
  - `length` (int): The initial length of the array.
  - `value` (const T&): The value to fill the array with.
- **Description**: Constructs an array with the specified initial length, filled with the given value.

### `$list(int&in start, int&in count) { repeat T }`
- **Parameters**:
  - `start` (int): The starting index.
  - `count` (int): The number of elements to create.
- **Return Type**: array<T>
- **Description**: Creates and returns a new array with the specified range.

## Methods

### `T& opIndex(uint index)`
- **Parameters**:
  - `index` (uint): The index to access.
- **Return Type**: T&
- **Description**: Provides indexed access to the array. Returns a reference to the element at the specified index.

### `const T& opIndex(uint index) const`
- **Parameters**:
  - `index` (uint): The index to access.
- **Return Type**: const T&
- **Description**: Provides indexed access to the array in a read-only manner. Returns a reference to the element at the specified index.

### `array<T>& opAssign(const array<T>&in other)`
- **Parameters**:
  - `other` (const array<T>&): The other array to assign.
- **Return Type**: array<T>&
- **Description**: Assigns the contents of another array to this array and returns a reference to this array.

### `void insert_at(uint index, const T&in value)`
- **Parameters**:
  - `index` (uint): The index at which to insert.
  - `value` (const T&): The value to insert.
- **Description**: Inserts a new element into the array at the specified index.

### `void insert_at(uint index, const array<T>&inout arr)`
- **Parameters**:
  - `index` (uint): The index at which to insert.
  - `arr` (const array<T>&inout): The array to insert.
- **Description**: Inserts another array into this array at the specified index.

### `void insert_last(const T&in value)`
- **Parameters**:
  - `value` (const T&): The value to insert at the end of the array.
- **Description**: Appends a new element to the end of the array.

### `void remove_at(uint index)`
- **Parameters**:
  - `index` (uint): The index of the element to remove.
- **Description**: Removes the element at the specified index from the array.

### `void remove_last()`
- **Description**: Removes the last element from the array.

### `void remove_range(uint start, uint count)`
- **Parameters**:
  - `start` (uint): The starting index of the range to remove.
  - `count` (uint): The number of elements to remove.
- **Description**: Removes a specified range of elements from the array.

### `uint length() const`
- **Return Type**: uint
- **Description**: Returns the current length of the array.

### `void reserve(uint length)`
- **Parameters**:
  - `length` (uint): The new minimum capacity to reserve for the array.
- **Description**: Reserves enough space in the array to hold at least the specified number of elements without reallocation.

### `void resize(uint length)`
- **Parameters**:
  - `length` (uint): The new size for the array.
- **Description**: Changes the size of the array. If the new size is larger than the current capacity, the array will be resized to accommodate it.

### `void sort_asc()`
- **Description**: Sorts the elements in ascending order.

### `void sort_asc(uint startAt, uint count)`
- **Parameters**:
  - `startAt` (uint): The starting index for sorting.
  - `count` (uint): The number of elements to sort.
- **Description**: Sorts a specified range of elements in the array in ascending order.

### `void sort_desc()`
- **Description**: Sorts the elements in descending order.

### `void sort_desc(uint startAt, uint count)`
- **Parameters**:
  - `startAt` (uint): The starting index for sorting.
  - `count` (uint): The number of elements to sort.
- **Description**: Sorts a specified range of elements in the array in descending order.

### `void reverse()`
- **Description**: Reverses the order of the elements in the array.

### `int find(const T&in value) const`
- **Parameters**:
  - `value` (const T&): The value to search for.
- **Return Type**: int
- **Description**: Searches for the specified value in the array and returns its index if found; otherwise, returns `-1`.

### `int find(uint startAt, const T&in value) const`
- **Parameters**:
  - `startAt` (uint): The starting index for search.
  - `value` (const T&): The value to search for.
- **Return Type**: int
- **Description**: Searches for the specified value in a specified range of the array and returns its index if found; otherwise, returns `-1`.

### `int find_by_ref(const T&in value) const`
- **Parameters**:
  - `value` (const T&): The value to search for.
- **Return Type**: int
- **Description**: Searches for the specified value in the array using reference equality and returns its index if found; otherwise, returns `-1`.

### `int find_by_ref(uint startAt, const T&in value) const`
- **Parameters**:
  - `startAt` (uint): The starting index for search.
  - `value` (const T&): The value to search for.
- **Return Type**: int
- **Description**: Searches for the specified value in a specified range of the array using reference equality and returns its index if found; otherwise, returns `-1`.

### `bool op_equals(const array<T>&in other) const`
- **Parameters**:
  - `other` (const array<T>&): The other array to compare.
- **Return Type**: bool
- **Description**: Compares this array with another array for equality and returns `true` if they are equal; otherwise, returns `false`.

### `bool is_empty() const`
- **Return Type**: bool
- **Description**: Checks if the array is empty and returns `true` if it is; otherwise, returns `false`.

### `void sort(array<T>::less&in comparer, uint startAt = 0, uint count = uint (-1))`
- **Parameters**:
  - `comparer` (array<T>::less&): The comparison function object.
  - `startAt` (uint): The starting index for sorting (default is `0`).
  - `count` (uint): The number of elements to sort (default is the entire array).
- **Description**: Sorts the array using a custom comparison function.
