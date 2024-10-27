# matrixcoefficients Enum

## Overview
The `matrixcoefficients` enum defines the transformation matrix used to convert from the color space of a source image or video to the color space of a target display. These matrices are crucial for maintaining accurate color representation when processing media.

## Syntax
```angelscript
enum matrixcoefficients {
    MATRIX_COEFFICIENTS_IDENTITY,
    MATRIX_COEFFICIENTS_BT709,
    MATRIX_COEFFICIENTS_UNSPECIFIED,
    MATRIX_COEFFICIENTS_FCC,
    MATRIX_COEFFICIENTS_BT470BG,
    MATRIX_COEFFICIENTS_BT601,
    MATRIX_COEFFICIENTS_SMPTE240,
    MATRIX_COEFFICIENTS_YCGCO,
    MATRIX_COEFFICIENTS_BT2020_NCL,
    MATRIX_COEFFICIENTS_BT2020_CL,
    MATRIX_COEFFICIENTS_SMPTE2085,
    MATRIX_COEFFICIENTS_CHROMA_DERIVED_NCL,
    MATRIX_COEFFICIENTS_CHROMA_DERIVED_CL,
    MATRIX_COEFFICIENTS_ICTCP,
    MATRIX_COEFFICIENTS_CUSTOM
};
```

## Enum Values
- **MATRIX_COEFFICIENTS_IDENTITY (0)**: Represents an identity transformation matrix, which leaves the color values unchanged.
- **MATRIX_COEFFICIENTS_BT709 (1)**: Transformation matrix based on Rec. 709 for HDTV and Blu-ray displays.
- **MATRIX_COEFFICIENTS_UNSPECIFIED (2)**: Indicates that the transformation matrix is not specified in the media data.
- **MATRIX_COEFFICIENTS_FCC (4)**: Transformation matrix based on Federal Communications Commission standards, primarily used in NTSC systems.
- **MATRIX_COEFFICIENTS_BT470BG (5)**: Transformation matrix based on BT.470 (1990) for SECAM and PAL systems.
- **MATRIX_COEFFICIENTS_BT601 (6)**: Transformation matrix based on Rec. 601 for NTSC, PAL, and SECAM television standards.
- **MATRIX_COEFFICIENTS_SMPTE240 (7)**: Transformation matrix used in studio lighting and photography.
- **MATRIX_COEFFICIENTS_YCGCO (8)**: Chromaticity coordinates using the YCbCr color space with a different chroma component arrangement than BT.601.
- **MATRIX_COEFFICIENTS_BT2020_NCL (9)**: Normalized chrominance components for BT.2020, used for 10-bit HDR content.
- **MATRIX_COEFFICIENTS_BT2020_CL (10)**: Chromaticity coordinates using the YCbCr color space with normalized chroma components for BT.2020, used for 12-bit HDR content.
- **MATRIX_COEFFICIENTS_SMPTE2085 (11)**: Chromaticity coordinates based on SMPTE ST 2085, designed for high dynamic range scenes with a larger gamut than Rec. 2020.
- **MATRIX_COEFFICIENTS_CHROMA_DERIVED_NCL (12)**: Chromaticity coordinates derived from the source chroma components for BT.2020, normalized.
- **MATRIX_COEFFICIENTS_CHROMA_DERIVED_CL (13)**: Chromaticity coordinates derived from the source chroma components for BT.2020, unnormalized.
- **MATRIX_COEFFICIENTS_ICTCP (14)**: Intensity-Chrominance-Tone Curve (ICTCP) transformation matrix for HDR displays and mastering workflows.
- **MATRIX_COEFFICIENTS_CUSTOM (31)**: Indicates that the transformation matrix is custom-defined.
