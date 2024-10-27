# blendmode Enum

## Overview
The `blendmode` enum defines the different blending modes that can be used for rendering graphics elements. These modes control how pixel colors are combined when drawing over existing pixels on the screen.

## Syntax
```angelscript
enum blendmode {
    BLENDMODE_NONE,
    BLENDMODE_BLEND,
    BLENDMODE_BLEND_PREMULTIPLIED,
    BLENDMODE_ADD,
    BLENDMODE_ADD_PREMULTIPLIED,
    BLENDMODE_MOD,
    BLENDMODE_MUL,
    BLENDMODE_INVALID
};
```

## Enum Values
- **BLENDMODE_NONE (0)**: No blending is performed. The source pixel will replace the destination pixel.
- **BLENDMODE_BLEND (1)**: Basic blending mode using standard alpha blending. This combines the source and destination pixels based on their alpha values.
- **BLENDMODE_BLEND_PREMULTIPLIED (16)**: Blending mode for pre-multiplied alpha images. This method assumes that the alpha has already been multiplied into the color channels, which can improve performance in some scenarios.
- **BLENDMODE_ADD (2)**: Adds the source pixel to the destination pixel. Useful for creating glowing or additive effects.
- **BLENDMODE_ADD_PREMULTIPLIED (32)**: Adds the pre-multiplied source pixel to the destination pixel. Similar to `BLENDMODE_ADD`, but assumes pre-multiplied alpha.
- **BLENDMODE_MOD (4)**: Multiplies the source pixel with the inverse of the destination pixel, then subtracts 1 from the result. This can be used for various effects like color burn or screen blending.
- **BLENDMODE_MUL (8)**: Multiplies the source and destination pixels together. Useful for creating darkening or multiplying effects.
- **BLENDMODE_INVALID (2147483647)**: Represents an invalid blend mode value.
