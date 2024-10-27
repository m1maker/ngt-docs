# bitmaporder Enum

## Overview
The `bitmaporder` enum defines the order in which pixel components (red, green, blue, and alpha) are stored in an image or texture. These orders affect how the pixels are interpreted when rendering graphics.

## Syntax
```angelscript
enum bitmaporder {
    BITMAPORDER_NONE,
    BITMAPORDER_4321,
    BITMAPORDER_1234
};
```

## Enum Values
- **BITMAPORDER_NONE (0)**: Represents an unknown or unspecified bitmap order.
- **BITMAPORDER_4321 (1)**: Pixels are stored with the alpha channel first, followed by red, green, and blue. This is also known as ABGR format.
- **BITMAPORDER_1234 (2)**: Pixels are stored with the red channel first, followed by green, blue, and alpha. This is also known as RGBA format.
