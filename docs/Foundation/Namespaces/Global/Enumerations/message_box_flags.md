# message_box_flags Enum

## Overview
The `message_box_flags` enum defines various flags that can be used to customize the appearance and behavior of a message box in an application. These flags allow you to specify things like the type of icon displayed, the order of buttons, and more.

## Syntax
```angelscript
enum message_box_flags {
    MESSAGE_BOX_ERROR = 16,
    MESSAGE_BOX_WARNING = 32,
    MESSAGE_BOX_INFORMATION = 64,
    MESSAGE_BOX_BUTTONS_LEFT_TO_RIGHT = 128,
    MESSAGE_BOX_BUTTONS_RIGHT_TO_LEFT = 256
};
```

## Enum Values
- **MESSAGE_BOX_ERROR (16)**: Displays an error icon in the message box.
- **MESSAGE_BOX_WARNING (32)**: Displays a warning icon in the message box.
- **MESSAGE_BOX_INFORMATION (64)**: Displays an information icon in the message box.
- **MESSAGE_BOX_BUTTONS_LEFT_TO_RIGHT (128)**: Arranges the buttons in the message box from left to right.
- **MESSAGE_BOX_BUTTONS_RIGHT_TO_LEFT (256)**: Arranges the buttons in the message box from right to left.
