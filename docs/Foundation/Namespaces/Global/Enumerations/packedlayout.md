# packedlayout Enum

## Overview
The `packedlayout` enum defines the layout and bit allocation for packed pixel formats. These layouts specify how individual color components (red, green, blue, and alpha) are encoded into a single word or integer value. Understanding these layouts is crucial when working with image processing libraries that use packed pixel representations.

## Syntax
```angelscript
enum packedlayout {
    PACKEDLAYOUT_NONE,
    PACKEDLAYOUT_332,
    PACKEDLAYOUT_4444,
    PACKEDLAYOUT_1555,
    PACKEDLAYOUT_5551,
    PACKEDLAYOUT_565,
    PACKEDLAYOUT_8888,
    PACKEDLAYOUT_2101010,
    PACKEDLAYOUT_1010102
};
```

## Enum Values
- **PACKEDLAYOUT_NONE (0)**: Represents an unknown or unspecified packed layout.
- **PACKEDLAYOUT_332 (1)**: 8-bit packed format with 3 bits for red, 3 bits for green, and 2 bits for blue. Often used for display purposes where high color accuracy is not critical.
- **PACKEDLAYOUT_4444 (2)**: 16-bit packed format with 4 bits each for red, green, blue, and alpha. Provides good color accuracy at the cost of higher memory usage.
- **PACKEDLAYOUT_1555 (3)**: 16-bit packed format with 1 bit for alpha and 5 bits each for red, green, and blue. Often used in hardware that supports this layout for efficient blending.
- **PACKEDLAYOUT_5551 (4)**: 16-bit packed format with 1 bit for alpha and 5 bits each for red, green, and blue. Similar to `PACKEDLAYOUT_1555`, but with a different arrangement of bits.
- **PACKEDLAYOUT_565 (5)**: 16-bit packed format with 5 bits each for red and green, and 6 bits for blue. Often used in graphics hardware where this specific layout is supported.
- **PACKEDLAYOUT_8888 (6)**: 32-bit packed format with 8 bits each for red, green, blue, and alpha. Provides the highest color accuracy but uses the most memory.
- **PACKEDLAYOUT_2101010 (7)**: 32-bit packed format with 2 bits for alpha, 10 bits each for red and green, and 1 bit each for blue and alpha. Used in some graphics APIs where this specific layout is supported for efficient storage.
- **PACKEDLAYOUT_1010102 (8)**: 32-bit packed format with 2 bits for alpha, 10 bits each for red and green, and 1 bit for blue. Similar to `PACKEDLAYOUT_2101010`, but with a different arrangement of bits.
