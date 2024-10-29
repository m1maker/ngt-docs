## 1. Overview

The `key_hold` class monitors a specific key's state (pressed or released) and manages repeat events based on predefined settings. It also provides methods to reset the state, set new repeat times, and retrieve historical event data.

This class is useful in scenarios where you need precise control over keyboard input handling, such as game controls, UI interactions, or any application requiring dynamic key response.

## 2. Class Members

### `keycode key_code`
- **Type**: `keycode`
- **Description**: The keycode of the key being monitored.

### `bool pressed`
- **Type**: `bool`
- **Description**: Indicates whether the key is currently pressed (`true`) or released (`false`).

### `uint64 timestamp`
- **Type**: `uint64`
- **Description**: The timestamp (in milliseconds) when the key event occurred.

### `on_press_callback @on_press`
- **Type**: `on_press_callback`
- **Description**: A callback function to be executed when the key is pressed. This can be customized by assigning a function to this member variable.

### `on_release_callback @on_release`
- **Type**: `on_release_callback`
- **Description**: A callback function to be executed when the key is released. This can be customized by assigning a function to this member variable.

### `array<key_event @> key_history`
- **Type**: `array<key_event @>`
- **Description**: An array that stores historical key events, including press and release times.

### `uint64 repeat_time`
- **Type**: `uint64`
- **Description**: The time interval (in milliseconds) at which the key repeats when held down.

### `uint64 setting_1`, `setting_2`
- **Type**: `uint64`
- **Description**: These variables store additional settings, with `setting_1` controlling the first repeat interval and `setting_2` controlling the second repeat interval.

### `timer key_timer`
- **Type**: `timer`
- **Description**: A timer used to track elapsed time since the last event.

### `uint64 wait_time`
- **Type**: `uint64`
- **Description**: An optional wait time (in milliseconds) that must pass before the first repeat occurs.

## 3. Constructors

### `key_hold(const keycode&in _key_code, const uint64&in _setting_1, const uint64&in _setting_2)`
- **Parameters**:
  - `_key_code`: The keycode of the key to monitor.
  - `_setting_1`, `_setting_2`: The repeat times for the first and second intervals.
- **Description**: Initializes the `key_hold` object with specified parameters.

### `key_hold()`
- **Parameters**: None
- **Description**: Initializes a default `key_hold` object, resetting all properties to their initial state.

## 4. Destructor

### `~key_hold()`
- **Parameters**: None
- **Description**: Cleans up the `key_hold` object when it is no longer needed.

## 5. Methods

### `bool pressing()`
- **Returns**: A boolean indicating whether a new press event has been detected since the last call.
- **Description**:
  - Monitors the key state and triggers the appropriate callbacks based on the key's state (pressed or released).
  - Adjusts the repeat time based on the current state and settings.

### `void reset()`
- **Parameters**: None
- **Description**:
  - Resets all properties of the `key_hold` object to their initial values.
  - Clears the history array and stops any active timers.

### `void set_repeat_times(uint64 new_setting_1, uint64 new_setting_2)`
- **Parameters**:
  - `new_setting_1`, `new_setting_2`: The new repeat times for the first and second intervals.
- **Description**: Updates the repeat times with the specified values.

### `void set_wait_time(uint64 new_wait_time)`
- **Parameters**:
  - `new_wait_time`: The new dynamic wait time (in milliseconds).
- **Description**: Sets a new wait time that must pass before the first repeat occurs.

## 6. Callbacks

The class includes two callback functions, `on_press` and `on_release`, which can be customized by assigning appropriate functions to them. These callbacks are invoked when the key is pressed or released.

```angelscript
void onKeyRelease() {
	// Handle release event
}

void onKeyDown() {
	// Handle press event
}
}

// Usage example
key_hold myKeyHold(KEY_SPACE, 100, 200);
@myKeyHold.on_press = onKeyDown;
@myKeyHold.on_release = onKeyRelease;
```

This setup allows for flexible handling of key events and can be integrated into various parts of your game or application to respond dynamically to user input.

## Usage Example

```angelscript
while (true) {
	wait(5);
	if (myKeyHold.pressing()) {
		// Handle key press event
	}
}
```

This example demonstrates how to create an instance of the `key_hold` class, assign callback functions for key events, and monitor these events in a loop.