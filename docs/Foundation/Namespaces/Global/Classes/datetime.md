# Class: datetime

The `datetime` class provides a data structure for representing and manipulating date and time values.

## Constructors

### `datetime()`
- **Description**: Constructs the current date and time when no parameters are provided.
  
### `datetime(const datetime&in other)`
- **Parameters**:
  - `other` (const datetime&): The other datetime object to copy.
- **Description**: Constructs a new datetime object by copying another one.

### `datetime(uint year, uint month, uint day, uint hour = 0, uint minute = 0, uint second = 0)`
- **Parameters**:
  - `year` (uint): The year part of the date.
  - `month` (uint): The month part of the date.
  - `day` (uint): The day part of the date.
  - `hour` (uint): The hour part of the time (default is 0).
  - `minute` (uint): The minute part of the time (default is 0).
  - `second` (uint): The second part of the time (default is 0).
- **Description**: Constructs a datetime object with specific year, month, day, hour, minute, and second values.

## Methods

### `datetime& opAssign(const datetime&in other)`
- **Parameters**:
  - `other` (const datetime&): The other datetime object to assign.
- **Return Type**: datetime&
- **Description**: Assigns the contents of another datetime object to this one and returns a reference to this object.

### `uint get_year() const property`
- **Return Type**: uint
- **Description**: Returns the year part of the datetime as a property.

### `uint get_month() const property`
- **Return Type**: uint
- **Description**: Returns the month part of the datetime as a property.

### `uint get_day() const property`
- **Return Type**: uint
- **Description**: Returns the day part of the datetime as a property.

### `uint get_hour() const property`
- **Return Type**: uint
- **Description**: Returns the hour part of the datetime as a property.

### `uint get_minute() const property`
- **Return Type**: uint
- **Description**: Returns the minute part of the datetime as a property.

### `uint get_second() const property`
- **Return Type**: uint
- **Description**: Returns the second part of the datetime as a property.

### `bool setDate(uint year, uint month, uint day)`
- **Parameters**:
  - `year` (uint): The new year to set.
  - `month` (uint): The new month to set.
  - `day` (uint): The new day to set.
- **Return Type**: bool
- **Description**: Sets the date part of the datetime and returns `true` if successful; otherwise, returns `false`.

### `bool setTime(uint hour, uint minute, uint second)`
- **Parameters**:
  - `hour` (uint): The new hour to set.
  - `minute` (uint): The new minute to set.
  - `second` (uint): The new second to set.
- **Return Type**: bool
- **Description**: Sets the time part of the datetime and returns `true` if successful; otherwise, returns `false`.

### `int64 opSub(const datetime&in other) const`
- **Parameters**:
  - `other` (const datetime&): The datetime to subtract from this one.
- **Return Type**: int64
- **Description**: Returns the difference in seconds between this datetime and another.

### `datetime opAdd(int64 seconds) const`
- **Parameters**:
  - `seconds` (int64): The number of seconds to add to this datetime.
- **Return Type**: datetime
- **Description**: Creates a new datetime by adding the specified number of seconds to this one and returns it.

### `datetime opAdd_r(int64 seconds) const`
- **Parameters**:
  - `seconds` (int64): The number of seconds to add to this datetime.
- **Return Type**: datetime
- **Description**: Creates a new datetime by adding the specified number of seconds to this one and returns it.

### `datetime& opAddAssign(int64 seconds)`
- **Parameters**:
  - `seconds` (int64): The number of seconds to add to this datetime.
- **Return Type**: datetime&
- **Description**: Adds the specified number of seconds to this datetime and returns a reference to this object.

### `datetime opSub(int64 seconds) const`
- **Parameters**:
  - `seconds` (int64): The number of seconds to subtract from this datetime.
- **Return Type**: datetime
- **Description**: Creates a new datetime by subtracting the specified number of seconds from this one and returns it.

### `datetime opSub_r(int64 seconds) const`
- **Parameters**:
  - `seconds` (int64): The number of seconds to subtract from this datetime.
- **Return Type**: datetime
- **Description**: Creates a new datetime by subtracting the specified number of seconds from this one and returns it.

### `datetime& opSubAssign(int64 seconds)`
- **Parameters**:
  - `seconds` (int64): The number of seconds to subtract from this datetime.
- **Return Type**: datetime&
- **Description**: Subtracts the specified number of seconds from this datetime and returns a reference to this object.

### `bool opEquals(const datetime&in other) const`
- **Parameters**:
  - `other` (const datetime&): The other datetime to compare with this one.
- **Return Type**: bool
- **Description**: Compares this datetime with another for equality and returns `true` if they are equal; otherwise, returns `false`.

### `int opCmp(const datetime&in other) const`
- **Parameters**:
  - `other` (const datetime&): The other datetime to compare with this one.
- **Return Type**: int
- **Description**: Compares this datetime with another and returns an integer value indicating the order of the two datetimes.
