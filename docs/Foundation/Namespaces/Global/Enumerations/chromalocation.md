# chromalocation Enum

## Overview
The `chromalocation` enum defines the sampling location of chroma components (Cr and Cb) relative to luma components (Y) in various image and video formats. This information is crucial for correct color reconstruction during decoding and display.

## Syntax
```angelscript
enum chromalocation {
    CHROMA_LOCATION_NONE,
    CHROMA_LOCATION_LEFT,
    CHROMA_LOCATION_CENTER,
    CHROMA_LOCATION_TOPLEFT
};
```

## Enum Values
- **CHROMA_LOCATION_NONE (0)**: Represents an unknown or unspecified chroma location.
- **CHROMA_LOCATION_LEFT (1)**: Chroma components are sampled at the left edge of each macroblock, with a half-pixel shift between luma and chroma samples.
- **CHROMA_LOCATION_CENTER (2)**: Chroma components are sampled at the center of each macroblock, with a quarter-pixel shift between luma and chroma samples.
- **CHROMA_LOCATION_TOPLEFT (3)**: Chroma components are sampled at the top-left edge of each macroblock, with a half-pixel shift in both horizontal and vertical directions.
