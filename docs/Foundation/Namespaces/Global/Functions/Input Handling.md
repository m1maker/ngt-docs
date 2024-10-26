## Input Handling

### `bool get_window_active() property`
- **Return Type**: bool
- **Description**: Checks whether the window is currently active as a property.

### `void set_window_fullscreen(bool enable)`
- **Parameters**:
  - `enable` (bool): Whether to enable fullscreen mode.
- **Description**: Sets whether the window should be displayed in fullscreen mode.

## Mouse Input

### `bool mouse_pressed(uint8 button)`
- **Parameters**:
  - `button` (uint8): The mouse button that was pressed.
- **Return Type**: bool
- **Description**: Checks if a specific mouse button was pressed.

### `bool mouse_released(uint8 button)`
- **Parameters**:
  - `button` (uint8): The mouse button that was released.
- **Return Type**: bool
- **Description**: Checks if a specific mouse button was released.

### `bool mouse_down(uint8 button)`
- **Parameters**:
  - `button` (uint8): The mouse button to check for being pressed down.
- **Return Type**: bool
- **Description**: Checks if a specific mouse button is currently pressed down.

## Mouse Coordinates

### `int get_MOUSE_X() property`
- **Return Type**: int
- **Description**: Retrieves the current X-coordinate of the mouse cursor as a property.

### `int get_MOUSE_Y() property`
- **Return Type**: int
- **Description**: Retrieves the current Y-coordinate of the mouse cursor as a property.

### `int get_MOUSE_Z() property`
- **Return Type**: int
- **Description**: Retrieves the current Z-coordinate of the mouse cursor (if available) as a property.

## Keyboard Handling

### `bool key_pressed(keycode)`
- **Parameters**:
  - `keycode` (keycode): The keycode of the key to check for being pressed.
- **Return Type**: bool
- **Description**: Checks if the specified key is currently pressed.

### `bool key_released(keycode)`
- **Parameters**:
  - `keycode` (keycode): The keycode of the key to check for being released.
- **Return Type**: bool
- **Description**: Checks if the specified key was just released.

### `bool key_down(keycode)`
- **Parameters**:
  - `keycode` (keycode): The keycode of the key to check for being held down.
- **Return Type**: bool
- **Description**: Checks if the specified key is currently held down.

### `bool key_repeat(keycode)`
- **Parameters**:
  - `keycode` (keycode): The keycode of the key to check for repeated presses.
- **Return Type**: bool
- **Description**: Checks if the specified key has been repeatedly pressed since the last call.

### `array<int>@ keys_pressed()`
- **Return Type**: array<int>
- **Description**: Retrieves an array of keycodes for all currently pressed keys.

### `array<int>@ keys_released()`
- **Return Type**: array<int>
- **Description**: Retrieves an array of keycodes for all keys that were just released.

### `array<int>@ keys_down()`
- **Return Type**: array<int>
- **Description**: Retrieves an array of keycodes for all keys currently held down.

### `array<int>@ keys_repeat()`
- **Return Type**: array<int>
- **Description**: Retrieves an array of keycodes for all keys that have been repeatedly pressed since the last call.

### `string key_to_string(int key_code)`
- **Parameters**:
  - `key_code` (int): The keycode to convert to a string representation.
- **Return Type**: string
- **Description**: Converts a keycode to its corresponding string representation.

### `int string_to_key(const string&in key_name)`
- **Parameters**:
  - `key_name` (const string&): The name of the key as a string.
- **Return Type**: int
- **Description**: Converts a key name to its corresponding keycode.

### `bool force_key_down(keycode)`
- **Parameters**:
  - `keycode` (keycode): The keycode of the key to force down.
- **Return Type**: bool
- **Description**: Forces the specified key to be held down and returns `true` if successful; otherwise, returns `false`.

### `bool force_key_up(keycode)`
- **Parameters**:
  - `keycode` (keycode): The keycode of the key to force up.
- **Return Type**: bool
- **Description**: Forces the specified key to be released and returns `true` if successful; otherwise, returns `false`.

### `void reset_keyboard()`
- **Description**: Resets keyboard state, releasing any held keys and resetting repeated press tracking.

### `void wait_event()`
- **Description**: Waits for a window event, blocking the current thread until an event occurs.
