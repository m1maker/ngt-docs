## Window Management

### `bool show_window(const string&in title, int width = 640, int height = 480, bool enable_renderer = false)`
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
