## Debugging

### `void assert(bool expr, const string&in fail_text = "")`
- **Parameters**:
  - `expr` (bool): The expression to check for truthiness.
  - `fail_text` (const string&): Optional text to display if the assertion fails.
- **Description**: Asserts that a condition is true; if false, it will trigger an error with optional custom failure text.
