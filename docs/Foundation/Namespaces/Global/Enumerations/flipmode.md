# flipmode Enum

## Overview
The `flipmode` enum defines the different ways an image or texture can be flipped. These modes allow you to mirror content horizontally, vertically, or both, which is useful for various visual effects and optimizations.

## Syntax
```angelscript
enum flipmode {
    FLIP_NONE,
    FLIP_HORIZONTAL,
    FLIP_VERTICAL
};
```

## Enum Values
- **FLIP_NONE (0)**: The image or texture remains in its original orientation without any flipping.
- **FLIP_HORIZONTAL (1)**: The image or texture is flipped horizontally, reflecting it along the vertical axis.
- **FLIP_VERTICAL (2)**: The image or texture is flipped vertically, reflecting it along the horizontal axis.
