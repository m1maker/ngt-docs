# Class: joystick

The `joystick` class provides a data structure for managing and controlling a joystick device. It allows you to interact with various properties of the joystick, such as its validity, name, path, serial number, axes, buttons, hats, balls, rumble effects, LED control, power information, and more.

## Constructors

### `joystick(uint id)`
- **Parameters**:
  - `id` (uint): The unique identifier for the joystick.
- **Description**: Constructs a `joystick` object with the specified identifier.


## Methods

### `bool get_valid() const property`
- **Parameters**: None
- **Return Type**: bool
- **Description**: Returns whether the joystick is valid or not.


### `string get_name() const property`
- **Parameters**: None
- **Return Type**: string
- **Description**: Returns the name of the joystick.


### `string get_path() const property`
- **Parameters**: None
- **Return Type**: string
- **Description**: Returns the path to the joystick device.


### `string get_serial() const property`
- **Parameters**: None
- **Return Type**: string
- **Description**: Returns the serial number of the joystick.


### `int get_num_axes() const property`
- **Parameters**: None
- **Return Type**: int
- **Description**: Returns the number of axes on the joystick.


### `int get_num_balls() const property`
- **Parameters**: None
- **Return Type**: int
- **Description**: Returns the number of balls on the joystick.


### `int get_num_hats() const property`
- **Parameters**: None
- **Return Type**: int
- **Description**: Returns the number of hats on the joystick.


### `int get_num_buttons() const property`
- **Parameters**: None
- **Return Type**: int
- **Description**: Returns the number of buttons on the joystick.


### `int16 get_axis(int axis) const`
- **Parameters**:
  - `axis` (int): The index of the axis to retrieve.
- **Return Type**: int16
- **Description**: Retrieves the current state of a specific axis.


### `bool get_button(int button) const`
- **Parameters**:
  - `button` (int): The index of the button to check.
- **Return Type**: bool
- **Description**: Checks whether a specific button is pressed or not.


### `joysticktype get_type() const property`
- **Parameters**: None
- **Return Type**: joysticktype
- **Description**: Returns the type of the joystick.


### `bool get_connected() const property`
- **Parameters**: None
- **Return Type**: bool
- **Description**: Checks whether the joystick is currently connected or not.


### `void set_events_enabled(bool enabled) property`
- **Parameters**:
  - `enabled` (bool): Whether to enable event handling for the joystick.
- **Return Type**: void
- **Description**: Enables or disables event handling for the joystick.


### `bool get_events_enabled() const property`
- **Parameters**: None
- **Return Type**: bool
- **Description**: Checks whether event handling is enabled for the joystick.


### `bool rumble(uint16 low_frequency_rumble, uint16 high_frequency_rumble, uint duration_ms) const`
- **Parameters**:
  - `low_frequency_rumble` (uint16): The intensity of the low-frequency rumble effect.
  - `high_frequency_rumble` (uint16): The intensity of the high-frequency rumble effect.
  - `duration_ms` (uint): The duration of the rumble effect in milliseconds.
- **Return Type**: bool
- **Description**: Applies a rumble effect to the joystick.


### `bool rumble_triggers(uint16 left_rumble, uint16 right_rumble, uint duration_ms) const`
- **Parameters**:
  - `left_rumble` (uint16): The intensity of the left trigger rumble effect.
  - `right_rumble` (uint16): The intensity of the right trigger rumble effect.
  - `duration_ms` (uint): The duration of the rumble effect in milliseconds.
- **Return Type**: bool
- **Description**: Applies a rumble effect to the joystick's triggers.


### `bool get_axis_initial_state(int axis, int16&out state) const`
- **Parameters**:
  - `axis` (int): The index of the axis to retrieve the initial state for.
  - `state` (int16&): Reference to store the initial state of the axis.
- **Return Type**: bool
- **Description**: Retrieves the initial state of a specific axis.


### `bool get_ball(int ball, int&out dx, int&out dy) const`
- **Parameters**:
  - `ball` (int): The index of the ball to retrieve the movement for.
  - `dx` (int&): Reference to store the change in x direction.
  - `dy` (int&): Reference to store the change in y direction.
- **Return Type**: bool
- **Description**: Retrieves the movement of a specific ball.


### `uint8 get_hat(int hat) const`
- **Parameters**:
  - `hat` (int): The index of the hat to retrieve the state for.
- **Return Type**: uint8
- **Description**: Retrieves the current state of a specific hat.


### `bool set_led(uint8 red, uint8 green, uint8 blue) const`
- **Parameters**:
  - `red` (uint8): The intensity of the red LED.
  - `green` (uint8): The intensity of the green LED.
  - `blue` (uint8): The intensity of the blue LED.
- **Return Type**: bool
- **Description**: Sets the color of the joystick's LED.


### `int get_power_info(int&out percent) const`
- **Parameters**:
  - `percent` (int&): Reference to store the battery percentage.
- **Return Type**: int
- **Description**: Retrieves the current battery power percentage of the joystick.
