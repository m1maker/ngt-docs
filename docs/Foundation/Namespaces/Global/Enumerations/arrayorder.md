# arrayorder Enum

## Overview
The `arrayorder` enum defines the order in which pixel components (red, green, blue, and alpha) are stored in a one-dimensional array. These orders affect how the pixels are accessed and interpreted when processing image data.

## Syntax
```angelscript
enum arrayorder {
    ARRAYORDER_NONE,
    ARRAYORDER_RGB,
    ARRAYORDER_RGBA,
    ARRAYORDER_ARGB,
    ARRAYORDER_BGR,
    ARRAYORDER_BGRA,
    ARRAYORDER_ABGR
};
```

## Enum Values
- **ARRAYORDER_NONE (0)**: Represents an unknown or unspecified array order.
- **ARRAYORDER_RGB (1)**: Pixels are stored with the red, green, and blue components in that order. This is a common format for representing color data without alpha transparency.
- **ARRAYORDER_RGBA (2)**: Pixels are stored with the red, green, blue, and alpha components in that order. This format includes an alpha channel for transparency information.
- **ARRAYORDER_ARGB (3)**: Pixels are stored with the alpha, red, green, and blue components in that order. This format starts with the alpha channel to facilitate blending operations.
- **ARRAYORDER_BGR (4)**: Pixels are stored with the blue, green, and red components in that order. This format is less common but can be useful for certain graphics operations.
- **ARRAYORDER_BGRA (5)**: Pixels are stored with the blue, green, red, and alpha components in that order. This format includes an alpha channel at the end of the pixel data.
- **ARRAYORDER_ABGR (6)**: Pixels are stored with the alpha, blue, green, and red components in that order. This format starts with the alpha channel and is less common than other formats.
