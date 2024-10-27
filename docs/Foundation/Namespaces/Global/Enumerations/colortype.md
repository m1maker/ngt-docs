# colortype Enum

## Overview
The `colortype` enum defines different types of color representations that can be used to store and process image data. These types specify how the red, green, blue (and sometimes alpha) components are organized within a pixel.

## Syntax
```angelscript
enum colortype {
    COLOR_TYPE_UNKNOWN,
    COLOR_TYPE_RGB,
    COLOR_TYPE_YCBCR
};
```

## Enum Values
- **COLOR_TYPE_UNKNOWN (0)**: Represents an unknown or unspecified color type.
- **COLOR_TYPE_RGB (1)**: Represents a color format with red, green, and blue components. This is a common format for storing truecolor images.
- **COLOR_TYPE_YCBCR (2)**: Represents a color format using the YCbCr color space, which separates luminance (Y) from chrominance (Cb and Cr). This format is often used in video processing and image compression.
