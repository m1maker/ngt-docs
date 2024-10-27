# scalemode Enum

## Overview
The `scalemode` enum defines the scaling methods that can be used to resize images, textures, or other graphical elements. These modes control how pixel data is interpolated when the dimensions of an image change.

## Syntax
```angelscript
enum scalemode {
    SCALEMODE_NEAREST,
    SCALEMODE_LINEAR
};
```

## Enum Values
- **SCALEMODE_NEAREST (0)**: Uses nearest neighbor interpolation for scaling. This method preserves edges but can result in pixelation, especially when scaling up.
- **SCALEMODE_LINEAR (1)**: Uses linear interpolation for scaling. This method provides smoother results by blending nearby pixels, which is generally preferred for scaling up.
