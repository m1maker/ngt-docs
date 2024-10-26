## Clipboard Operations

### `bool clipboard_copy_text(const string&in text)`
- **Parameters**:
  - `text` (const string&): The text to copy to the clipboard.
- **Return Type**: bool
- **Description**: Copies the specified text to the clipboard and returns `true` if successful; otherwise, returns `false`.

### `string clipboard_read_text()`
- **Return Type**: string
- **Description**: Reads the current text from the clipboard.
