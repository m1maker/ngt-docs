### `void set_interrupt(bool) property`
- **Parameters**:
  - `interrupt` (bool): Whether to enable or disable interrupts.
- **Description**: Sets whether the screen reader should interrupt current speech when a new message is received.

### `bool get_interrupt() property`
- **Return Type**: bool
- **Description**: Gets whether interrupts are currently enabled for the screen reader as a property.

### `bool speak(const string&in text, bool interrupt = true)`
- **Parameters**:
  - `text` (const string&): The text to be spoken.
  - `interrupt` (bool): Whether to interrupt current speech if it is already running.
- **Return Type**: bool
- **Description**: Speaks the specified text. If `interrupt` is `true`, it will stop any ongoing speech before starting the new message.

### `bool braille(const string&in text)`
- **Parameters**:
  - `text` (const string&): The text to be output as Braille.
- **Return Type**: bool
- **Description**: Outputs the specified text using Braille technology. Returns `true` if successful; otherwise, returns `false`.

### `void stop_speech()`
- **Description**: Stops any ongoing speech or braille output.

### `string detect()`
- **Return Type**: string
- **Description**: Detects and returns current screen reader name.
