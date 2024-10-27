# colorrange Enum

## Overview
The `colorrange` enum defines the valid range of values that can be used to represent colors in various image and video formats. These ranges are crucial for maintaining accurate color representation when processing media.

## Syntax
```angelscript
enum colorrange {
    COLOR_RANGE_UNKNOWN,
    COLOR_RANGE_LIMITED,
    COLOR_RANGE_FULL
};
```

## Enum Values
- **COLOR_RANGE_UNKNOWN (0)**: Represents an unknown or unspecified color range.
- **COLOR_RANGE_LIMITED (1)**: Represents a limited color range, typically used in consumer-grade video where the valid values are restricted to 16-235 for Y and 16-240 for Cb and Cr (for YCbCr) or R and B (for RGB).
- **COLOR_RANGE_FULL (2)**: Represents a full color range, which can include all possible values from 0 to 255. This is commonly used in professional-grade video where the full dynamic range of the hardware is utilized.
