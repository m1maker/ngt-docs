# pixeltype Enum

## Overview
The `pixeltype` enum defines the different types of pixel data that can be used in images, textures, and other graphical elements. These types specify how the pixel values are stored and interpreted.

## Syntax
```angelscript
enum pixeltype {
    PIXELTYPE_UNKNOWN,
    PIXELTYPE_INDEX1,
    PIXELTYPE_INDEX4,
    PIXELTYPE_INDEX8,
    PIXELTYPE_PACKED8,
    PIXELTYPE_PACKED16,
    PIXELTYPE_PACKED32,
    PIXELTYPE_ARRAYU8,
    PIXELTYPE_ARRAYU16,
    PIXELTYPE_ARRAYU32,
    PIXELTYPE_ARRAYF16,
    PIXELTYPE_ARRAYF32,
    PIXELTYPE_INDEX2
};
```

## Enum Values
- **PIXELTYPE_UNKNOWN (0)**: Represents an unknown or unspecified pixel type.
- **PIXELTYPE_INDEX1 (1)**: Each pixel is represented by a 1-bit index into a color palette.
- **PIXELTYPE_INDEX4 (2)**: Each pixel is represented by a 4-bit index into a color palette.
- **PIXELTYPE_INDEX8 (3)**: Each pixel is represented by an 8-bit index into a color palette.
- **PIXELTYPE_PACKED8 (4)**: Pixel values are packed into 8-bit quantities, typically representing red, green, and blue components.
- **PIXELTYPE_PACKED16 (5)**: Pixel values are packed into 16-bit quantities, often including alpha as well as RGB.
- **PIXELTYPE_PACKED32 (6)**: Pixel values are packed into 32-bit quantities, providing full RGB(A) information.
- **PIXELTYPE_ARRAYU8 (7)**: Each component (red, green, blue, and optionally alpha) is represented by an 8-bit unsigned integer.
- **PIXELTYPE_ARRAYU16 (8)**: Each component is represented by a 16-bit unsigned integer.
- **PIXELTYPE_ARRAYU32 (9)**: Each component is represented by a 32-bit unsigned integer.
- **PIXELTYPE_ARRAYF16 (10)**: Each component is represented by a 16-bit floating-point number.
- **PIXELTYPE_ARRAYF32 (11)**: Each component is represented by a 32-bit floating-point number.
- **PIXELTYPE_INDEX2 (12)**: Each pixel is represented by a 2-bit index into a color palette.
