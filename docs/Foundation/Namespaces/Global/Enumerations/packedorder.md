# packedorder Enum

## Overview
The `packedorder` enum defines the order in which pixel components (red, green, blue, and alpha) are packed into a single 32-bit integer. These orders affect how the pixels are interpreted when rendering graphics.

## Syntax
```angelscript
enum packedorder {
    PACKEDORDER_NONE,
    PACKEDORDER_XRGB,
    PACKEDORDER_RGBX,
    PACKEDORDER_ARGB,
    PACKEDORDER_RGBA,
    PACKEDORDER_XBGR,
    PACKEDORDER_BGRX,
    PACKEDORDER_ABGR,
    PACKEDORDER_BGRA
};
```

## Enum Values
- **PACKEDORDER_NONE (0)**: Represents an unknown or unspecified packed order.
- **PACKEDORDER_XRGB (1)**: Packed order with the alpha channel omitted, followed by red, green, and blue. This is often used for efficient storage but requires careful handling of the alpha component.
- **PACKEDORDER_RGBX (2)**: Packed order with the alpha channel omitted, followed by red, green, and blue. Similar to `PACKEDORDER_XRGB`, this format can be less efficient due to the missing alpha information.
- **PACKEDORDER_ARGB (3)**: Packed order with the alpha channel first, followed by red, green, and blue. This is a common format used in many graphics APIs and libraries.
- **PACKEDORDER_RGBA (4)**: Packed order with the red channel first, followed by green, blue, and alpha. This is another common format used in various rendering systems.
- **PACKEDORDER_XBGR (5)**: Packed order with the alpha channel omitted, followed by blue, green, and red. Similar to `PACKEDORDER_XRGB`, this format can be less efficient due to the missing alpha information.
- **PACKEDORDER_BGRX (6)**: Packed order with the alpha channel omitted, followed by blue, green, and red. This is a less common but still used format for certain graphics operations.
- **PACKEDORDER_ABGR (7)**: Packed order with the alpha channel first, followed by blue, green, and red. This format can be useful in some specific scenarios where the color components are accessed differently from RGB formats.
- **PACKEDORDER_BGRA (8)**: Packed order with the blue channel first, followed by green, red, and alpha. This is another common format used in various rendering systems.
