# colorprimaries Enum

## Overview
The `colorprimaries` enum defines the chromaticity coordinates of the three primary colors used in various image and video formats. These primary colors determine the color gamut that can be represented, which is crucial for accurate color representation when processing media.

## Syntax
```angelscript
enum colorprimaries {
    PRIMARIES_UNKNOWN,
    PRIMARIES_BT709,
    PRIMARIES_UNSPECIFIED,
    PRIMARIES_BT470M,
    PRIMARIES_BT470BG,
    PRIMARIES_BT601,
    PRIMARIES_SMPTE240,
    PRIMARIES_GENERIC_FILM,
    PRIMARIES_BT2020,
    PRIMARIES_XYZ,
    PRIMARIES_SMPTE431,
    PRIMARIES_SMPTE432,
    PRIMARIES_EBU3213,
    PRIMARIES_CUSTOM
};
```

## Enum Values
- **PRIMARIES_UNKNOWN (0)**: Represents an unknown or unspecified set of color primaries.
- **PRIMARIES_BT709 (1)**: Standard primary colors for HDTV, Blu-ray, and many modern displays. Also known as Rec. 709.
- **PRIMARIES_UNSPECIFIED (2)**: Indicates that the color primaries are not specified in the media data.
- **PRIMARIES_BT470M (4)**: Primary colors based on BT.470 (1953) for NTSC systems, which have a slightly smaller gamut than Rec. 709.
- **PRIMARIES_BT470BG (5)**: Primary colors based on BT.470 (1990) for SECAM and PAL systems.
- **PRIMARIES_BT601 (6)**: Primary colors used in NTSC, PAL, and SECAM television standards, also known as Rec. 601.
- **PRIMARIES_SMPTE240 (7)**: Primary colors used in studio lighting and photography.
- **PRIMARIES_GENERIC_FILM (8)**: Generic primary colors for film emulation.
- **PRIMARIES_BT2020 (9)**: Primary colors for HDR displays, also known as Rec. 2020.
- **PRIMARIES_XYZ (10)**: Chromaticity coordinates in the CIE XYZ color space.
- **PRIMARIES_SMPTE431 (11)**: Primary colors based on SMPTE ST 431, used for high dynamic range scenes with a larger gamut than Rec. 2020.
- **PRIMARIES_SMPTE432 (12)**: Primary colors based on SMPTE ST 432, similar to Rec. 2020 but designed for improved colorimetric accuracy.
- **PRIMARIES_EBU3213 (22)**: Chromaticity coordinates defined in EBU Technical Specification 3213, used primarily in Europe for broadcast television and radio.
- **PRIMARIES_CUSTOM (31)**: Indicates that the primary colors are custom-defined.
