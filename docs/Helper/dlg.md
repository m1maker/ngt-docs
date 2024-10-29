## Function: dlg

### Parameters

- `string& in message = ""`: The message to display in the dialog.
- `uint64 time = 0`: The duration (in milliseconds) for which the dialog should be displayed. If set to 0, the dialog will wait indefinitely until a key is pressed.
- `dlg_callback @cb = null`: A callback function that is executed periodically during the dialog's display. This can be used for updating the dialog's state or performing other actions.
- `bool auto_close = false`: If `true`, and the dialog times out, it will automatically close.

### Usage

The `dlg` function can be used to display a dialog with various options:
- **Message Display**: Pass a string message to be displayed.
- **Timeout**: Set a duration for the dialog using the `time` parameter. The dialog will close after this time if no key is pressed.
- **Callback Function**: Provide a callback function (`dlg_callback`) that will be executed periodically during the dialog's display. This can be used for updating UI elements or performing other tasks.
- **Auto-Close**: Use the `auto_close` parameter to automatically close the dialog when it times out.
