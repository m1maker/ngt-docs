## Window Management

### `bool show_window(const string&in title, int width = 640, int height = 480, bool enable_renderer = true)`
- **Parameters**:
  - `title` (const string&): The title of the window.
  - `width` (int): The width of the window in pixels (default is 640).
  - `height` (int): The height of the window in pixels (default is 480).
  - `enable_renderer` (bool): Whether to enable rendering for the window.
- **Return Type**: bool
- **Description**: Creates and shows a window with the specified properties. Returns `true` if successful; otherwise, returns `false`.

### `uint64 get_window_handle() property`
- **Return Type**: uint64
- **Description**: Retrieves the handle of the currently active window as a property.

### `void hide_window()`
- **Description**: Hides the currently active window.

### `void set_update_window_freq(int64 freq) property`
- **Parameters**:
  - `freq` (int64): The desired update frequency for the window in milliseconds.
- **Description**: Sets the frequency at which the window should be updated.

### `int64 get_update_window_freq() property`
- **Return Type**: int64
- **Description**: Retrieves the current update frequency of the window in milliseconds as a property.

### `void set_window_title(const string&in title) property`
- **Parameters**:
  - `title` (const string&): The new title for the window.
- **Description**: Sets the title of the window.

### `void window_present()`
- **Description**: Forces the window to redraw its content immediately.

### `int message_box(const string&in title, const string&in text, array<string>@ buttons, uint flags = 0)`
- **Parameters**:
  - `title` (const string&): The title of the message box.
  - `text` (const string&): The text to display in the message box.
  - `buttons` (array<string>@): An array of button labels for the message box.
  - `flags` (uint): Optional flags to customize the message box behavior.
- **Return Type**: int
- **Description**: Displays a message box with the specified title, text, buttons, and flags, and returns the index of the clicked button.

### `bool alert(const string&in title, const string&in text, const string&in button_name = "OK")`
- **Parameters**:
  - `title` (const string&): The title of the alert box.
  - `text` (const string&): The text to display in the alert box.
  - `button_name` (const string&): The label for the alert button.
- **Return Type**: bool
- **Description**: Displays a simple alert box with an "OK" button and returns `true`.

### `int question(const string&in title, const string&in text)`
- **Parameters**:
  - `title` (const string&): The title of the question box.
  - `text` (const string&): The text to display in the question box.
- **Return Type**: int
- **Description**: Displays a question box with "Yes" and "No" buttons, and returns the response.

### `bool urlopen(const string&in url)`
- **Parameters**:
  - `url` (const string&): The URL to open.
- **Return Type**: bool
- **Description**: Opens a URL and returns `true` if successful; otherwise, returns `false`.
