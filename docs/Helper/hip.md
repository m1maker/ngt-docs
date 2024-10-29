# Helpful Includes pack (HIP)

The Helpful Includes pack, or HIP for short, is a collection of utility functions designed to simplify common tasks in game development using the NGT engine. This pack includes features such as keyboard input checks, random number generation, array and string manipulations, file operations, and more. The pack aims to make code more readable, concise, and maintainable.

## Usage

To use this pack in your project, include it at the beginning of your script:

```angelscript
#include "hip"
```

### Namespace

If `HIP_NAMESPACE` is defined, all functions are encapsulated within a namespace `hip`.

## Table of Contents

1. **Keyboard Input Checks**
2. **Random Number Generation**
3. **Lister Class**
4. **String Size Conversion**
5. **Month and Weekday Conversions**
6. **Rating Calculation**
7. **Text Parsing**
8. **Percentage Calculation**
9. **File Operations**
10. **Range Checking**
11. **Toggle and Boolean Functions**
12. **Miscellaneous Utility Functions**

## 1. Keyboard Input Checks

### `control_is_down()`
- **Description**: Checks if the left or right control key is down.
- **Returns**: `true` if either control key is pressed, otherwise `false`.

```angelscript
bool ctrlDown = control_is_down();
```

### `alt_is_down()`
- **Description**: Checks if the left or right alt key is down.
- **Returns**: `true` if either alt key is pressed, otherwise `false`.

```angelscript
bool altDown = alt_is_down();
```

### `shift_is_down()`
- **Description**: Checks if the left or right shift key is down.
- **Returns**: `true` if either shift key is pressed, otherwise `false`.

```angelscript
bool shiftDown = shift_is_down();
```

### Properties

- **get_control_down()**
- **get_shift_down()**
- **get_alt_down()**

These properties provide a more convenient way to access the keyboard input checks.

## 2. Random Number Generation

### `rdm(double minimum, double maximum, bool rounded = false, double number_of_rounding = 0)`
- **Description**: Generates a random number within the specified range.
- **Parameters**:
  - `minimum`: The lower bound of the range.
  - `maximum`: The upper bound of the range.
  - `rounded`: If `true`, rounds the result to a specified number of decimal places.
  - `number_of_rounding`: The number of decimal places for rounding.
- **Returns**: A random number within the specified range.

```angelscript
double randomNumber = rdm(0, 100);
```

## 3. Lister Class

### `lister` Class Methods

#### `string convert(string[] arr, const string&in each = ", ")`
- **Description**: Converts an array of strings to a single string with items separated by a specified delimiter.
- **Parameters**:
  - `arr`: The array of strings to convert.
  - `each`: The delimiter to use between items (default is a comma and space).
- **Returns**: A single string containing the array elements joined by the specified delimiter.

```angelscript
string[] fruits = {"apple", "banana", "cherry"};
string fruitList = lister.convert(fruits); // "apple, banana, cherry"
```

#### `string convert(int[] arr, const string&in each = ", ")`
- **Description**: Converts an array of integers to a single string with items separated by a specified delimiter.
- **Parameters**:
  - `arr`: The array of integers to convert.
  - `each`: The delimiter to use between items (default is a comma and space).
- **Returns**: A single string containing the array elements joined by the specified delimiter.

```angelscript
int[] numbers = {1, 2, 3};
string numberList = lister.convert(numbers); // "1, 2, 3"
```

#### `string convert(double[] arr, const string&in each = ", ")`
- **Description**: Converts an array of doubles to a single string with items separated by a specified delimiter.
- **Parameters**:
  - `arr`: The array of doubles to convert.
  - `each`: The delimiter to use between items (default is a comma and space).
- **Returns**: A single string containing the array elements joined by the specified delimiter.

```angelscript
double[] values = {1.1, 2.2, 3.3};
string valueList = lister.convert(values); // "1.1, 2.2, 3.3"
```

#### `string convert(float[] arr, const string&in each = ", ")`
- **Description**: Converts an array of floats to a single string with items separated by a specified delimiter.
- **Parameters**:
  - `arr`: The array of floats to convert.
  - `each`: The delimiter to use between items (default is a comma and space).
- **Returns**: A single string containing the array elements joined by the specified delimiter.

```angelscript
float[] heights = {1.6, 1.75, 1.8};
string heightList = lister.convert(heights); // "1.6, 1.75, 1.8"
```

#### `string convert(uint[] arr, const string&in each = ", ")`
- **Description**: Converts an array of unsigned integers to a single string with items separated by a specified delimiter.
- **Parameters**:
  - `arr`: The array of unsigned integers to convert.
  - `each`: The delimiter to use between items (default is a comma and space).
- **Returns**: A single string containing the array elements joined by the specified delimiter.

```angelscript
uint[] ids = {10, 20, 30};
string idList = lister.convert(ids); // "10, 20, 30"
```

## 4. String Size Conversion

### `string convert_size(double size, int round_to = 2)`
- **Description**: Converts a size in bytes to the most appropriate unit (B, KB, MB, GB, TB).
- **Parameters**:
  - `size`: The size in bytes.
  - `round_to`: The number of decimal places to round the result.
- **Returns**: A string representing the converted size.

```angelscript
double fileSize = 1024 * 1024 * 5;
string formattedSize = convert_size(fileSize); // "5 MB"
```

## 5. Month and Weekday Conversions

### `string convert_month_name(double value)`
- **Description**: Converts a month number to its corresponding name.
- **Parameters**:
  - `value`: The month number (1-12).
- **Returns**: The name of the month.

```angelscript
double monthNumber = 4;
string monthName = convert_month_name(monthNumber); // "April"
```

### `double convert_month_number(const string&in monthname)`
- **Description**: Converts a month name to its corresponding number.
- **Parameters**:
  - `monthname`: The name of the month.
- **Returns**: The month number (1-12).

```angelscript
string monthName = "April";
double monthNumber = convert_month_number(monthName); // 4
```

### `string convert_weekday_name(double value)`
- **Description**: Converts a weekday number to its corresponding name.
- **Parameters**:
  - `value`: The weekday number (1-7).
- **Returns**: The name of the weekday.

```angelscript
double weekdayNumber = 2;
string weekdayName = convert_weekday_name(weekdayNumber); // "Monday"
```

### `double convert_weekday_number(const string&in weekdayname)`
- **Description**: Converts a weekday name to its corresponding number.
- **Parameters**:
  - `weekdayname`: The name of the weekday.
- **Returns**: The weekday number (1-7).

```angelscript
string weekdayName = "Monday";
double weekdayNumber = convert_weekday_number(weekdayName); // 2
```

## 6. Rating Calculation

### `double get5rating(double five, double four, double three, double two, double one, int round_to = 1)`
- **Description**: Calculates the average rating based on a 5-star scale.
- **Parameters**:
  - `five`: Number of 5-star ratings.
  - `four`: Number of 4-star ratings.
  - `three`: Number of 3-star ratings.
  - `two`: Number of 2-star ratings.
  - `one`: Number of 1-star ratings.
  - `round_to`: The number of decimal places to round the result.
- **Returns**: The average rating rounded to the specified number of decimal places.

```angelscript
double avgRating = get5rating(3, 2, 4, 1, 0); // 4.0
```

## 7. Text Parsing

### `string get_item_text(const string&in text, const string&in split_with = "[[]]")`
- **Description**: Extracts the item text from a given string based on a delimiter.
- **Parameters**:
  - `text`: The input string containing items.
  - `split_with`: The delimiter to use for splitting (default is "[[]]").
- **Returns**: The extracted item text.

```angelscript
string fullText = "item [[]] description";
string itemText = get_item_text(fullText); // "item"
```

### `string get_item_name(const string&in text, const string&in split_with = "[[]]")`
- **Description**: Extracts the item name from a given string based on a delimiter.
- **Parameters**:
  - `text`: The input string containing items.
  - `split_with`: The delimiter to use for splitting (default is "[[]]").
- **Returns**: The extracted item name.

```angelscript
string fullText = "item [[]] description";
string itemName = get_item_name(fullText); // "item"
```

## 8. Percentage Calculation

### `double percent(double n1, double n2)`
- **Description**: Calculates the percentage of one value relative to another.
- **Parameters**:
  - `n1`: The numerator.
  - `n2`: The denominator.
- **Returns**: The percentage as a decimal.

```angelscript
double result = percent(75, 100); // 0.75
```

## 9. File Operations

### `bool file_put_contents(const string&in filename, const string&in contents, uint8 filemode = FILE_WRITE)`
- **Description**: Writes content to a file.
- **Parameters**:
  - `filename`: The name of the file.
  - `contents`: The content to write.
  - `filemode`: The mode in which to open the file (default is `FILE_WRITE`).
- **Returns**: `true` if the file was successfully written, otherwise `false`.

```angelscript
bool success = file_put_contents("example.txt", "Hello, World!");
```

### `string file_get_contents(const string&in filename)`
- **Description**: Reads content from a file.
- **Parameters**:
  - `filename`: The name of the file.
- **Returns**: The content of the file.

```angelscript
string content = file_get_contents("example.txt");
```

## 10. Range Checking

### `bool in_range(float value, float min, float max)`
- **Description**: Checks if a value is within a specified range.
- **Parameters**:
  - `value`: The value to check.
  - `min`: The minimum value of the range.
  - `max`: The maximum value of the range.
- **Returns**: `true` if the value is within the range, otherwise `false`.

```angelscript
bool isInRange = in_range(5, 0, 10); // true
```

### `bool in_range(double x, double y, double z, double minx, double maxx, double miny, double maxy, double minz, double maxz)`
- **Description**: Checks if a 3D point is within a specified range.
- **Parameters**:
  - `x`, `y`, `z`: The coordinates of the point.
  - `minx`, `maxx`, `miny`, `maxy`, `minz`, `maxz`: The minimum and maximum coordinates of the range.
- **Returns**: `true` if the point is within the range, otherwise `false`.

```angelscript
bool isInRange = in_range(1, 2, 3, 0, 4, 0, 5, 0, 6); // true
```

### `bool in_range(double x, double y, double z, vector @min, vector @max)`
- **Description**: Checks if a 3D point is within a specified range using a vector.
- **Parameters**:
  - `x`, `y`, `z`: The coordinates of the point.
  - `min`: The minimum coordinates as a vector.
  - `max`: The maximum coordinates as a vector.
- **Returns**: `true` if the point is within the range, otherwise `false`.

### `bool in_range(vector @current, vector @min, vector @max)`
- **Description**: Checks if a 3D point is within a specified range using a vector.
- **Parameters**:
  - `current`: The current coordinates as a vector.
  - `min`: The minimum coordinates as a vector.
  - `max`: The maximum coordinates as a vector.
- **Returns**: `true` if the point is within the range, otherwise `false`.

## 11. Toggle and Boolean Functions

### `bool toggle(bool b)`
- **Description**: Toggles a boolean value.
- **Parameters**:
  - `b`: The boolean value to toggle.
- **Returns**: The negated value of the input.

```angelscript
bool toggled = toggle(true); // false
```

### `bool int_to_bool(int b)`
- **Description**: Converts an integer to a boolean.
- **Parameters**:
  - `b`: The integer value (1 for true, 0 for false).
- **Returns**: A boolean value.

```angelscript
bool boolValue = int_to_bool(1); // true
```

### `int toggle(int b)`
- **Description**: Toggles an integer between 0 and 1.
- **Parameters**:
  - `b`: The integer value to toggle (0 or 1).
- **Returns**: The negated value of the input.

```angelscript
int toggled = toggle(1); // 0
```

### `int bool_to_int(bool b)`
- **Description**: Converts a boolean to an integer.
- **Parameters**:
  - `b`: The boolean value (true for 1, false for 0).
- **Returns**: An integer value.

```angelscript
int intValue = bool_to_int(true); // 1
```

## 12. Miscellaneous Utility Functions

### `string ms_to_readable_time(double ms, int round_year_to = 0, int round_month_to = 0, int round_week_to = 0, int round_day_to = 0, int round_hour_to = 0, int round_minute_to = 0, int round_second_to = 0)`
- **Description**: Converts milliseconds to a human-readable time format.
- **Parameters**:
  - `ms`: The duration in milliseconds.
  - `round_year_to`, `round_month_to`, `round_week_to`, `round_day_to`, `round_hour_to`, `round_minute_to`, `round_second_to`: The number of decimal places to round each unit.
- **Returns**: A string representing the time in a readable format.

```angelscript
string readableTime = ms_to_readable_time(3600 * 1000); // "1 hour"
```

### `string string_left(const string&in str, uint count)`
- **Description**: Retrieves the leftmost characters from a string.
- **Parameters**:
  - `str`: The input string.
  - `count`: The number of characters to retrieve.
- **Returns**: A substring containing the specified number of characters.

```angelscript
string leftPart = string_left("Hello, World!", 5); // "Hello"
```

### `string string_right(const string&in str, uint count)`
- **Description**: Retrieves the rightmost characters from a string.
- **Parameters**:
  - `str`: The input string.
  - `count`: The number of characters to retrieve.
- **Returns**: A substring containing the specified number of characters.

```angelscript
string rightPart = string_right("Hello, World!", 6); // "World!"
```

### `string string_trim_left(const string&in str, uint count)`
- **Description**: Trims the left side of a string.
- **Parameters**:
  - `str`: The input string.
  - `count`: The number of characters to trim.
- **Returns**: A substring with the specified number of characters removed from the beginning.

```angelscript
string trimmedLeft = string_trim_left("   Hello, World!", 3); // "Hello, World!"
```

### `string string_trim_right(const string&in str, uint count)`
- **Description**: Trims the right side of a string.
- **Parameters**:
  - `str`: The input string.
  - `count`: The number of characters to trim.
- **Returns**: A substring with the specified number of characters removed from the end.

```angelscript
string trimmedRight = string_trim_right("Hello, World!   ", 3); // "Hello, World!"
```

### `string var_replace(string&out text, string[] replacers = {}, const string&in opening = "%", const string&in closing = "%")`
- **Description**: Replaces variables in a string with specified values.
- **Parameters**:
  - `text`: The input string containing variables.
  - `replacers`: An array of strings to replace the variables.
  - `opening`, `closing`: Delimiters for identifying variables (default is "%").
- **Returns**: The modified string.

```angelscript
string text = "Hello, %1!";
string[] replacements = {"World"};
string result = var_replace(text, replacements); // "Hello, World!"
```

### `string var_replace2(string&out text, string[] fir = {}, string[] sec = {})`
- **Description**: Replaces substrings in a string with specified values.
- **Parameters**:
  - `text`: The input string containing substrings to replace.
  - `fir`, `sec`: Arrays of strings for replacement (must be equal length).
- **Returns**: The modified string.

```angelscript
string text = "Hello, World!";
string[] find = {"World"};
string[] replaceWith = {"Universe"};
string result = var_replace2(text, find, replaceWith); // "Hello, Universe!"
```
