## Constructors

### `effect(string&in type)`
- **Parameters**:
  - `type`: A string representing the type of sound effect.
- **Description**: Initializes a new instance of the `effect` class with the specified type.

### `~effect()`
- **Parameters**: None
- **Description**: Uninitializes a default `effect` instance. Detaches all attached handles if they are no longer safe and resets the muted array.

## Methods

### `is_safe(sound @handle)`
- **Parameters**:
  - `handle`: The sound handle to check.
- **Returns**: A boolean indicating whether the handle is safe (not null and active).
- **Description**: Checks if a given sound handle is valid and active. Returns `false` if the handle is null or not active.

### `attach(sound @handle)`
- **Parameters**:
  - `handle`: The sound handle to attach.
- **Returns**: A boolean indicating whether the attachment was successful.
- **Description**: Attaches a sound handle to the effect if it's safe and ensures it's added to the list of attached handles. Configures the effect on the handle.

### `detach(sound @handle, bool complete = true)`
- **Parameters**:
  - `handle`: The sound handle to detach.
  - `complete`: A boolean indicating whether to completely remove the handle from the list (default is `true`).
- **Returns**: A boolean indicating whether the detachment was successful.
- **Description**: Detaches a sound handle from the effect if it's safe. Optionally removes the handle from the list and resets the muted array.

### `configure_effect(sound @handle)`
- **Parameters**:
  - `handle`: The sound handle to configure.
- **Returns**: A boolean indicating whether the configuration was successful. Default implementation returns `false`.
- **Description**: This method can be overridden by subclasses to provide specific configurations for sound effects. Currently, it does nothing and always returns `false`.

### `ranges_monitor()`
- **Parameters**: None
- **Description**: Monitors the ranges defined (`left_range`, `right_range`, etc.) and mutes or unmutes attached sounds based on whether they are within these ranges.

## Properties

### `type`, `upper_range`, `lower_range`, `left_range`, `right_range`, `backward_range`, `forward_range`
- **Type**: `string`, `float`
- **Description**: These properties define the type and spatial ranges of the effect. The `type` property indicates the kind of sound effect, while the range properties dictate within which spatial boundaries sounds should be affected.

### `attached_handles`, `muted`
- **Type**: `array<sound @>`, `array<bool>`
- **Description**: These protected arrays store references to attached sound handles and their muted status respectively. The `attached_handles` array keeps track of all sound handles that have been attached, while the `muted` array tracks whether each handle is currently muted based on its spatial position.

## Usage

To use this class effectively, you would typically create a subclass that implements the `configure_effect` method to set up specific parameters for your effect. You can attach and detach sounds as needed within a loop or at key events, such as when the listener's position changes.
